# Proyecto1
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
