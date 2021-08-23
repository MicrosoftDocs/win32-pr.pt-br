---
description: Fornece uma breve introdução a alguns tipos de situações de estouro de buffer e oferece algumas ideias e recursos para ajudá-lo a evitar a criação de novos riscos e atenuar os existentes.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitando estouros de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae85d66d32b1efc29e75e187bb1afa67653084a3b9c729cd56728078f5e0c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622946"
---
# <a name="avoiding-buffer-overruns"></a>Evitando estouros de buffer

Um estouro de buffer é uma das fontes de risco de segurança mais comuns. Um estouro de buffer é essencialmente causado pelo tratamento de entrada externa desmarcada como dados confiáveis. O ato de copiar esses dados, usando operações como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** ou **wcscpy**, pode criar resultados imprevistos, o que permite a corrupção do sistema. Na melhor das situações, seu aplicativo será anulado com um despejo principal, falha de segmentação ou violação de acesso. Na pior das hipóteses, um invasor pode explorar o estouro do buffer introduzindo e executando outro código mal-intencionado em seu processo. Copiar dados de entrada não verificados em um buffer baseado em pilha é a causa mais comum de falhas exploráveis.

Os estouros de buffer podem ocorrer de várias maneiras. A lista a seguir fornece uma breve introdução a alguns tipos de situações de estouro de buffer e oferece algumas ideias e recursos para ajudá-lo a evitar a criação de novos riscos e atenuar os existentes:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Estouros de buffer estático
</dt> <dd>

Um estouro de buffer estático ocorre quando um buffer, que foi declarado na pilha, é gravado com mais dados do que foi alocado para manter. As versões menos aparentes desse erro ocorrem quando os dados de entrada do usuário não verificados são copiados diretamente para uma variável estática, causando potencial corrupção de pilha.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Estouros de heap
</dt> <dd>

Estouros de heap, como estouros de buffer estático, podem levar à corrupção de memória e pilha. Como as estouros de heap ocorrem na memória do heap em vez de na pilha, algumas pessoas as consideram menos capazes de causar problemas sérios; no entanto, as estouros de heap exigem cuidado real com a programação e são tão capazes de permitir riscos do sistema quanto estouros de buffer estático.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Erros de indexação de matriz
</dt> <dd>

Erros de indexação de matriz também são uma fonte de estouros de memória. A verificação cuidadosa de limites e o gerenciamento de índice ajudarão a evitar esse tipo de estouros de memória.

</dd> </dl>

Evitar estouros de buffer se trata principalmente de escrever um bom código. Sempre valide todas as suas entradas e falhe normalmente quando necessário. Para obter mais informações sobre como escrever código seguro, consulte os seguintes recursos:

-   Gates, Steve \[ 1993, \] *Escrevendo código* sólido, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Charles, Michael e Le Ltda, David \[ 2003 , Escrevendo código \] seguro, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países.

 

Cofre manipulação de cadeia de caracteres é um problema de longa duração que continua a ser resolvido seguindo as boas práticas de programação e, muitas vezes, usando e reajustando sistemas existentes com funções seguras de manipulação de cadeia de caracteres. Um exemplo desse conjunto de funções para o shell Windows começa com [**StringCbCat.**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)

 

 
