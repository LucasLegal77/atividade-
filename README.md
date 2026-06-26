#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Definição da estrutura do Item
typedef struct {
    int id;
    char descricao[150];
    char local[50];
    char status[20]; // "Disponivel" ou "Entregue"
    int ra_retirou;
} Item;

// Funções que serão desenvolvidas ao longo do projeto
void cadastrarItem() {
    printf("\n--- CADASTRAR ITEM ACHADO ---\n");
    // Aqui vai a lógica para ler os dados e salvar no banco/arquivo
    printf("Funcionalidade em desenvolvimento...\n");
}

void listarItens() {
    printf("\n--- ITENS DISPONÍVEIS ---\n");
    // Aqui vai a lógica para buscar e mostrar os itens do banco/arquivo
    printf("Funcionalidade em desenvolvimento...\n");
}

void registrarEntrega() {
    printf("\n--- REGISTRAR ENTREGA DE ITEM ---\n");
    // Aqui vai a lógica para mudar o status do item para 'Entregue'
    printf("Funcionalidade em desenvolvimento...\n");
}

int main() {
    int opcao;

    do {
        printf("\n=================================");
        printf("\n   SISTEMA DE ACHADOS E PERDIDOS ");
        printf("\n=================================");
        printf("\n1. Cadastrar Item Achado");
        printf("\n2. Listar Itens Disponíveis");
        printf("\n3. Registrar Entrega (Baixa)");
        printf("\n0. Sair");
        printf("\nEscolha uma opcao: ");
        scanf("%d", &opcao);
        getchar(); // Limpa o buffer do teclado

        switch(opcao) {
            case 1:
                cadastrarItem();
                break;
            case 2:
                listarItens();
                break;
            case 3:
                registrarEntrega();
                break;
            case 0:
                printf("\nSaindo do sistema. Até logo!\n");
                break;
            default:
                printf("\nOpção inválida! Tente novamente.\n");
        }
    } while(opcao != 0);

    return 0;
}
