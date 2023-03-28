# solana-rust
# Funcionamiento del Smart Contract

Este es un programa básico en Rust para la blockchain de Solana. Su función es incrementar un contador almacenado en una cuenta de la blockchain cada vez que se llama al programa. Aquí hay un resumen de las partes principales del programa:

El programa tiene una sola función pública llamada process_instruction, que se llama cuando se envía una transacción al programa.

La función process_instruction toma tres argumentos: el program_id, una lista de accounts, y _instruction_data (que no se usa en este caso).

El programa usa la biblioteca borsh para definir el tipo de estado que se almacenará en las cuentas. En este caso, el estado es simplemente un contador de saludos, almacenado como un número entero sin signo de 32 bits.

En la función process_instruction, el programa obtiene la cuenta a la que se va a saludar, verifica que el programa sea el propietario de la cuenta (para asegurarse de que solo el programa pueda modificarla), incrementa el contador de saludos y lo almacena en la cuenta. 

Luego, la función devuelve un resultado Ok para indicar que todo ha ido bien.
El programa también tiene una función de prueba (test_sanity) que prueba la funcionalidad básica del programa.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)


