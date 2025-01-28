import java.util.Scanner;

public class Main {
    public Main() {
    }

    public static int numeroSeguinte(int numero) {
        return numero + 1;
    }

    public static String juntarNome(String nome, String apelido) {
        String nomecompleto = nome.concat(apelido);
        return nomecompleto;
    }

    public static int maior(int[] numeros) {
        int Maior = numeros[0];
        int[] var2 = numeros;
        int var3 = numeros.length;

        for(int var4 = 0; var4 < var3; ++var4) {
            int num = var2[var4];
            if (num > numeros[0]) {
                Maior = num;
            }
        }

        return Maior;
    }

    public static int soma(int[] numeros) {
        int soma = 0;
        int[] var2 = numeros;
        int var3 = numeros.length;

        for(int var4 = 0; var4 < var3; ++var4) {
            int num = var2[var4];
            soma += num;
        }

        return soma;
    }

    public static double media(double[] numerosV) {
        double soma = 0.0;
        double[] var3 = numerosV;
        int var4 = numerosV.length;

        for(int var5 = 0; var5 < var4; ++var5) {
            double num = var3[var5];
            soma += num;
        }

        return soma / (double)numerosV.length;
    }

    public static void main(String[] args) {
        int numero = 6;
        numero = numeroSeguinte(numero);
        Scanner nome_completo = new Scanner(System.in);
        System.out.print("------Escreva o seu nome-------\n");
        System.out.print("Nome: ");
        String nome = nome_completo.next();
        System.out.print("Apelido: ");
        String apelido = nome_completo.next();
        String nomecompleto = juntarNome(nome, apelido);
        int[] numeros = new int[]{5, 2, 4, 3, 12};
        int soma = soma(numeros);
        double[] numeros_media = new double[]{1.6, 10.0, 5.6, 6.12};
        double media = media(numeros_media);
        int Maior = maior(numeros);
        System.out.println("\n---------Resultado-----------");
        System.out.println("Numero seguinte: " + numero);
        System.out.println("Nome completo: " + nomecompleto);
        System.out.println("O numero maior é: " + Maior);
        System.out.println("A soma dos numeros é: " + soma);
        System.out.println("A média dos numeros é: " + media);
        System.out.println("------------------------------");
    }
}
