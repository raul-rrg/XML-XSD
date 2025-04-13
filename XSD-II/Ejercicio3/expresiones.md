### Expresiones Regulares

1. **"Capítulo 0", "Capítulo 1", ..., "Capítulo 9" (solo se permite un dígito):**
   - `Capítulo \d`
   - `Capítulo [0-9]`

2. **"Capítulo 0", ..., "Capítulo 99" (uno o dos dígitos):**
   - `Capítulo \d{1,2}`
   - `Capítulo [0-9]{1,2}`

3. **"Capítulo 1", ..., "Capítulo 99" (sin "Capítulo 0"):**
   - `Capítulo [1-9]\d?`
   - `Capítulo [1-9]([0-9]?)`

4. **"Capítulo 0", ..., "Capítulo 99", "Capítulo 100" (uno o más dígitos):**
   - `Capítulo \d+`
   - `Capítulo [0-9]+`

5. **Dos caracteres, primer carácter distinto de un dígito y segundo carácter "Z":**
   - `\DZ`
   - `[^0-9]Z`

6. **"ABBC", "ABBBC", ..., "ABBBBBC":**
   - `AB{2,5}C`

7. **"RSS", "RSSS", ..., "RSS3", ..., "RSSSSSSSSSSS7" (dos o más "S", opcionalmente seguidas de un dígito del 3 al 8):**
   - `RS{2,}\d?[3-8]?`
   - `RS{2,}[3-8]?`

8. **"COD" seguido de tres dígitos y uno o más caracteres:**
   - `COD\d{3}.+`
   - `COD[0-9]{3}.*`

