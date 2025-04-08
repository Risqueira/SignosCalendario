# SignosCalendario
```java
package signos;

import java.util.Calendar;
import java.util.Scanner;

/**
 *
 * @author Henrique Michel Rodrigues
 */
public class Signos {

    public static void main(String[] args) {

        //Declarando Variaveis
        String nome, cor, signo;
        int anoNascimento, diaNascimento, mesNascimento, numeroSorte, idade, numCor, sexo;
        Scanner ler = new Scanner(System.in);
        Calendar hoje = Calendar.getInstance();

        //Entrada de dados
        System.out.println("Qual seu nome?");
        nome = ler.nextLine();
        System.out.println("Digite 1 para mulher ou 2 para homem ou 3 para outros");
        sexo = ler.nextInt();
        System.out.println("Digite o dia que nasceu:");
        diaNascimento = ler.nextInt();
        System.out.println("Digite o mês que nasceu:");
        mesNascimento = ler.nextInt();
        System.out.println("Digite o ano que nasceu:");
        anoNascimento = ler.nextInt();

        //processamento da idade
        int diaAtual = hoje.get(Calendar.DATE);
        int mesAtual = hoje.get(Calendar.MONTH) + 1;
        int anoAtual = hoje.get(Calendar.YEAR);
        idade = anoAtual - anoNascimento;
        if (mesNascimento > mesAtual || (mesNascimento == mesAtual && diaNascimento > diaAtual)) {
            idade--;
        }

        /*Processamento de Dia/Mes
        if (mesNascimento == 1 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
        if (mesNascimento == 2 && diaNascimento >= 1 && diaNascimento <= 28) {

            return;
        }
        if (mesNascimento == 3 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
        if (mesNascimento == 4 && diaNascimento >= 1 && diaNascimento <= 30) {

            return;
        }
        if (mesNascimento == 5 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
        if (mesNascimento == 6 && diaNascimento >= 1 && diaNascimento <= 30) {

            return;
        }
        if (mesNascimento == 7 && diaNascimento >= 1 && diaNascimento <= 31) {
            
            return;
        }
        if (mesNascimento == 8 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
        if (mesNascimento == 9 && diaNascimento >= 1 && diaNascimento <= 30) {

            return;
        }
        if (mesNascimento == 10 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
        if (mesNascimento == 11 && diaNascimento >= 1 && diaNascimento <= 30) {

            return;
        }
        if (mesNascimento == 12 && diaNascimento >= 1 && diaNascimento <= 31) {

            return;
        }
*/
        //Declarar a string signo vazia
        signo="Aries";
        //Aries
       if(diaNascimento>0  && diaNascimento <=31 && 
               mesNascimento>0 && mesNascimento<=12 && 
               anoNascimento>=1900 && anoNascimento<=anoAtual){
        if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 3)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesAtual == 4)) {
            
            //Touro
        } else if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 4)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 5)) {
            signo = "Touro";
            //Gêmeos
        } else if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 5)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 6)) {
            signo = "Gêmeos";
        } else if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 6)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 7)) {
            signo = "Câncer";
        } else if ((diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 7)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 8)) {
            signo = "Leâo";
        } else if ((diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 8)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 9)) {
            signo = "Virgem";
        }else if((diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 9)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 10)) {
            signo = "Libra";
        }else if((diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 10)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 11)) {
            signo = "Escorpião";
        }else if((diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 11)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 12)) {
            signo = "Sagitário";          
        }else if((diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 12)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 1)) {
            signo = "Capricórnio";
        }else if((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 1)
                || (diaNascimento >= 1 && diaNascimento <= 19 && mesNascimento == 2)) {
            signo = "Aquário";
        }else if((diaNascimento >= 20 && diaNascimento <= 31 && mesNascimento == 2)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 3)) {
            signo = "Peixes";
        }
       }else{
           System.out.println("Dia ou mes ou ano invalidos");
       }

        //Gera um número da sorte de 1 a 100
        numeroSorte = 1 + (int) (Math.random() * 100);

        //Gera uma cor da sorte de 1 a 10
        numCor = 1 + (int) Math.random() * 10;

        cor = "azul";

        switch (numCor) {
            case 1:
                break;
            case 2:
                cor = "Vermelho";
                break;
            case 3:
                cor = "Verde";
                break;
            case 4:
                cor = "Amarelo";
                break;
            case 5:
                cor = "Roxo";
                break;
            case 6:
                cor = "Laranja";
                break;
            case 7:
                cor = "Índigo";
                break;
            case 8:
                cor = "Preto";
                break;
            case 9:
                cor = "Branco";
                break;
            case 10:
                cor = "Cinza";
                break;
        }

        switch (sexo) {
            case 1:
                System.out.println("Sra." + nome + ", nascida em [" + diaNascimento + "/" + mesNascimento + "/" + anoNascimento + "], "
                        + "é do signo de " + signo + "." + " Você tem " + idade + " anos." + " Seu número da sorte é " + numeroSorte
                        + "e sua cor é " + cor + ".");
                break;
            case 2:
                System.out.println("Sr." + nome + ", nascida em [" + diaNascimento + "/" + mesNascimento + "/" + anoNascimento + "], "
                        + "é do signo de " + signo + "." + " Você tem " + idade + " anos." + " Seu número da sorte é " + numeroSorte
                        + "e sua cor é " + cor + ".");
                break;
            default:
                System.out.println("Sra ou Sr." + nome + ", nascida em [" + diaNascimento + "/" + mesNascimento + "/" + anoNascimento + "], "
                        + "é do signo de " + signo + "." + " Você tem " + idade + " anos." + " Seu número da sorte é " + numeroSorte
                        + "e sua cor é " + cor + ".");
                break;
        }
    }
}
```
