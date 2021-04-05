---
description: As cadeias de caracteres de consulta SQL para Windows Installer são restritas aos formatos a seguir.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintaxe SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827938"
---
# <a name="sql-syntax"></a>Sintaxe SQL

As cadeias de caracteres de consulta SQL para Windows Installer são restritas aos formatos a seguir.



| Ação                             | Consulta                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selecionar um grupo de registros          | Selecione \[ uma \] {Column-List} distinta em {Table-List} \[ , em que {Operation-List} \] \[ ordenar por {Column-List}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Excluir registros de uma tabela        | EXCLUIR de {Table} \[ em que {Operation-List}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificar registros existentes em uma tabela | ATUALIZAR {Table-List} SET {coluna} = {constante} \[ , {coluna} = {constante} \] \[ ,... \] \[ ONDE {Operation-List} as \] consultas de atualização funcionam somente em colunas de chave não primárias.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Adicionar registros a uma tabela             | INSERIR em {Table} ({Column-List}) valores \[ \] binários temporários não podem ser inseridos em uma tabela diretamente usando as consultas de inserção ou atualização de SQL. Para obter mais informações, consulte [adicionando dados binários a uma tabela usando o SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Adicionar uma tabela                        | CREATE TABLE {table} ({coluna} {tipo de coluna}) os \[ \] tipos de coluna de retenção devem ser especificados para cada coluna ao adicionar uma tabela. Pelo menos uma coluna de chave primária deve ser especificada para a criação de uma nova tabela. As substituições possíveis para {column Type} nos itens acima são: CHAR \[ ({Size}) \] \| caractere \[ ({Size}) \] \| LONGCHAR \| \| Long int \| inteiro \| \| objeto longo \[ não nulo \] \[ temporário \] \[ localizável \] \[ , coluna... \] \[ ,. \] .. Coluna de chave primária \[ , coluna \] \[ ,... \]<br/> |
| Remover uma tabela                     | REMOVER tabela {Table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Adicionar uma coluna                       | ALTER TABLE {tabela} adicionar {Column} {tipo de coluna} o tipo de coluna deve ser especificado ao adicionar uma coluna. As substituições possíveis para {column Type} nos itens acima são: CHAR \[ ({Size}) \] \| caractere \[ ({Size}) \] \| LONGCHAR \| \| Long int \| inteiro o objeto de \| longo prazo \| não nulo de uma \[ \] \[ \] \[ suspensão localizável temporário \] \[ \] .<br/>                                                                                                                                                                  |
| Suspender e liberar tabelas temporárias     | ALTER TABLE {nome da tabela} tabela HOLDALTER {nome da tabela} gratuito<br/> O usuário pode usar os comandos HOLD e FREE para controlar o período de vida de uma tabela temporária ou uma coluna temporária. A contagem de espera em uma tabela é incrementada para cada operação de suspensão do SQL nessa tabela e decrementada para cada operação do SQL livre na tabela. Quando a última contagem de isenções é liberada em uma tabela, todas as colunas temporárias se tornam inacessíveis. Se todas as colunas forem temporárias, a tabela se tornará inacessível.<br/>     |



 

Para obter mais informações, consulte [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Gramática SQL

Os parâmetros opcionais são mostrados entre colchetes \[ \] . Quando várias opções são listadas, os parâmetros opcionais são separados por uma barra vertical.

Uma {Constant} é uma cadeia de caracteres ou um inteiro. Uma cadeia de caracteres deve ser colocada entre aspas simples ' example '. Uma {Constant-list} é uma lista delimitada por vírgula de uma ou mais constantes.

A opção LOCALIZÁvel define um atributo Column que indica que a coluna precisa ser localizada.

Uma {Column} é uma referência de coluna para um valor em um campo de uma tabela.

Um {Marker} é uma referência de parâmetro para um valor fornecido por um registro enviado com a consulta. Ele é representado na instrução SQL por um ponto de interrogação?. Para obter informações sobre o uso de parâmetros, consulte a função [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) ou o método [**Execute**](view-execute.md) .

A sintaxe do Windows Installer SQL não dá suporte à saída de aspas simples (valor ASCII 39) em um literal de cadeia de caracteres. No entanto, você pode buscar ou criar o registro, definir o campo com a propriedade [**StringData**](record-stringdata.md) ou [**IntegerData**](record-integerdata.md) e, em seguida, chamar o método [**Modify**](view-modify.md) . Como alternativa, você pode criar um registro e usar os marcadores de parâmetro (?) descritos no método [**Execute**](view-execute.md) . Você também pode fazer isso usando as funções de banco de dados [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)e [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Uma cláusula WHERE {Operation-list} é opcional e é um agrupamento de operações a serem usadas para filtrar a seleção. As operações devem ser dos seguintes tipos:

-   {Column} = {coluna}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constante}
-   {coluna} = \|  <>  \|  >  \|  <  \|  >=  \| <= {Marker}
-   {Column} é nulo
-   {Column} não é nulo

Para valores de cadeia de caracteres, somente as operações = ou <> são possíveis. As comparações de valor de objeto são limitadas a são nulas e não são nulas.

Operações individuais podem ser agrupadas por operadores AND ou OR. A ordenação pode ser imposta pelo uso de parênteses ().

A cláusula ORDER BY é opcional e causa um atraso inicial durante a classificação. Ordenar por cadeias de caracteres agrupará cadeias de caracteres idênticas, mas não colocará em ordem alfabética as cadeias de caracteres

A cláusula DISTINCT é opcional e não repete registros idênticos no conjunto de resultados retornado.

Uma {Table-list} é uma lista delimitada por vírgulas de um ou mais nomes de tabela referenciados como {Table} na junção.

Uma {Column-list} é uma lista delimitada por vírgulas de uma ou mais colunas de tabela referenciadas como {Column} selecionadas. Colunas ambíguas podem ser mais qualificadas como {TableName. Column}. Um asterisco pode ser usado como uma lista de colunas em uma consulta SELECT para representar todas as colunas nas tabelas referenciadas. Ao fazer referência a campos por posição de coluna, selecione as colunas por nome em vez de usar o asterisco. Um asterisco não pode ser usado como uma lista de colunas em uma consulta INSERT INTO.

Para escapar nomes de tabela e nomes de coluna que conflitam com palavras-chave SQL, coloque o nome entre duas marcas de acento grave \` \` (valor ASCII 96). Se um nome de coluna deve ter escape e é qualificado como {TableName. Column}, a tabela e a coluna devem ter um escape individual como { \` TableName \` . \` coluna \` }. É recomendável que todos os nomes de tabela e nomes de coluna sejam ignorados dessa maneira para evitar conflitos com palavras reservadas e obter um desempenho significativo.

Os nomes de tabela são limitados a 31 caracteres. Para obter mais informações, consulte [nomes de tabela](table-names.md). Os nomes de tabela e coluna diferenciam maiúsculas de minúsculas. As palavras-chave SQL não diferenciam maiúsculas de minúsculas.

O número máximo de expressões em uma cláusula WHERE de uma consulta SQL é limitado a 32.

Somente junções internas têm suporte e são especificadas por uma comparação de colunas de tabelas diferentes. Não há suporte para junções circulares. Uma junção circular é uma consulta SQL que vincula três ou mais tabelas em um circuito. Por exemplo, a seguir está uma junção circular:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

As colunas que fazem parte das chaves primárias de uma tabela devem ser definidas primeiro em ordem de prioridade, seguidas por colunas de chave não primárias. As colunas persistentes devem ser definidas antes das colunas temporárias. A sequência de classificação de uma coluna de texto é indefinida; no entanto, valores de texto idênticos sempre são agrupados juntos.

Observe que, ao adicionar ou criar uma coluna, você deve especificar o tipo de coluna.

Tabelas não podem conter mais de uma coluna do tipo ' Object '.

O tamanho máximo que pode ser especificado explicitamente para uma coluna de cadeia de caracteres em uma consulta SQL é 255. Uma coluna de cadeia de caracteres de comprimento infinito é representada como tendo o tamanho 0. Para obter mais informações, consulte [formato de definição de coluna](column-definition-format.md).

Para executar qualquer instrução SQL, é necessário criar uma exibição. No entanto, uma exibição que não cria um conjunto de resultados, como CREATE TABLE ou INSERT INTO, não pode ser usada com [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou o método [**Modify**](view-modify.md) para atualizar tabelas por meio da exibição.

Observe que você não pode buscar um registro que contém dados binários de um banco e, em seguida, usar esse registro para inserir os dados em um banco de dado completamente diferente. Você deve exportar os dados para um arquivo e, em seguida, importá-los para o novo banco de dados por meio de uma consulta e a função [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) . Isso garante que cada banco de dados tenha sua própria cópia dos dados binários.

 

 




