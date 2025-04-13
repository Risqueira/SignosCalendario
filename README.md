# SignosCalendario
```java
package javaapplication23;

import java.util.Calendar;
import java.util.Scanner;

/**
 *
 * @author Henrique
 */
public class JavaApplication23 {

    public static void main(String[] args) {
        //Declarando Variaveis
        String nome, cor, signo, sexo;
        int anoNascimento, diaNascimento, mesNascimento, numeroSorte, idade, numCor;
        Scanner ler = new Scanner(System.in);
        Calendar hoje = Calendar.getInstance();

        //Entrada de dados das informaçãoes do usuário
        
        System.out.println("Qual seu nome?");
        nome = ler.nextLine();
        System.out.println("Digite 1 para mulher ou 2 para homem:");
        sexo = ler.nextLine();
        System.out.println("Digite o dia que nasceu:");
        diaNascimento = ler.nextInt();
        System.out.println("Digite o mês que nasceu:");
        mesNascimento = ler.nextInt();
        System.out.println("Digite o ano que nasceu:");
        anoNascimento = ler.nextInt();
        
        //verificar se o nome tem mais ou igual 8 caracteres 
        if(nome.length()>=8){
            System.out.println("Valido");
        }else{
            System.out.println("Seu nome não foi informado corretamente");
            return;
        }

        //processamento da idade para verificar se já fez aniversario ou não
        int diaAtual = hoje.get(Calendar.DATE);
        int mesAtual = hoje.get(Calendar.MONTH) + 1;
        int anoAtual = hoje.get(Calendar.YEAR);
        idade = anoAtual - anoNascimento;
        if (mesNascimento > mesAtual || (mesNascimento == mesAtual && diaNascimento > diaAtual)) {
            idade--;
        }
        
        //entrada de dados de signo
        signo="Aries";
        
        //As condições de dia/mes/ano de nascimento
       if(diaNascimento>1  && diaNascimento <=31 && 
               mesNascimento>1 && mesNascimento<=12 && 
               anoNascimento>=1900 && anoNascimento<=anoAtual){
           
           /*
           Abaixo verifica se o dia e o mês que a pessoa nasceu
           esta de acordo com o signo
           */

           //Aries
        if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 3)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 4)) {
            signo="Aries";
            //Touro
        } else if ((diaNascimento >= 21 && diaNascimento <= 30 && mesNascimento == 4)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 5)) {
            signo = "Touro";
            //Gêmeos
        } else if ((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 5)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 6)) {
            signo = "Gêmeos";
            //Câncer
        } else if ((diaNascimento >= 21 && diaNascimento <= 30 && mesNascimento == 6)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 7)) {
            signo = "Câncer";
            //Leão
        } else if ((diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 7)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 8)) {
            signo = "Leão";
            //Virgem
        } else if ((diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 8)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 9)) {
            signo = "Virgem";
            //Libra
        }else if((diaNascimento >= 23 && diaNascimento <= 30 && mesNascimento == 9)
                || (diaNascimento >= 1 && diaNascimento <= 22 && mesNascimento == 10)) {
            signo = "Libra";
            //Escorpião
        }else if((diaNascimento >= 23 && diaNascimento <= 31 && mesNascimento == 10)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 11)) {
            signo = "Escorpião";
            //Sagitário
        }else if((diaNascimento >= 22 && diaNascimento <= 30 && mesNascimento == 11)
                || (diaNascimento >= 1 && diaNascimento <= 21 && mesNascimento == 12)) {
            signo = "Sagitário";
            //Capricórnio
        }else if((diaNascimento >= 22 && diaNascimento <= 31 && mesNascimento == 12)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 1)) {
            signo = "Capricórnio";
            //Aquário
        }else if((diaNascimento >= 21 && diaNascimento <= 31 && mesNascimento == 1)
                || (diaNascimento >= 1 && diaNascimento <= 19 && mesNascimento == 2)) {
            signo = "Aquário";
            //Peixes
        }else if((diaNascimento >= 20 && diaNascimento <= 28 && mesNascimento == 2)
                || (diaNascimento >= 1 && diaNascimento <= 20 && mesNascimento == 3)) {
            signo = "Peixes";
        }
        /*
        Conectado no if de condições de nascimento. se der falso lá em cima
        não irá verificar os signos e resultará na mensagem abaixo
        */
       }else{
           System.out.println("Dia ou mes ou ano invalidos");
           return;
       }

        //Gera um número da sorte de 1 a 99
        numeroSorte = 1 + (int) (Math.random() * 99);

        //Gera uma cor da sorte de 1 a 10
        numCor = 1 + (int) (Math.random() * 10);
        
        //entrada de dados da cor
        cor="azul";

        //Condições que pode resultar na cor daquele número
        if(numCor==1){
            cor="Rosa";
        }else if(numCor==2){
            cor="Verde";
        }else if(numCor==3){
            cor="Amarelo";
        }else if(numCor==4){
            cor="Roxo";
        }else if(numCor==5){
            cor="Laranja";
        }else if(numCor==6){
            cor="Preto";
        }else if(numCor==7){
            cor="Branco";
        }else if(numCor==8){
            cor="Marrom";
        }else if(numCor==9){
            cor="Vermelho";
        }else{
            cor="Azul";
        //Saída de dados da mensagem final
        if(sexo.equals("1")){
            System.out.println("Sra." + nome + ", nascida em [" + diaNascimento + "/" + mesNascimento + "/" + anoNascimento + "], "
                        + "é do signo de " + signo + "." + " Você tem " + idade + " anos." + " Seu número da sorte é " + numeroSorte
                        + " e sua cor é " + cor + ".");
        }else{
            System.out.println("Sr." + nome + ", nascida(o) em [" + diaNascimento + "/" + mesNascimento + "/" + anoNascimento + "], "
                        + "é do signo de " + signo + "." + " Você tem " + idade + " anos." + " Seu número da sorte é " + numeroSorte
                        + " e sua cor da sorte é " + cor + ".");
        }

    }
}

```
