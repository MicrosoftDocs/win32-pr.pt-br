---
description: 'Saiba mais sobre: pesquisa de registros no índice'
title: Pesquisando registros no índice
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789479"
---
# <a name="searching-records-in-the-index"></a>Pesquisando registros no índice


_**Aplica-se a:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Pesquisando registros no índice

As chaves de pesquisa são criadas para pesquisar uma única entrada ou um conjunto de entradas em um índice. As chaves de pesquisa só podem ser construídas para as colunas de chave no índice e podem conter um ou mais valores de coluna. A chave de pesquisa é construída com uma única chamada ou uma série de chamadas para [JetMakeKey](./jetmakekey-function.md)e pode ser recuperada com [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy. Depois que a chave de pesquisa é construída, ela pode ser usada para mover o cursor para o registro no índice.

Há três métodos de localizar registros em uma tabela:

1.  Procure uma única entrada de índice. Para fazer isso, crie a chave de pesquisa com [JetMakeKey](./jetmakekey-function.md)e, em seguida, mova para esse registro com [JetSeek](./jetseek-function.md).

2.  Pesquise o índice registro por registro. Os registros podem ser atravessados em um registro por vez, chamando [JetMove](./jetmove-function.md). O cursor pode ser movido para o primeiro registro no índice, especificando JET_MoveFirst no parâmetro de *galinha* de [JetMove](./jetmove-function.md). Da mesma forma, o cursor pode ser movido para frente, para trás ou para a última entrada no índice.

3.  Pesquisar em um conjunto de registros. Para fazer isso, defina um intervalo de entradas de índice a serem pesquisadas e, em seguida, mova os registros sequencialmente. Para obter mais informações, consulte [pesquisando um conjunto de registros]() seção deste tópico.

### <a name="searching-through-a-set-of-records"></a>Pesquisando um conjunto de registros

O diagrama aqui mostra o cursor passando por um intervalo de entradas de índice definidas por chamadas para [JetSeek](./jetseek-function.md) e [JetSetIndexRange](./jetsetindexrange-function.md).

Use o procedimento a seguir para pesquisar em um conjunto de registros em um índice.

### <a name="to-search-a-set-of-records-in-an-index"></a>Para pesquisar um conjunto de registros em um índice

1.  Crie a chave de pesquisa para o primeiro registro no conjunto de registros a ser pesquisado com [JetMakeKey](./jetmakekey-function.md).

2.  Mova o cursor para o registro indicado na chave de pesquisa com [JetSeek](./jetseek-function.md).

3.  Crie outra chave de pesquisa para a última entrada de índice no intervalo com [JetMakeKey](./jetmakekey-function.md).

4.  Defina o intervalo de índice com [JetSetIndexRange](./jetsetindexrange-function.md) usando a chave criada na etapa 3.

5.  Chame [JetMove](./jetmove-function.md) para mover sequencialmente por cada registro no intervalo de índice, conforme mostrado no diagrama a seguir.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

O cursor no diagrama aqui só pode percorrer o intervalo de índices definido na chamada para [JetSetIndexRange](./jetsetindexrange-function.md). Se o aplicativo tentar mover o cursor além do intervalo de índice, o ESE retornará um erro Jet_errNoCurrentRecord da chamada para [JetMove](./jetmove-function.md). Observe que qualquer tipo de navegação com esse cursor diferente de mover para o registro seguinte ou anterior cancelará o intervalo de índice. Consulte [JetSetIndexRange](./jetsetindexrange-function.md) para obter mais informações.

O tipo de dados inserido no parâmetro *pvData* para [JetMakeKey](./jetmakekey-function.md) deve corresponder ao tipo de dados e às propriedades especificadas para a coluna. Por exemplo, chamar [JetMakeKey](./jetmakekey-function.md) com "Ben Miller" especificado no parâmetro *pvData* para um tipo de coluna JET_coltypText é uma correspondência de tipo de dados válida. Se você quiser criar uma chave de pesquisa para pesquisar entre os nomes "Ben Miller" e "Max Stevens" em um índice, mova o cursor para o registro com o nome "Ben Miller" chamando [JetSeek](./jetseek-function.md). Chame [JetMakeKey](./jetmakekey-function.md) uma segunda vez e especifique um ponteiro para uma cadeia de caracteres que contenha o nome "Max Stevens". O intervalo de índice é definido para limitar o cursor a ser movido entre os nomes "Ben Miller" e "Max Stevens" na chamada para [JetSetIndexRange](./jetsetindexrange-function.md).
