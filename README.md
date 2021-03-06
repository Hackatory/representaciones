# README

Esta app tiene como objetivo armar los mockups de la applicacion de hoteleria y turismo.

La app esta construida en rails y muchas de las features estan hardcodeadas.

## Modelos

### Invoice

Representa una factura de compra o de venta. Se puede asignar un operator retailer (agencia, factura de venta) o un wholesaler (mayorista, factura de compra)

#### Atributos

* *date*
* *operator*
* *invoice_type* - tipo de factura. puede ser A, B o NC
* *sales_point* - punto de venta. primer parte del numero de la factura
* *number* - segunda parte del numero de factura
* *taxed_21_cents* - monto gravado con 21% de IVA, en centavos
* *taxed_105_cents* - monto gravado 10.5%
* *not_taxed_cents* - monto no gravado
* *exempt_cents* - monto exento

#### Atributos virtuales (no se almacenan en la base de datos)

* *taxed_21* - monto gravado 21%, pero en decimales (ej 1050 -> 10.50)
* *tax_21* - IVA correspondiente al monto gravado con 21%, en formato decimal
* *tax_21_cents* - IVA correspondiente al monto gravado con 21%, en centavos

* *taxed_105* - Idem
* *tax_105* - Idem
* *tax_105_cents* - Idem

* *not_taxed* - Monto no gravado, en decimal
* *exempt* - Monto exento, en decimal

* *total* - Total de factura, en decimal
* *total_cents* - Total de factura, en centavos
