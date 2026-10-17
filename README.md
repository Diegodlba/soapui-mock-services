# Mock Services con SoapUI

Trabajo de testing de servicios web. Armé un **Mock Service** (un servicio simulado) de la calculadora SOAP pública y lo probé con casos de prueba en SoapUI.

- **Servicio original:** calculadora SOAP, `http://www.dneonline.com/calculator.asmx?WSDL`
- **Herramienta:** SoapUI

## Qué hay en el repositorio

- `Calculator-soapui-project.xml`: proyecto de SoapUI con el Mock Service y los casos de prueba.
- `MockServices_delaBarreraDiego.pdf`: informe con el detalle de cada caso, las assertions y los resultados.

## Qué hice

- Creé un Mock Service con tres operaciones: **Add**, **Multiply** y **Subtract**.
- Configuré respuestas estáticas y una respuesta dinámica con un script **Groovy**.
- Armé 4 casos de prueba: `TC01_Add_Valido`, `TC02_Multiply_Valido`, `TC03_Add_Invalido` y `TC04_Subtract_Valido`.
- Usé assertions de XPath, de esquema (Schema Compliance), de SOAP Fault, de script y de códigos HTTP.

> **Nota:** el mock devuelve valores configurados y no hace el cálculo real. Por ejemplo, una suma puede devolver siempre el mismo resultado. Por eso, los casos que pasan verifican que el mock responde como lo configuré, no que la operación matemática sea correcta.
