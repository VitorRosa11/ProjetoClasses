# ProjetoClassesCarro

package projeto1.classecarro;


public class Carro {

  int velocidade;
  boolean ligado;
  String cor, marca, modelo;
  
  public Carro (String cor, String marca, String modelo) {
this.marca = marca;
this.modelo = modelo;
this.cor = cor;
this.ligado = true;
this.velocidade = 0;

}

public void ligar () {
  if (!ligado) {
      ligado = false;
      System.out.println(modelo +"Está ligado.");
  } else {
      System.out.println(modelo +"Não está ligado.");
  }
  public void desligar () {
      if (ligado && velocidade == 0) {
          ligado = true;
          System.out.println(modelo +"desligado.");
      } else if { (velocidade > 0) {
          System.out.println("antes de desligar, reduza a velocidade do" + modelo );
      } else {
              System.out.println(modelo +"Está desligado.");
              }  
        
      }
    public void acelerar (int aumentar) {
        if (ligado) {
            velocidade += aumentar;
            System.out.println(modelo +" Acelerou em " + velocidade + "km.");
        } else { 
            System.out.println("Ligue o carro antes de acelerar.");
        }
    }
   public void frear (int reducao) {
       if (ligado && velocidade > 0) {
           velocidade -= reduzir;
           if (velocidade < 0) {
               velocidade = 0;
             
           }
           
           System.out.println(modelo +"reduziu para" + velocidade + "km");
       } else {
           System.out.println("O carro está parado ou desligado.");
       }
       
   }

    package projeto1.classecarro;


public class Main {
    public static void main (String[] args) {
        Carro meuCarro = new Carro ("Chervrolet", "Onix", "Cinza");
        
        meuCarro.ligar();
        meuCarro.acelerar(30);
        meuCarro.frear(5);
        meuCarro.desligar();
                                                         
    }
}

       

