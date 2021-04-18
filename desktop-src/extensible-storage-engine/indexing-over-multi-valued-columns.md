---
description: 'Saiba mais sobre: indexação em colunas com valores múltiplos'
title: Indexação em colunas com valores múltiplos
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781211"
---
# <a name="indexing-over-multi-valued-columns"></a>Indexação em colunas com valores múltiplos


_**Aplica-se a:** Windows | Windows Server_

## <a name="indexing-over-multi-valued-columns"></a>Indexação em colunas com valores múltiplos

A indexação em colunas com vários valores só é executada pela primeira coluna de valores múltiplos no índice. A primeira coluna com vários valores é expandida para que todos os valores na coluna sejam indexados. Todas as outras colunas com valores múltiplos são indexadas somente no primeiro valor da coluna. Por exemplo, um índice é definido na coluna A e na coluna B, em que essas duas colunas têm valores múltiplos. Em um determinado registro, a coluna A tem os valores vermelho e azul, e a coluna B tem os valores 1, 2 e 3. O índice resultante forneceria entradas para Red-1 e Blue-1. Os valores na segunda coluna, coluna B, não são expandidos. Observe que, embora todas as colunas marcadas possam ter valores múltiplos, somente as colunas marcadas sinalizadas explicitamente como com valores múltiplos por meio de JET_bitColumnMultiValued são expandidas dessa maneira. Além disso, devido ao fato de que as entradas de índice primário contêm registros, não é permitido ter um índice primário em uma coluna com valores múltiplos porque isso resultaria em vários locais no índice em que o registro teria que residir. Para obter mais informações, consulte o tópico [marcas, fixas e variáveis em colunas](./tagged-fixed-and-variable-columns.md) .

A partir do Windows Vista, os usuários têm a opção de definir a opção JET_bitIndexCrossProduct quando o índice é criado com [JetCreateIndex](./jetcreateindex-function.md) ou [JetCreateIndex2](./jetcreateindex2-function.md) usando a estrutura [JET_INDEXCREATE](./jet-indexcreate-structure.md) . Quando essa opção é definida em um índice, todas as colunas de chave com valores múltiplos no índice são expandidas e um produto cruzado é criado no índice para cada valor nessas colunas. O exemplo acima agora produz entradas para vermelho-1, vermelho-2, vermelho-3, azul-1, azul-2, azul-3. Novamente, cada coluna de chave deve ser declarada explicitamente para ter valores múltiplos por meio de JET_bitColumnMultiValued ser expandida no índice.
