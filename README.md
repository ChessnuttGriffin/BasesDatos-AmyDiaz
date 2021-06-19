# BasesDatos-Odontologia

## Entidades
  
       1.Paciente
       2.Consulta
       3.Odontologo
       4.Expediente
       5.Tratamiento
       6.Receta_med
       7.Local
       8.Consultorio
       9.Empleado
       10.Factura 
   

  ### Paciente 
  Almacen de entidades paciente, con atributos nombre (Primer nombre, segundo nombre, primer apellido), telefono, direccion, correo (solo se pedira un correo porque nos servira de referencia), edad e idPaciente. Almacena la informacion del paciente, y algunos de sus datos mas importantes.
  
  ### Consulta
  Almacen de entidades consulta, con los atributos numConsulta (que es el numero de consulta y el PK), fecha y el Id_Paciente. Almacena la informacion de la cita que realiza el paciente, es un tipo de referencia, osea que a traves de este elemento puede ser atendido el mismo.
  
  ### Odontologo
  Almacena entidades de tipo odontologo, con atributos nombre, DNI (PK), especialidad (son valores por default). Se guarda la informacion del odontologo, junto con la especialidad que ejerce, ya se tecnico dental, asistente dental, o solo el rol de doctor.
  
  ### Expediente
  Almacena entidades de tipo registro, con atributos idRegistro (PK), descripcion. Son los expedientes, osea los datos que el paciente presenta antes de ser antendido.
  
  ### Tratamiento
  Almacen entidades de tipo tratamiento, con atributos nombre, precio e idTratamiento. Son los diferentes tratamientos que la clinica ofrece a los clientes.
  
  ### Receta_med
  Almacen de entidades tipo receta_med (recetas prescristas por el doctor) con atributos, idReceta, fecha, descripcion y el Id_Paciente. Se guarda la informacion de las recetas medicas y que puedan ser vistas por el medico como por el paciente.
  
  ### Local
  Local almacena la informacion relacionada a la ubicacion del local de la misma clinica (Como es una empresa, pueden haber varias locales con diferentes ubicaciones). Sus atributos son la direccion que es compuesta (Avenida, Calle y ciudad), Id_local y el telefono, que es multivalor.
  
  ### Consultorio
  Almacena la informacion del consultorio del odontologo, tiene un num_Consultorio, que es la PK del consultorio en que trabaja, ya que es un solo local, la ubicacion y un nombre de consultorio. Es una entidad debil porque sin un local, no existiria un consultorio. 
  
  ### Empleado
  Almacena entidades de tipo empleado, aqui se encuentran todos los empleados que son parte de la clinica pero tienen funciones a parte del odontologo. Sus atributos son el DNI (PK), Cargo, Telefono, Sexo, Nombre (Atributo compuesto).
  
  ### Factura
  Almacena la informacion que se pone en la factura una vez se ha realizado un pago, y esta debe hacerse publica al paciente. Como atributos presenta fecha, direccion, empl_atendio, total_pagar, descuento (tercera edad, rebaja, pago_tarjeta, no_descuento), descripcion y subtotal (total con descuentos e isv).
  
/*### Gastos_admin
Almacena los gastos administrativos de la empresa, en este caso por medio de las facturas se toman los impuestos y se realiza un total para pago de impuestos y la empresa guarda estos registros para almacenamiento propio.*/
  
  
  ### Relaciones
  
  1. El paciente realiza una consulta, esto se puede hacer gracias al id del paciente, que es una instancia de Paciente que contiene todos los datos en el.
  2. El paciente tiene un expdiente diferente cada vez que se realiza un tratamiento.
  3. El expediente lo crea el odontologo, quien tambien es el que brinda la consulta.
  4. El Odontologo es quien realiza el tratamiento especifico y quien establece las redacta las recetas medicas, tambien es quien puede realizar varios tratamientos.
  5. El odontologo trabaja en un local (Es una sola clinica, que tiene varios locales) y en el mismo local, el odontologo tiene un consultorio, que es como la          oficina del odontologo (Un odontologo, puede no tener un consultorio, o bien puede compartir el consultorio con otro odontologo).
  6. En el local laboran varios empleados.
  7. Tratamiento tiene una relacion con factura donde solo se puede dar una factura por tratamiento.
  
  
  
  

    
