# Proyecto1

var Lista_Clientes = new List<Clientes>();
Lista_Clientes.Add(new Clientes(){ Id = 1, Documento = 1000407371, Nombre = "Vale"});
Lista_Clientes.Add(new Clientes(){ Id = 2, Documento = 1023525415, Nombre = "Fede"});
Lista_Clientes.Add(new Clientes(){ Id = 3, Documento = 42684127, Nombre = "Marta"});
Lista_Clientes.Add(new Clientes(){ Id = 4, Documento = 70844122, Nombre = "Oscar"});

var Lista_Veterinarios = new List<Veterinarios>();
Lista_Veterinarios.Add(new Veterinarios(){ Id = 1, Documento = 71722937, Nombre = "Pedro"});
Lista_Veterinarios.Add(new Veterinarios(){ Id = 2, Documento = 43604052, Nombre = "Pablo"});
Lista_Veterinarios.Add(new Veterinarios(){ Id = 3, Documento = 1011401261, Nombre = "Javier"});

var Lista_Razas = new List<Razas>();
Lista_Razas.Add(new Razas(){ Id = 1,  Nombre = "Bulldog"});
Lista_Razas.Add(new Razas(){ Id = 2,  Nombre = "Poodle"});
Lista_Razas.Add(new Razas(){ Id = 3,  Nombre = "Birmano"});
Lista_Razas.Add(new Razas(){ Id = 4,  Nombre = "Chihuahua"});

var Lista_Medicamentos = new List<Medicamentos>();
Lista_Medicamentos.Add(new Medicamentos(){ Id = 1,  Nombre = "Meloxicam"});
Lista_Medicamentos.Add(new Medicamentos(){ Id = 2,  Nombre = "Colirio"});
Lista_Medicamentos.Add(new Medicamentos(){ Id = 3,  Nombre = "Metronid"});
Lista_Medicamentos.Add(new Medicamentos(){ Id = 4,  Nombre = "Aciflux"});
Lista_Medicamentos.Add(new Medicamentos(){ Id = 5,  Nombre = "Stomorgyl"});

public class Clientes
{
    public int Id { get; set; }
    public int Documento { get; set; }
    public string? Nombre { get; set; }
      public List<Clientes>? Clientes { get; set; }
}

public class Veterinarios
{
    public int Id { get; set; }
    public int Documento { get; set; }
    public string? Nombre { get; set; }
      public List<Veterinarios>? Veterinarios { get; set; }
}

public class Razas
{
    public int Id { get; set; }
    public string? Nombre { get; set; }
      public List<Razas>? Razas { get; set; }
}

public class Medicamentos
{
    public int Id { get; set; }
    public string? Nombre { get; set; }
      public List<Medicamentos>? Medicamentos { get; set; }
}

public class Mascotas
{
    public int Id { get; set; }
    public string? Nombre { get; set; }
    public int Raza { get; set; }
      public Razas? _Raza { get; set; }
}
public class Formulas
{
    public int Id { get; set; }
    public string? Codigo { get; set; }
    public int Mascota { get; set; }
      public Mascotas? _Mascota { get; set; }
}

public class Formulas_Medicamentos
{
    public int Id { get; set; }
    public int Formula { get; set; }
    public int Medicamento{ get; set; }
    public int Cantidad { get; set; }
   public Formulas? _Formula { get; set; }
    public Medicamentos? _Medicamento{ get; set; }
   
}

public class Historiales_Clinicos
{
    public int Id { get; set; }
    public string? Codigo { get; set; }
    public int Medicamento{ get; set; }
    public DateTime Fecha { get; set; }
    public int Mascota { get; set; }
    public int Cliente{ get; set; }
    public int Formula { get; set; }
    public int Veterinario { get; set; }
    public Mascotas? _Mascota { get; set; }
    public Clientes? _Cliente { get; set; }
    public Formulas? _Formula { get; set; }
    public Veterinarios? _Veterinario { get; set; }
}
