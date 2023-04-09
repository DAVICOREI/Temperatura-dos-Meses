# Temperatura-dos-Meses

import java.util.Scanner;

public class Meses {
	
    public static void main(String[] args) {
        try (Scanner input = new Scanner(System.in)) {
			double TMA[] = new double[12];
			double TMI[] = new double[12];
			String M[]= {"Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"};
			
			for (int i = 0; i < 12; i++) {
			    System.out.print("Ponha a temperatura máxima de " + M[i] + ": ");
			    TMA[i] = input.nextDouble();
			    System.out.print("Ponha a temperatura mínima de " + M[i] + ": ");
			    TMI[i] = input.nextDouble();
			}
			
			System.out.println("A maior temperatura: " + EncontrarMaior(TMA) + "º mês: " + M[indiceMaior(TMA)] + ".");
			System.out.println("A menor temperatura: " + encontrarMenor(TMI) + "º mês: " + M[indiceMenor(TMI)] + ".");
		}
    }
    public static double EncontrarMaior (double  T[]) {
        double maior = T[0];
        for (int i = 1; i < T.length; i++) {
            if (T[i] > maior) {
                maior = T[i];
            }
        }
        return maior;
    }  
    public static double encontrarMenor(double T[]) {
        double menor = T[0];
        for (int i = 1; i < T.length; i++) {
            if (T[i] < menor) {
                menor = T[i];
            }
        }
        return menor;
    }
    public static int indiceMaior(double T[]) {
        double maior = T[0];
        int indice = 0;
        for (int i = 1; i < T.length; i++) {
            if (T[i] > maior) {
                maior = T[i];
                indice = i;
            }
        }
        return indice;
    }
    public static int indiceMenor(double T[]) {
        double menor = T[0];
        int indice = 0;
        for (int i = 1; i < T.length; i++) {
            if (T[i] < menor) {
                menor = T[i];
                indice = i;
            }
        }
        return indice;
    }
}
