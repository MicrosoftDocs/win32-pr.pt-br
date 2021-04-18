---
description: Fornece uma breve introdução a alguns tipos de situações de saturação de buffer e oferece algumas ideias e recursos para ajudá-lo a evitar a criação de novos riscos e a mitigar os existentes.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitando estouros de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769192"
---
# <a name="avoiding-buffer-overruns"></a>Evitando estouros de buffer

Uma saturação de buffer é uma das fontes mais comuns de risco de segurança. Uma saturação de buffer é essencialmente causada pela tratamento de entrada externa não verificada como dados confiáveis. O ato de copiar esses dados, usando operações como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** ou **wcscpy**, pode criar resultados imprevistos, o que permite a corrupção do sistema. No melhor dos casos, seu aplicativo será anulado com um dump principal, uma falha de segmentação ou uma violação de acesso. No pior dos casos, um invasor pode explorar a saturação do buffer introduzindo e executando outros códigos mal-intencionados em seu processo. A cópia desmarcada, dados de entrada em um buffer baseado em pilha é a causa mais comum de falhas exploráveis.

As saturações de buffer podem ocorrer de várias maneiras. A lista a seguir fornece uma breve introdução a alguns tipos de situações de saturação de buffer e oferece algumas ideias e recursos para ajudá-lo a evitar a criação de novos riscos e a mitigar os existentes:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Saturações de buffer estático
</dt> <dd>

Uma saturação de buffer estático ocorre quando um buffer, que foi declarado na pilha, é gravado em com mais dados do que foi alocado para conter. As versões menos aparentes desse erro ocorrem quando dados de entrada do usuário não verificados são copiados diretamente para uma variável estática, causando uma possível corrupção da pilha.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Saturações de heap
</dt> <dd>

Saturações de heap, como estouros de buffer estático, podem levar à memória e à corrupção de pilha. Como as saturações de heap ocorrem na memória de heap em vez de na pilha, algumas pessoas as consideram menos capazes de causar problemas sérios; no entanto, as saturações de heap exigem o real cuidado de programação e são capazes de permitir riscos de sistema como estouros de buffer estáticos.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Erros de indexação de matriz
</dt> <dd>

Erros de indexação de matriz também são uma fonte de saturações de memória. Verificação de limites cuidadoso e gerenciamento de índice ajudará a evitar esse tipo de saturação de memória.

</dd> </dl>

Impedir saturações de buffer é, basicamente, escrever um bom código. Sempre valide todas as suas entradas e falhe normalmente quando necessário. Para obter mais informações sobre como escrever código seguro, consulte os seguintes recursos:

-   Maguire, Steve \[ 1993 \] , *escrevendo código sólido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael e LeBlanc, David \[ 2003 \] , *escrevendo código seguro*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países.

 

A manipulação de cadeia de caracteres segura é um problema de longa duração que continua sendo abordado seguindo práticas recomendadas de programação e muitas vezes usando e modernização sistemas existentes com funções de manipulação de cadeias de caracteres seguras. Um exemplo desse conjunto de funções para o Shell do Windows começa com [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 
