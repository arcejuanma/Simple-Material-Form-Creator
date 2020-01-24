# Simple-Material-Form-Creator
A simple function to speed up the process of form creation using React, Material UI and Axios (currently under construction 🏗)

Functionality:
- Supports Date, Text, Password, Multiline and Select Inputs

# Example:

```javascript
formCreator([{row: 2, placeHolder: 'ajdskahs', name: 'Ejemplo1', type: 'date', required: true}, 
                    {row: 1, placeHolder: 'asds', name:'Ejemplo2', type:'password', value:'hola'},
                    {row: 2, placeHolder: 'asds', name:'Ejemplo3', type:'password'},
                    {row: 4, placeHolder: 'asds', name:'Ejemplo4', type:'select', options:['Hola', 'Como', 'Estas']}, 
                    {row: 2, placeHolder: 'ajdskahs', name: 'Ejemplo5', type: 'text'},
                    {row: 3, placeHolder: 'ajdskahs', name: 'Ejemplo6', type: 'text'},
                    {row: 2, placeHolder: 'ajdskahs', name: 'Ejemplo8', type: 'text'},
                    {row: 3, placeHolder: 'Hola', name: 'Ejemplo7', type: 'date'},
                    {row: 5, placeHolder: 'Hola', name: 'Ejemplo10', type: 'date'},
                    {row: 5, placeHolder: 'Hola', name: 'Ejemplo9', type: 'date'} ], {
                    name: 'Ejemplo', 
                    handler: handleChange2,
                    submit:{
                      text: 'Agregar',
                      alertFrontError: 'Por favor rellenar todos los campos',
                      http:{
                        enforce: 'all',
                        provider: 'axios',
                        route: '/api/example',
                      }
                    },
                    clear:{
                      text: 'Borrar',
                    },
                    restore:{
                      text: 'Restaurar'
                    },
                    headers: {
                      formHeader: ['Un Ejemplo de Formulario', 'h5'],
                      rowHeadersVariant: 'h5',
                      '1':'Mi primer Row',
                      '3': 'Mi Tercer Row' 
                    }})
           
...
