# React

![React logo](https://logos-download.com/wp-content/uploads/2016/09/React_logo_wordmark.png)

Para empezar con [React](https://reactjs.org/) lo mejor es instalar un paquete de npm llamado **create-react-app** este nos da un scaffolding de un proyecto con todo listo para que no nos tengamos que preocupar de la configuración:

```
sudo npm i -g create-react-app
```

## Iniciar un proyecto

```
create-react-app nombreDelProyecto
```

## Arrancar el proyecto

```
npm start
```

## Crear un componente de clase en React

```javascript
import React from 'react'

class MiComponente extends React.Component {

  render() {
    return (
      <h1>Hola mundo</h1>
    )
  }

}

export default MiComponente
```

## Crear un componente funciona en React

```javascript
import React from 'react'

export default props => 
  <h1>Hola mundo</h1>
```

## Jugando con el estado

```javascript
import React from 'react'

class MiComponente extends React.Component {

  state = {
    count: 0
  }
  incrementCount = this.incrementCount.bind(this)

  render() {
    return (
      <>
        <h1>{this.state.count} clicks</h1>
        <button onClick={this.incrementCount}>Increment</button>
      </>
    )
  }

  incrementCount() {
    this.setState({ count: this.state.count + 1 })
  }

}

export default MiComponente
```

## Jugando con las props

```javascript

const CounterText = props =>
  <h1>{props.count} clicks</h1>

class MiComponente extends React.Component {

  state = {
    count: 0
  }
  incrementCount = this.incrementCount.bind(this)

  render() {
    return (
      <>
        <CounterText count={this.state.count} />
        <button onClick={this.incrementCount}>Increment</button>
      </>
    )
  }

  incrementCount() {
    this.setState({ count: this.state.count + 1 })
  }

}

export default MiComponente
```
