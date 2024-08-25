# Guilda de Heróis

Este projeto, desenvolvido em grupo, implementa um sistema de gerenciamento de uma guilda de heróis. A aplicação permite a visualização, busca e ordenação de membros da guilda, além da leitura e gravação de dados em arquivos CSV e DAT.

## Membros da Equipe

- **Alexandre de Castro Nunes Borges Filho**
- **Ana Clara Moreira Viana**
- **Maycon Henrique Soares de Sousa**

## Funcionalidades

- **Visualização de Membros**: Exibe detalhes sobre os membros da guilda, como ID, nome, rank, sucesso e atividade.
- **Busca Binária**: Implementada para busca por nome e ID de membros.
- **Ordenação**: Utiliza o algoritmo QuickSort para ordenar os membros da guilda por ID ou nome.
- **Leitura de Arquivos**: Suporta leitura de dados da guilda a partir de arquivos CSV e DAT.
- **Gravação de Arquivos**: Permite salvar os dados da guilda em arquivos CSV ou DAT.

## Estrutura de Dados

### `guildMember`
A estrutura `guildMember` armazena as informações de cada membro da guilda:
- `int id`: ID único do membro.
- `string name`: Nome do membro.
- `char rank`: Rank do membro.
- `float success`: Taxa de sucesso do membro.
- `bool active`: Indica se o membro está ativo na guilda.

## Funções Principais

### `void printFile()`
Exibe uma arte ASCII do nome do sistema.

### `void displaySection(int memberCount, guildMember *memberList, int begin, int end)`
Exibe uma seção específica dos membros da guilda.

### `int binarySearchByName(guildMember *arr, int size, string name)`
Realiza uma busca binária por nome.

### `int binarySearchById(guildMember *arr, int size, int id)`
Realiza uma busca binária por ID.

### `void quicksortInt(guildMember *vetor, int low, int high)`
Ordena os membros por ID usando o algoritmo QuickSort.

### `void quicksortString(guildMember *vetor, int low, int high)`
Ordena os membros por nome usando o algoritmo QuickSort.

### `guildMember* csvGet(string name, int &memberCount)`
Lê os dados dos membros a partir de um arquivo CSV.

### `guildMember* datGet(string name, int &memberCount)`
Lê os dados dos membros a partir de um arquivo DAT.

### `void saveDat(guildMember *memberList, int memberCount, string nome)`
Salva os dados dos membros em um arquivo DAT.

### `void saveCSV(guildMember *memberList, int memberCount, string fileName)`
Salva os dados dos membros em um arquivo CSV.

## Como Executar

1. **Compilar**: Compile o código utilizando um compilador C++.
2. **Executar**: Execute o programa a partir da linha de comando. Você será solicitado a fornecer o nome do arquivo com os dados da guilda (extensões suportadas: `.csv` e `.dat`).
3. **Interagir**: Siga as instruções na tela para visualizar, buscar, ordenar ou salvar dados.

## Requisitos

- Compilador C++ compatível com C++11 ou superior.

## Observações

- As funções de busca e ordenação funcionam corretamente apenas quando a lista de membros está ordenada.
- O projeto está configurado para trabalhar com um diretório específico (`./guildList/`) para a leitura e gravação de arquivos.

## Licença

Este projeto é licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais informações.
