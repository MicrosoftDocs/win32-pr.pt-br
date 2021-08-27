---
description: As SQL de consulta para Windows Instalador são restritas aos formatos a seguir.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintaxe SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6512f52ae687ee3f95a00f104c7cdfa251c878b649809faeb86c73bdcf82bf84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624670"
---
# <a name="sql-syntax"></a>Sintaxe SQL

As SQL de consulta para Windows Instalador são restritas aos formatos a seguir.



| Ação                             | Consulta                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selecionar um grupo de registros          | SELECT \[ DISTINCT \] {column-list} FROM {table-list} \[ WHERE {operation-list} \] \[ ORDER BY {column-list}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Excluir registros de uma tabela        | DELETE FROM {table} \[ WHERE {operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificar registros existentes em uma tabela | UPDATE {table-list} SET {column}= {constant} \[ , {column}= {constant} \] \[ , ... \] \[ AS consultas WHERE {operation-list} \] UPDATE só funcionam em colunas de chave não exclusivas.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Adicionar registros a uma tabela             | INSERT INTO {table} ({column-list}) VALUES ({constant-list}) Dados binários TEMPORÁRIOs não podem ser inseridos em uma tabela diretamente usando as consultas \[ INSERT INTO ou UPDATE \] SQL. Para obter mais informações, consulte [Adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Adicionar uma tabela                        | CREATE TABLE {table} ( {column} {column type}) Os tipos de coluna HOLD devem ser especificados para cada coluna ao \[ \] adicionar uma tabela. Pelo menos uma coluna de chave primária deve ser especificada para a criação de uma nova tabela. As substituições possíveis para {tipo de coluna} no acima são: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT \| INT INTEGER LONG OBJECT \| NOT NULL TEMPORARY \| \| \[ \] \[ \] \[ LOCALIZABLE , \] \[ column... , \] \[ ... \] COLUNA PRIMARY KEY \[ , coluna , ... \] \[ \] .<br/> |
| Remover uma tabela                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Adicionar uma coluna                       | ALTER TABLE {table} ADD {column} {column type}O tipo de coluna deve ser especificado ao adicionar uma coluna. As substituições possíveis para {tipo de coluna} no acima são: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT \| INT INTEGER LONG OBJECT \| NOT NULL TEMPORARY \| \| \[ \] \[ \] \[ LOCALIZABLE HOLD \] \[ \] .<br/>                                                                                                                                                                  |
| Manter e liberar tabelas temporárias     | ALTER TABLE {table name} HOLDALTER TABLE {table name} FREE<br/> O usuário pode usar os comandos HOLD e FREE para controlar o período de vida de uma tabela temporária ou uma coluna temporária. A contagem de espera em uma tabela é incrementada para cada SQL HOLD nessa tabela e decrementada para cada SQL DE LIBERAÇÃO na tabela. Quando a última contagem de espera é liberada em uma tabela, todas as colunas temporárias ficam inacessíveis. Se todas as colunas são temporárias, a tabela se torna inacessível.<br/>     |



 

Para obter mais informações, consulte [Exemplos de consultas de banco de dados usando SQL script e](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Gramática SQL

Os parâmetros opcionais são mostrados entre colchetes \[ \] . Quando várias opções são listadas, os parâmetros opcionais são separados por uma barra vertical.

Um {constant} é uma cadeia de caracteres ou um inteiro. Uma cadeia de caracteres deve ser entre aspas simples 'example'. Uma {constant-list} é uma lista delimitada por vírgulas de uma ou mais constantes.

A opção LOCALIZABLE define um atributo de coluna que indica que a coluna precisa ser localizada.

Um {column} é uma referência colunar a um valor em um campo de uma tabela.

Um {marker} é uma referência de parâmetro a um valor fornecido por um registro enviado com a consulta. Ele é representado na instrução SQL por um ponto de interrogação ?. Para obter informações sobre o uso de parâmetros, consulte a [**função MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) ou o [**método Execute.**](view-execute.md)

A Windows do SQL não dá suporte ao escape de aspas simples (valor ASCII 39) em um literal de cadeia de caracteres. No entanto, você pode buscar ou criar o registro, definir o campo com a propriedade [**StringData**](record-stringdata.md) ou [**IntegerData**](record-integerdata.md) e, em seguida, chamar o [**método Modify.**](view-modify.md) Como alternativa, você pode criar um registro e usar os marcadores de parâmetro (?) descritos em [**Método Execute.**](view-execute.md) Você também pode fazer isso usando as funções de banco de dados [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)e [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Uma cláusula WHERE {operation-list} é opcional e é um grupo de operações a serem usadas para filtrar a seleção. As operações devem ser dos seguintes tipos:

-   {column} = {column}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constant}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marker}
-   {column} é nulo
-   {column} não é nulo

Para valores de cadeia de caracteres, somente as operações = ou <> são possíveis. As comparações de valor do objeto são limitadas a IS NULL e IS NOT NULL.

Operações individuais podem ser agrupadas por operadores AND ou OR. A ordenação pode ser imposta pelo uso de parênteses ( ).

A cláusula ORDER BY é opcional e causa um atraso inicial durante a classificação. A ordenação por cadeias de caracteres agrupará cadeias de caracteres idênticas, mas não fará a ordem alfabética das cadeias de caracteres.

A cláusula DISTINCT é opcional e não repete registros idênticos no conjunto de resultados retornado.

Um {table-list} é uma lista delimitada por vírgulas de um ou mais nomes de tabela chamados {table} na junção.

Uma {column-list} é uma lista delimitada por vírgulas de uma ou mais colunas de tabela conhecidas como {column} selecionadas. Colunas ambíguas podem ser ainda mais qualificadas como {tablename.column}. Um asterisco pode ser usado como uma lista de colunas em uma consulta SELECT para representar todas as colunas nas tabelas referenciadas. Ao referenciar campos por posição de coluna, selecione as colunas por nome em vez de usar o asterisco. Um asterisco não pode ser usado como uma lista de colunas em uma consulta INSERT INTO.

Para escapar nomes de tabela e nomes de coluna que se SQL palavras-chave, coloque o nome entre duas marcas de acento grave \` \` (valor ASCII 96). Se um nome de coluna tiver que ser escapado e for qualificado como {tablename.column}, a tabela e a coluna deverão ser escapadas individualmente como { \` tablename \` . \` column \` }. É recomendável que todos os nomes de tabela e nomes de coluna sejam escapados dessa maneira para evitar conflitos com palavras reservadas e obter um desempenho significativo.

Os nomes de tabela são limitados a 31 caracteres. Para obter mais informações, consulte [Nomes de tabela.](table-names.md) Os nomes de tabela e coluna são sensíveis a minúsculas. SQL palavras-chave não são sensíveis a minúsculas.

O número máximo de expressões em uma cláusula WHERE de uma SQL consulta é limitado a 32.

Somente junções internas têm suporte e são especificadas por uma comparação de colunas de tabelas diferentes. Não há suporte para junções circulares. Uma junção circular é SQL consulta que vincula três ou mais tabelas em um circuito. Por exemplo, o seguinte é uma junção circular:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

As colunas que fazem parte das chaves primárias de uma tabela devem ser definidas primeiro em ordem de prioridade, seguidas por qualquer coluna de chave não primária. Colunas persistentes devem ser definidas antes de colunas temporárias. A sequência de classificação de uma coluna de texto é indefinida; No entanto, valores de texto idênticos sempre se agrupam.

Observe que, ao adicionar ou criar uma coluna, você deve especificar o tipo de coluna.

As tabelas podem não conter mais de uma coluna do tipo 'object'.

O tamanho máximo que pode ser especificado explicitamente para uma coluna de cadeia de caracteres em uma SQL consulta é 255. Uma coluna de cadeia de caracteres de comprimento infinito é representada como tendo tamanho 0. Para obter mais informações, consulte [Formato de definição de coluna](column-definition-format.md).

Para executar qualquer instrução SQL, uma exibição deve ser criada. No entanto, uma exibição que não cria um conjunto de resultados, como CREATE TABLE ou INSERT INTO, [](view-modify.md) não pode ser usada com [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou o método Modify para atualizar tabelas por meio da exibição.

Observe que você não pode buscar um registro que contém dados binários de um banco de dados e, em seguida, usar esse registro para inserir os dados em um banco de dados completamente diferente. Para mover dados binários de um banco de dados para outro, você deve exportar os dados para um arquivo e importá-los para o novo banco de dados por meio de uma consulta e a [**função MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) Isso garante que cada banco de dados tenha sua própria cópia dos dados binários.

 

 




