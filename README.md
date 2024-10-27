# Calculadora-de-Partidas-Rankeadas
Calculadora de Partidas Rankeadas DIO e GFT Brasil

Instruções para entrega
 # 2️⃣ Calculadora de partidas Rankeadas
**O Que deve ser utilizado**

- Variáveis
- Operadores
- Laços de repetição
- Estruturas de decisões
- Funções

## Objetivo:

Crie uma função que recebe como parâmetro a quantidade de vitórias e derrotas de um jogador,
depois disso retorne o resultado para uma variável, o saldo de Rankeadas deve ser feito através do calculo (vitórias - derrotas)

Se vitórias for menor do que 10 = Ferro <br>
Se vitórias for entre 11 e 20 = Bronze <br>v
Se vitórias for entre 21 e 50 = Prata <br>
Se vitórias for entre 51 e 80 = Ouro <br>
Se vitórias for entre 81 e 90 = Diamante <br>
Se vitórias for entre 91 e 100= Lendário <br>
Se vitórias for maior ou igual a 101 = Imortal <br>

## Saída

Ao final deve se exibir uma mensagem:
"O Herói tem de saldo de **{saldoVitorias}** está no nível de **{nivel}**"

## Código feito em Java

```
import java.io.File;
import java.util.Scanner;
public class Main {


        // Função para calcular o nível com base nas vitórias e derrotas
        public static String calcularNivel(int vitorias, int derrotas) {
            int saldoVitorias = vitorias - derrotas;
            String nivel;

            // Estrutura de decisão para determinar o nível
            if (saldoVitorias < 10) {
                nivel = "Ferro";
            } else if (saldoVitorias >= 10 && saldoVitorias <= 20) {
                nivel = "Bronze";
            } else if (saldoVitorias >= 21 && saldoVitorias <= 50) {
                nivel = "Prata";
            } else if (saldoVitorias >= 51 && saldoVitorias <= 80) {
                nivel = "Ouro";
            } else if (saldoVitorias >= 81 && saldoVitorias <= 90) {
                nivel = "Diamante";
            } else if (saldoVitorias >= 91 && saldoVitorias <= 100) {
                nivel = "Lendário";
            } else {
                nivel = "Imortal";
            }

            // Retorna o resultado
            return "O Herói tem um saldo de " + saldoVitorias + " vitórias e está no nível de " + nivel;
        }

        public static void main(String[] args) {
            // Criação do Scanner para entrada de dados do usuário
            Scanner scanner = new Scanner(System.in);

            // Solicita o número de vitórias
            System.out.print("Digite o número de vitórias: ");
            int vitorias = scanner.nextInt();

            // Solicita o número de derrotas
            System.out.print("Digite o número de derrotas: ");
            int derrotas = scanner.nextInt();

            // Chama a função para calcular o nível e exibe o resultado
            String resultado = calcularNivel(vitorias, derrotas);
            System.out.println(resultado);

            // Fecha o scanner
            scanner.close();
        }
    }

