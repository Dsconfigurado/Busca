Funcionalidade: Busca

Eu, como usuário de um website de cinema,
Quero buscar filmes usando a palavra chave
Para encontrar e explorar filmes que correspondam ao meu interesse.

Contexto:
    Dado que o usuário está na página de busca de filmes
 
@alta
  Cenário: Busca de filmes com palavra-chave válida
    Quando o usuário digita uma palavra-chave válida
    Então o sistema exibe os filmes que correspondem à palavra-chave

@alta
  Cenário: Busca de filmes sem resultados
    Quando o usuário digita uma palavra-chave que não corresponde a nenhum filme
    Então o sistema informa que não há filmes correspondentes

@alta
  Cenário: Limpar a busca de filmes
    Dado que o usuário realizou uma busca
    Quando o usuário clica no botão "Limpar Busca"
    Então a lista de filmes é resetada para o estado inicial

        Exemplos:
            | Filmes       | Buscas        | Palavra-chave                  |
            | A Lagoa Azul | 10 Resultados | válida                         |
            | 3 Dentes     | 0 Resultados  | não corresponde a nenhum filme |
            | 001652       | 0 Resultados  | não corresponde a nenhum filme |
            | DeadPool     | 15 Resultados | válida                         |
            | Armagedon    | 8 Resultados  | válida                         |
