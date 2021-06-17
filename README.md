# BasesDatos-Odontologia

## Entidades
  
  * Entidades:
    1. Paciente
    2. Cita
    3. Odontologo
    4. Expediente
    5. Tratamiento
    6. Receta_med
    7. Consultorio
    8. Factura
    9. Gastos_admin
    10.  //

  ### Paciente 
  Almacen de entidades paciente, con atributos nombre (Primer nombre, segundo nombre, primer apellido), telefono, direccion, correo (solo se pedira un correo porque nos servira de referencia), edad e idPaciente. Almacena la informacion del paciente, y algunos de sus datos mas importantes.
  
  ### Cita
  Almacen de entidades cita, con los atributos numConsulta (que es el numero de consulta y el PK), fecha (). Almacena la informacion de la cita que realiza el paciente, es un tipo de referencia, osea que a traves de este elemento puede ser atendido el mismo.
  
  ### Odontologo
  Almacena entidades de tipo odontologo, con atributos nombre, DNI (PK), especialidad (son valores por default). Se guarda la informacion del odontologo, junto con la especialidad que ejerce, ya se tecnico dental, asistente dental, o solo el rol de doctor.
  
  ### Expediente
  Almacena entidades de tipo registro, con atributos idRegistro (PK), descripcion. Son los expedientes, osea los datos que el paciente presenta antes de ser antendido.
  
  ### Tratamiento
  Almacen entidades de tipo tratamiento, con atributos nombre, precio e idTratamiento. Son los diferentes tratamientos que la clinica ofrece a los clientes.
  
  ### Receta_med
  Almacen de entidades tipo receta_med (recetas prescristas por el doctor) con atributos, idReceta, fecha, descripcion. Se guarda la informacion de las recetas medicas y que puedan ser vistas por el medico como por el paciente.
  
  ### Consultorio
  Almacena la informacion del consultorio del odontologo, tiene un idConsultorio, que es la PK del consultorio en que trabaja, ya que es un solo local y un num_consultorio que es el numero del consultorio. 
  
  ### Factura
  Almacena la informacion que se pone en la factura una vez se ha realizado un pago, y esta debe hacerse publica al paciente. Como atributos presenta fecha, direccion, empl_atendio, total_pagar, descuento (tercera edad, rebaja, pago_tarjeta, no_descuento), descripcion y subtotal (total con descuentos e isv).
  
  ### Gastos_admin
  Almacena los gastos administrativos de la empresa, en este caso por medio de las facturas se toman los impuestos y se realiza un total para pago de impuestos y la empresa guarda estos registros para almacenamiento propio.
  
  ### Pago (?)
  
  
  

    
