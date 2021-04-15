---
description: 'Saiba mais sobre: sequenciamento em colunas com valores múltiplos'
title: Sequenciamento em colunas com valores múltiplos
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569660"
---
# <a name="sequencing-in-multi-valued-columns"></a>Sequenciamento em colunas com valores múltiplos


_**Aplica-se a:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Sequenciamento em colunas com valores múltiplos

Os valores em uma coluna com valores múltiplos são identificados por um número de índice chamado *itagSequence*. Esse número é uma referência a um único valor da coluna. Esse número é usado quando novos valores são definidos, recuperados ou enumerados na coluna. O *itagSequence* é usado em várias estruturas, incluindo:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Esse *itagSequence* começa em 1 para cada valor na coluna de valores múltiplos. O número de sequência aumenta quando novos valores são adicionados à coluna. Definir um valor em uma coluna com um *itagSequence* de 0 indica que o valor deve ser acrescentado ao conjunto de valores já existentes nessa coluna. O uso de um *itagSequence* maior que o número de valores atualmente definidos para uma coluna terá o mesmo efeito. Especificar o *itagSequence* de um valor existente substituirá esse valor, não inserirá um novo. A definição de um valor existente como NULL removerá esse valor do conjunto de valores já existentes nessa coluna. Isso moverá todos os valores subsequentes na coluna por um slot de modo que o acesso subsequente a esses valores por *itagSequence* seja de um número menor do que o usado anteriormente.

O diagrama a seguir mostra um *itagSequence* em uma coluna com vários valores. A coluna chamada ColA tem três entradas: val1, Val2 e Val3 com *itagSequence* de 1, 2 e 3, respectivamente.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
