# styled-components

![logo](https://www.styled-components.com/static/atom.png)

[Pagina oficial](https://www.styled-components.com/)

Librería para dar estilos a nuestros componentes comodamente. [CSS is broken](https://medium.com/@zamarrowski/css-is-broken-5138773e17a5)

## Crear un componente con estilos

```javascript
import styled, { css } from 'styled-components'

export default styled.div`
  border: 1px solid black;
  border-radius: 50px;
`

export const Button = styled.button`
  background-color: white;
  color: black;
  ${props => props.success && css`
    background-color: green;
  `}
`
```
