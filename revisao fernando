import java.util.LinkedList;
import java.util.Queue;
import java.util.Scanner;

class TrabalhoImpressao {

private int idAluno;
private String nomeArquivo;
private int numPaginas;


public TrabalhoImpressao(int idAluno, String nomeArquivo, int numPaginas) {
this.idAluno = idAluno;
 this.nomeArquivo = nomeArquivo;
 this.numPaginas = numPaginas;
    }


    @Override
    public String toString() {
 return "ID Aluno: " + idAluno + ", Arquivo: " + nomeArquivo + ", Páginas: " + numPaginas;
    }
}

class FilaImpressao {

    private Queue<TrabalhoImpressao> fila;


    public FilaImpressao() {
 this.fila = new LinkedList<>();
    }


    public void adicionarTrabalho(TrabalhoImpressao trabalho) {
        fila.add(trabalho);
        System.out.println("Trabalho adicionado: " + trabalho);
    }

    public void imprimirProximoTrabalho() {
        if (!fila.isEmpty()) {
 TrabalhoImpressao trabalho = fila.poll();
 System.out.println("Impressão iniciada: " + trabalho);
        } else {
 System.out.println("A fila está vazia! Nenhum trabalho para imprimir.");
        }
    }


    public void exibirFila() {
 if (fila.isEmpty()) {
 System.out.println("A fila está vazia.");
 } else {
 System.out.println("Trabalhos na fila:");
 for (TrabalhoImpressao trabalho : fila) {
   System.out.println(trabalho);
            }
        }
    }
}

public class SistemaImpressao {
 
    public static void simularProcessoImpressao() {
Scanner scanner = new Scanner(System.in); 
FilaImpressao filaImpressao = new FilaImpressao(); 

        while (true) {
 System.out.println("\nEscolha uma opção:");
 System.out.println("1. Adicionar trabalho à fila");
 System.out.println("2. Imprimir próximo trabalho");
   System.out.println("3. Exibir fila de impressão");
 System.out.println("4. Sair");

 System.out.print("Digite a opção desejada: ");
 String opcao = scanner.nextLine();

switch (opcao) {
 case "1":

   try {
     System.out.print("Digite o ID do aluno: ");
int idAluno = Integer.parseInt(scanner.nextLine());
 System.out.print("Digite o nome do arquivo: ");
 String nomeArquivo = scanner.nextLine();
 System.out.print("Digite o número de páginas: ");
int numPaginas = Integer.parseInt(scanner.nextLine());
                        

  TrabalhoImpressao trabalho = new TrabalhoImpressao(idAluno, nomeArquivo, numPaginas);
filaImpressao.adicionarTrabalho(trabalho);
} catch (NumberFormatException e) {
System.out.println("Erro na entrada! Tente novamente com números válidos.");
  }
 break;

  case "2":
 
filaImpressao.imprimirProximoTrabalho();
break;
case "3":

filaImpressao.exibirFila();
break;

case "4":
System.out.println("Saindo do sistema de impressão.");
scanner.close();
return;

default:
  System.out.println("Opção inválida! Escolha uma opção válida.");
 }
}
    }

    public static void main(String[] args) {
        simularProcessoImpressao();
    }
}
