# Custumer Segmentation ML Model - KMeans
The repository implements a clarification Machine Learning model using KMeans algorithm form the Scikit Learn Python Library.

The model is based on retail based data.

The data:

## Descripción de las variables
1. transaction_data.csv
    * household_key: Identificación única del cliente.
    * BASKET_ID: Identificación única de la  transacción.
    * PRODUCT_ID: Identificación única del producto.
    * QUANTITY: Cantidad de productos comprados.
    * SALES_VALUE: Monto en dolares de la compra.
    * STORE_ID: Identificación única de cada tienda.
    * WEEK_NO: Semana en que se realizó la transacción (1 - 102)
2. product.csv
    * PRODUCT_ID: Identificación única del producto.
    * MANUFACTURER: Código del proveedor.
    * DEPARTMENT: Departamento al cual pertenece un producto .
    * BRAND: Indica si la marca del producto es internacional o nacional.
    * COMMODITY_DESC:Categoría al que pertenece el producto.
3. hh_demographic.csv
    * AGE_DESC: Rango de edad estimado.
    * MARITAL_STATUS_CODE: Estado marital del cliente.
    * INCOME_DESC: Ingresos del cliente.
    * household_key: ID por cada cliente
    * label: Indica si el cliente es buen comprador o no (0= mal comprador, 1=buen comprador)
