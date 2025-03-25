# SignosCalendario
```java
package signostrabalho;

import java.util.Calendar;
import java.util.Scanner;

/**
 * Descrição do Trabalho: Você foi contratado para desenvolver um sistema para a
 * empresa chamada &quot;Sei de Tudo&quot;, que oferece consultoria de Zodíaco.
 * Seu programa deve solicitar as seguintes informações do usuário: nome, sexo,
 * dia, mês e ano de nascimento. Com base nesses dados, o programa calculará a
 * idade do usuário, identificará o signo correspondente e apresentará
 * informações personalizadas, como o número da sorte e a cor da sorte.
 *
 * @author Henrique
 */
public class SignosTrabalho {

    public static void main(String[] args) {

        //Declarando Variaveis
        String nome, cor, sexo, signo;
        int anoNascimento, diaNascimento, mesNascimento, numeroSorte, idade;
        Scanner ler = new Scanner(System.in);
        Calendar hoje = Calendar.getInstance();

        //Entrada de dados
        System.out.println("Qual seu nome?");
        nome = ler.nextLine();
        System.out.println("Digite 1 para mulher ou 2 para homem");
        sexo = ler.nextLine();
        System.out.println("Digite o dia que nasceu:");
        diaNascimento = ler.nextInt();
        System.out.println("Digite o mês que nasceu:");
        mesNascimento = ler.nextInt();
        System.out.println("Digite o ano que nasceu:");
        anoNascimento = ler.nextInt();

        //Processamento para qual sexo
        switch (sexo) {
            case "1":
                break;
            case "2":
                break;
            default:
                System.out.println("INVALIDO");
                ;
                break;
        }

        //processamento da idade
        int diaAtual = hoje.get(Calendar.DATE);
        int mesAtual = hoje.get(Calendar.MONTH) + 1;
        int anoAtual = hoje.get(Calendar.YEAR);
        idade = anoAtual - anoNascimento;
        if (mesNascimento > mesAtual || (mesNascimento == mesAtual && diaNascimento > diaAtual)) {
            idade--;
        }

        //Processamento de Dia/Mes/Ano
        if (mesNascimento == 1 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 2 && diaNascimento >= 1 && diaNascimento <= 28) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 3 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 4 && diaNascimento >= 1 && diaNascimento <= 30) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 5 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 6 && diaNascimento >= 1 && diaNascimento <= 30) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 7 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 8 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 9 && diaNascimento >= 1 && diaNascimento <= 30) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 10 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 11 && diaNascimento >= 1 && diaNascimento <= 30) {

        } else {
            System.out.println("INVALIDO");
            return;
        }
        if (mesNascimento == 12 && diaNascimento >= 1 && diaNascimento <= 31) {

        } else {
            System.out.println("INVALIDO");
            return;
        }

        //Aries
        if (diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 3) {

        } else if (diaNascimento >= 1 && diaNascimento <= 20 && mesAtual == 4) {

        }
        //Touro
        if (diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 4) {

        } else if (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 5) {

        }
        //Gêmeos
        if (diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 5) {

        } else if (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 6) {

        }
        //Câncer
        if (diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 6) {

        } else if (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 7) {

        }
        //Leão
        if (diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 7) {

        } else if (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 8) {

        }
        //Virgem
        if (diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 8) {

        } else if (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 9) {

        }
        //Libra 
        if (diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 9) {

        } else if (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 10) {

        }
        //Escorpião
        if (diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 10) {

        } else if (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 11) {

        }
        //Sagitário
        if (diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 11) {

        } else if (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 12) {

        }
        //Capricórnio
        if (diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 12) {

        } else if (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 1) {

        }
        //Aquário
        if (diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 1) {

        } else if (diaNascimento >= 1 && diaNascimento <= 19 && mesNascimento == 2) {

        }
        //Peixes
        if (diaNascimento >= 20 && diaNascimento <= 31 && mesNascimento == 2) {

        } else if (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 3) {

        }

    }
}

```
