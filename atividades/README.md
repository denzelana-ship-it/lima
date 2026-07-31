Exercícios Práticos de XML — Identificação e Correção de Erros
Este repositório contém um conjunto de exercícios focados na identificação, depuração e correção de erros de sintaxe em documentos XML (Extensible Markup Language).

🎯 Objetivo
Desenvolver e consolidar a habilidade de analisar arquivos XML, identificando violações das regras de formação de documentos (Well-Formed XML) e aplicando as correções necessárias para tornar o código válido e semântico.

🛠️ Detalhamento das Correções por Exercício
🔹 Exercício 1: Cadastro de Livro
Erros Encontrados: A tag <titulo> foi aberta, mas não foi fechada (</titulo>).

O que foi feito: Adicionada a tag de fechamento correspondente ao final do título do livro, garantindo que o elemento estivesse completo.

🔹 Exercício 2: Cadastro de Aluno
Erros Encontrados:

O valor do atributo matricula=202501 estava sem aspas.

A idade foi declarada usando atribuição direta na própria tag (<idade=20></idade>), o que é inválido no XML.

O que foi feito:

Adicionadas aspas duplas ao valor do atributo: matricula="202501".

Corrigida a estrutura da tag de idade para conter o valor entre a abertura e o fechamento do elemento: <idade>20</idade>.

🔹 Exercício 3: Empresa
Erros Encontrados:

O cabeçalho XML estava malformado (faltavam aspas em version=1.0 e o ? final).

O caractere especial & foi utilizado diretamente no texto ("Tech & Sistemas").

O que foi feito:

Corrigida a instrução de processamento do cabeçalho para <?xml version="1.0" encoding="UTF-8"?>.

Substituído o caractere reservado & por sua entidade XML correspondente: &amp;.

🔹 Exercício 4: Pedido de Venda
Erros Encontrados: Quebra na hierarquia de aninhamento (nesting). A tag <itens> foi aberta dentro de <cliente>, mas fechada fora dela.

O que foi feito: Reestruturada a árvore do documento para que <cliente> e <itens> se tornassem blocos irmãos (siblings), devidamente fechados e contidos apenas pela tag raiz <pedido>.

🔹 Exercício 5: Cadastro de Produtos
Erros Encontrados:

Nome de elemento com espaço (<nome produto>).

Nome de elemento iniciando com um número (<1preco>).

O que foi feito:

Criada uma tag pai <produto> para agrupar as informações de forma semântica.

Renomeadas as tags internas para <nome> e <preco>, removendo o caractere numérico no início da tag e o espaço.

🔹 Exercício 6: Sistema Escolar (Desafio)
Erros Encontrados:

Incompatibilidade de aspas no cabeçalho (version='1.0") e no atributo (matricula='202501").

Valor de atributo sem aspas (curso=Informática).

Caractere & sem escapamento em <nome>Lucas & Ana</nome>.

Tag de disciplina sem fechamento (<disciplina>Banco de Dados).

O que foi feito:

Padronizado o uso de aspas duplas em todos os atributos e no cabeçalho.

Adicionadas aspas ao atributo curso="Informática".

Substituído & por &amp;.

Fechada a tag do elemento com </disciplina>.