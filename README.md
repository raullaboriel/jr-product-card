# Product Card

Este es un paquete para hacer despliegue a NPM.

## Raul Laboriel

### Ejemplo
```
import {} from 'jr-product-card'
```
```
<ProductCard
    product={ product }
    className="bg-dark text-white"
    initialValues={{
        count: 6,
        // maxCount: 10,
    }}
>
    {
        ({ reset, count, isMaxCountReached, maxCount, increaseBy  }) => (
            <>
                <ProductImage className="custom-image" style={{ boxShadow: '10px 10px 10px rgba(0,0,0,0.2)' }} />
                <ProductTitle className="text-bold" />
                <ProductButtons className="custom-buttons" />

                <button onClick={ reset }>Reset</button>
                <button onClick={ () => increaseBy(-2) }> -2 </button>
                {
                    ( !isMaxCountReached && <button onClick={ ()=> increaseBy(+2) }> +2 </button> )
                }

                <span>{ count } - { maxCount }</span>
            </>
        )
    }
</ProductCard>
```
