# Ejercicios de DIP, ISP, SRP
## Ejercicio 1 

**DIP:** se cumple o no y por que
-El codigo no cumple con el principio dip. Donde queremos que se creen lo menos posibles objectos dentro de oros sino que preferimos usar interfaces que hereden estas funciones.
**ISP:** se cumple o no y por que
-No usa interfaces. Por lo que de por si no puede cumplir el principio ISP
**SRP:** se cumple o no y por que
No. Porque por ejemplo analiador de datos cumple mas de una funcion. Como la de producir mensajes

## Ejercicio 2

```cs
class DataBaseObject
{
    public string Descripcion { get; }
}
class Interface Imesage
{
    
    public void MensajeUno()
    { /*Mensaje predeterminado*/ }
    public void MensajeDos()
    { /*Mensaje predeterminado*/ }

}

class Interface IListador
{
    public String[] ListarClaves()
    {
        //Devuelve un String[] con todas las claves
    }
    public String[] ListarDescripcionDatos()
    {
        //Devuelve un String[] con la descripción de todas los 
        //datos almacenados en  la base
    }
    public DataBaseObject[] ListarDatos()
    {
        //Devuelve un DataBaseObject[] con todos los datos almacenados en la base
    }

}

//Base de datos.
class BaseDeDatos:Listador
{
    public DataBaseObject ObtenerDato(string clave)
    {
        //Devuelve el dato correspondiente a la clave
    }
    public void GrabarDato(string clave, DataBaseObject dato)
    {
        //Graba el dato en la base de datos, bajo la clave dada
    }
}
class AnlizadorDatos:Listador,Imesage
{
    public void Analizar()
    {
        foreach (DataBaseObject DBObj in ListarDatos())
        {
            if (CumpleCondicion(DBObj))
            {
                MensajeUno();
            }
            else
            {
                MensajeDos();
            }
        }
    }
    public bool Cumplecondicion(DataBaseObject DBobj)
    {
        //Devuelve true si se cumple una cierta condición
    }
}





//Insertar el código corregido

```
## Ejercicio 3 

```cs
////Insertar el código corregido. El ejercicio 2 y 3 pueden ser resueltos de forma conjunta

    public bool Cumplecondicion(DataBaseObject DBobj)
    {
        string mensaje;
        mensaje = DBobj.Descripcion
        if (mensaje[0]="f")
        {
            return True
        }
        else
        {
            return False
        }
}

```
