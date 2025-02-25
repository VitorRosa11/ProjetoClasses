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

2.
                                                         
    }
}

public class Pessoa {
    private String nome;
    private int idade;
    private double altura;

    // Construtor
    public Pessoa(String nome, int idade, double altura) {
        this.nome = nome;
        this.idade = idade;
        this.altura = altura;
    }

    // Método para andar
    public void andar() {
        System.out.println(nome + " está andando.");
    }

    // Método para falar
    public void falar(String frase) {
        System.out.println(nome + " disse: " + frase);
    }

    // Método para comer
    public void comer(String comida) {
        System.out.println(nome + " está comendo " + comida + ".");
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa pessoa1 = new Pessoa("Carlos", 25, 1.75);

        pessoa1.andar();
        pessoa1.falar("Olá, tudo bem?");
        pessoa1.comer("um hambúrguer");
    }
}

Carlos está andando.
Carlos disse: Olá, tudo bem?
Carlos está comendo um hambúrguer.

3.


public class Cachorro {
    private String raca;
    private int idade;
    private String cor;

    // Construtor
    public Cachorro(String raca, int idade, String cor) {
        this.raca = raca;
        this.idade = idade;
        this.cor = cor;
    }

    // Método para latir
    public void latir() {
        System.out.println("Au au! O cachorro está latindo.");
    }

    // Método para correr
    public void correr() {
        System.out.println("O cachorro está correndo!");
    }

    // Método para brincar
    public void brincar() {
        System.out.println("O cachorro está brincando feliz!");
    }
}

public class Main {
    public static void main(String[] args) {
        Cachorro cachorro1 = new Cachorro("Labrador", 3, "Marrom");

        cachorro1.latir();
        cachorro1.correr();
        cachorro1.brincar();
    }
}

O cachorro está latindo!
O cachorro está correndo!
O cachorro está brincando feliz!


4.


public class ContaBancaria {
    private String numeroConta;
    private double saldo;

    // Construtor
    public ContaBancaria(String numeroConta, double saldoInicial) {
        this.numeroConta = numeroConta;
        this.saldo = saldoInicial;
    }

    // Método para depositar dinheiro
    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Depósito de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Valor de depósito inválido.");
        }
    }

    // Método para sacar dinheiro
    public void sacar(double valor) {
        if (valor > 0 && valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Saldo insuficiente ou valor inválido.");
        }
    }

    // Método para verificar saldo
    public void verificarSaldo() {
        System.out.println("Saldo atual: R$" + saldo);
    }
}

public class Main {
    public static void main(String[] args) {
        ContaBancaria conta1 = new ContaBancaria("12345-6", 1000.00);

        conta1.verificarSaldo();
        conta1.depositar(500.00);
        conta1.sacar(200.00);
        conta1.verificarSaldo();
    }
}


Saldo atual: R$1000.0
Depósito de R$500.0 realizado com sucesso.
Saque de R$200.0 realizado com sucesso.
Saldo atual: R$1300.0

5.



public class Livro {
    private String titulo;
    private String autor;
    private String genero;
    private boolean aberto;
    private int paginaAtual;

    // Construtor
    public Livro(String titulo, String autor, String genero) {
        this.titulo = titulo;
        this.autor = autor;
        this.genero = genero;
        this.aberto = false;
        this.paginaAtual = 0;
    }

    // Método para abrir o livro
    public void abrir() {
        if (!aberto) {
            aberto = true;
            paginaAtual = 1;
            System.out.println("O livro \"" + titulo + "\" foi aberto na página " + paginaAtual + ".");
        } else {
            System.out.println("O livro já está aberto.");
        }
    }

    // Método para fechar o livro
    public void fechar() {
        if (aberto) {
            aberto = false;
            paginaAtual = 0;
            System.out.println("O livro \"" + titulo + "\" foi fechado.");
        } else {
            System.out.println("O livro já está fechado.");
        }
    }

    // Método para virar a página
    public void virarPagina() {
        if (aberto) {
            paginaAtual++;
            System.out.println("Virando para a página " + paginaAtual + " do livro \"" + titulo + "\".");
        } else {
            System.out.println("O livro está fechado. Abra-o antes de virar a página.");
        }
    }
}


public class Main {
    public static void main(String[] args) {
        Livro livro1 = new Livro("1984", "George Orwell", "Ficção Distópica");

        livro1.abrir();
        livro1.virarPagina();
        livro1.virarPagina();
        livro1.fechar();
        livro1.virarPagina(); // Tentando virar página com o livro fechado
    }
}


O livro "1984" foi aberto na página 1.
Virando para a página 2 do livro "1984".
Virando para a página 3 do livro "1984".
O livro "1984" foi fechado.
O livro está fechado. Abra-o antes de virar a página.




       

