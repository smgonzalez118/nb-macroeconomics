# ANÁLISIS MACROECONÓMICO

Funcionalidades para el análisis macroeconómico. Permite analizar las principales variables macro del país utilizando la función "getMacroDataBCRA()" pudiendo observar datos y evolución junto a indicadores técnicos como medias móviles (utiliza API "https://api.estadisticasbcra.com/"). Asimismo otorga funcionalidades para analizar el dólar Contado Con Liquidación (CCL) y la brecha cambiaria entre el Dólar Oifical y el Dólar CCL.

## INDICE DE FUNCIONES:

- getMacroDataBCRA(endpoint, desde, hasta, timeframe = "daily", smas = True, n_fast = 20, n_slow = 100):
     Esta función devuelve gráfico y datos de cualquier variable macroeconómica del BCRA. Se puede parametrizar el timeframe en diario,
    semanal o anual, y si se quiere agregar medias móviles o no, las cuales generarán un oscilador en otro gráfico debajo que refleje la
    magnitud de diferencia (porcentual) entre las medias móviles. Permite ver la evolución, tendencia, convergencia y divergencia, las
    medidas estadísticas descriptivas principales y la ubicación del valor actual respecto de las mismas (estado de situación).

- getCCL(tipo = "period", period = "1y", desde = None, hasta = None, timeframe = "1d", n_fast = 20, n_slow = 100): Esta función devuelve serie del dólar CCL con indicadores técnicos calculados (RSI, MACD, Estocástico y MM exponenciales). Se puede parametrizar el timeframe en diario, semanal o anual.

- watchCCL(tipo = "period", period = "1y", desde = None, hasta = None, timeframe = "1d", n_fast = 20, n_slow = 100): Esta función devuelve serie del dólar CCL con indicadores técnicos calculados (MACD y MM exponenciales). Se puede parametrizar el timeframe en diario, semanal o anual.

- watchBrechaCambiaria(tipo, period, desde = None, hasta = None, emas = True, timeframe = "1d", n_fast = 10, n_slow = 20): Esta función devuelve: un dataframe con la brecha cambiaria dólar CCL-Oficial, así como un gráfico de evolución del precio con medias móviles cuya longitud es parametrizable.