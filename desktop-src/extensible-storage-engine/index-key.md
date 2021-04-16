---
description: 'Saiba mais sobre: chave de índice'
title: Chave de índice
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563757"
---
# <a name="index-key"></a>Chave de índice


_**Aplica-se a:** Windows | Windows Server_

## <a name="index-key"></a>Chave de índice

Um índice é criado sobre os dados na tabela com [JetCreateIndex](./jetcreateindex-function.md) ou vários índices podem ser criados simultaneamente com [JetCreateIndex2](./jetcreateindex2-function.md) usando a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) . O índice é definido em termos de uma matriz de colunas, em ordem de precedência. Essa matriz de colunas também é chamada de chave de índice. A chave de índice pode ser definida como o índice primário quando a opção JET_bitIndexPrimary é definida no parâmetro *grbit* de [JetCreateIndex](./jetcreateindex-function.md) ou [JET_INDEXCREATE](./jet-indexcreate-structure.md). A chave de índice é uma cadeia de caracteres terminada em NULL de tokens terminados em nulo, conforme mostrado no exemplo a seguir:

\+Col1 \\ 0-Col2 \\ 0 + Col3 \\ 0 \\ 0

A chave no exemplo pode ser usada para criar um índice em três colunas na tabela. Cada coluna especificada no índice é chamada de "segmento de índice" ou "coluna de chave". O segmento de índice pode ser crescente ou decrescente em termos de sua contribuição de ordenação. No exemplo acima, o nome da primeira coluna no índice é col1. O + indica que Col1 é indexado em ordem crescente. O – Before Col2 indica que ele está indexado em ordem decrescente.

Quando as colunas condicionais estão presentes no índice, a estrutura de [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) é usada para indicar como elas são indexadas. Uma coluna condicional pode ser usada para controlar a presença ou a ausência de uma entrada de índice em um índice com base no valor na coluna condicional correspondente sem afetar a ordem de classificação do índice. Uma coluna condicional pode incluir ou excluir uma entrada de índice do índice se o valor dessa coluna condicional for nulo para o registro correspondente.

Por padrão, o tamanho máximo da chave de índice é fornecido pela constante JET_cbKeyMost que sempre foi de 255 bytes de dados normalizados (bytes de dados, incluindo a sobrecarga de indexação). A partir do Windows Vista, o tamanho máximo da chave de índice pode ser definido com a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) . O tamanho máximo da chave de índice corresponde ao tamanho da página do banco de dados. Para habilitar um tamanho de chave máximo personalizado, especifique a opção Jet_bitIndexKeyMost no membro grbits de [JET_INDEXCREATE](./jet-indexcreate-structure.md)e defina o membro **cbKeyMost** como um dos seguintes valores:

  - JET_cbKeyMost2KBytePage: quando o tamanho da página do banco de dados é 2048 bytes, o tamanho máximo da chave de índice pode ter entre 255 bytes no mínimo e o máximo de 500 bytes.

  - JET_cbKeyMost4KBytePage: quando o tamanho da página do banco de dados é 4096 bytes, o tamanho máximo da chave de índice pode ter entre 255 bytes no mínimo e o máximo de 1000 bytes.

  - JET_cbKeyMost8KBytePage: quando o tamanho da página do banco de dados é 8196 bytes, o tamanho máximo da chave de índice pode ter entre 255 bytes no mínimo e o máximo de 2000 bytes.

O exemplo no diagrama a seguir mostra uma tabela que contém informações de funcionários. A tabela tem 6 colunas, cada uma definindo um atributo de funcionário específico. Um registro na tabela contém valores para um funcionário, como o nome do funcionário na coluna 1 e a ID do funcionário na coluna 2. Um índice primário criado para esta tabela organiza os dados de acordo com o nome do funcionário primeiro e a ID do funcionário em segundo lugar. O nome e a ID são indexados em ordem crescente. Por exemplo, um registro que contém o nome Johnson e a ID de funcionário 12345 será listado antes de um registro com um nome de funcionário Jones e uma ID de 10000. Todos os registros de Jones são armazenados juntos na tabela, com suas IDs de funcionário em ordem crescente, conforme mostrado na tabela.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

A chave no índice primário deve ser exclusiva, mas as chaves no índice secundário podem ser duplicatas. Por exemplo, se um índice for criado com base no sobrenome e houver duas pessoas com Stevens no banco de dados, o ESE retornará um erro de Jet_errKeyDuplicate de [JetUpdate](./jetupdate-function.md) ou [JetUpdate2](./jetupdate2-function.md), quando o aplicativo tentar inserir o segundo "Stevens". Quando a chave real é maior que o tamanho máximo da chave, a chave é truncada. Pesquisa e exclusividade de efeitos de truncamento de chave e devem ser gerenciados pelo aplicativo. Por exemplo, se "Stevens" e "Stevenson" foram armazenados em um índice por sobrenome e o tamanho máximo da chave era muito pequeno para armazenar a parte "on" de "Stevenson", o truncamento de chave resultaria no mecanismo de banco de dados declarando que "Stevens" e "Stevenson" são duplicatas, mesmo que não sejam. O aplicativo deve estar preparado para manipular casos como esse durante a pesquisa e a atualização se a definição de índice e os valores de coluna indexados por ele são de tal forma que o truncamento de chave é uma possibilidade. A partir do Windows Vista, os aplicativos podem especificar a opção Jet_bitIndexDisallowTruncation em [JET_INDEXCREATE](./jet-indexcreate-structure.md) ou [JetMakeKey](./jetmakekey-function.md). A especificação desse sinalizador fará com que qualquer atualização do índice que resulte em uma chave truncada falhe com JET_errKeyTruncated. Caso contrário, as chaves serão truncadas silenciosamente. Isso permitirá que o aplicativo funcione sem preocupação com os artefatos causados pelo truncamento de chave que foi descrito anteriormente.
