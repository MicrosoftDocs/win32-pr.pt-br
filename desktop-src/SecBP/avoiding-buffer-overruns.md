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
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="a04b0-103">Evitando estouros de buffer</span><span class="sxs-lookup"><span data-stu-id="a04b0-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="a04b0-104">Uma saturação de buffer é uma das fontes mais comuns de risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="a04b0-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="a04b0-105">Uma saturação de buffer é essencialmente causada pela tratamento de entrada externa não verificada como dados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="a04b0-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="a04b0-106">O ato de copiar esses dados, usando operações como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** ou **wcscpy**, pode criar resultados imprevistos, o que permite a corrupção do sistema.</span><span class="sxs-lookup"><span data-stu-id="a04b0-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="a04b0-107">No melhor dos casos, seu aplicativo será anulado com um dump principal, uma falha de segmentação ou uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="a04b0-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="a04b0-108">No pior dos casos, um invasor pode explorar a saturação do buffer introduzindo e executando outros códigos mal-intencionados em seu processo.</span><span class="sxs-lookup"><span data-stu-id="a04b0-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="a04b0-109">A cópia desmarcada, dados de entrada em um buffer baseado em pilha é a causa mais comum de falhas exploráveis.</span><span class="sxs-lookup"><span data-stu-id="a04b0-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="a04b0-110">As saturações de buffer podem ocorrer de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="a04b0-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="a04b0-111">A lista a seguir fornece uma breve introdução a alguns tipos de situações de saturação de buffer e oferece algumas ideias e recursos para ajudá-lo a evitar a criação de novos riscos e a mitigar os existentes:</span><span class="sxs-lookup"><span data-stu-id="a04b0-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="a04b0-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Saturações de buffer estático</span><span class="sxs-lookup"><span data-stu-id="a04b0-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="a04b0-113">Uma saturação de buffer estático ocorre quando um buffer, que foi declarado na pilha, é gravado em com mais dados do que foi alocado para conter.</span><span class="sxs-lookup"><span data-stu-id="a04b0-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="a04b0-114">As versões menos aparentes desse erro ocorrem quando dados de entrada do usuário não verificados são copiados diretamente para uma variável estática, causando uma possível corrupção da pilha.</span><span class="sxs-lookup"><span data-stu-id="a04b0-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="a04b0-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Saturações de heap</span><span class="sxs-lookup"><span data-stu-id="a04b0-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="a04b0-116">Saturações de heap, como estouros de buffer estático, podem levar à memória e à corrupção de pilha.</span><span class="sxs-lookup"><span data-stu-id="a04b0-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="a04b0-117">Como as saturações de heap ocorrem na memória de heap em vez de na pilha, algumas pessoas as consideram menos capazes de causar problemas sérios; no entanto, as saturações de heap exigem o real cuidado de programação e são capazes de permitir riscos de sistema como estouros de buffer estáticos.</span><span class="sxs-lookup"><span data-stu-id="a04b0-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="a04b0-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Erros de indexação de matriz</span><span class="sxs-lookup"><span data-stu-id="a04b0-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="a04b0-119">Erros de indexação de matriz também são uma fonte de saturações de memória.</span><span class="sxs-lookup"><span data-stu-id="a04b0-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="a04b0-120">Verificação de limites cuidadoso e gerenciamento de índice ajudará a evitar esse tipo de saturação de memória.</span><span class="sxs-lookup"><span data-stu-id="a04b0-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="a04b0-121">Impedir saturações de buffer é, basicamente, escrever um bom código.</span><span class="sxs-lookup"><span data-stu-id="a04b0-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="a04b0-122">Sempre valide todas as suas entradas e falhe normalmente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="a04b0-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="a04b0-123">Para obter mais informações sobre como escrever código seguro, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="a04b0-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="a04b0-124">Maguire, Steve \[ 1993 \] , *escrevendo código sólido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="a04b0-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="a04b0-125">Howard, Michael e LeBlanc, David \[ 2003 \] , *escrevendo código seguro*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="a04b0-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="a04b0-126">Esses recursos podem não estar disponíveis em alguns idiomas e países.</span><span class="sxs-lookup"><span data-stu-id="a04b0-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="a04b0-127">A manipulação de cadeia de caracteres segura é um problema de longa duração que continua sendo abordado seguindo práticas recomendadas de programação e muitas vezes usando e modernização sistemas existentes com funções de manipulação de cadeias de caracteres seguras.</span><span class="sxs-lookup"><span data-stu-id="a04b0-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="a04b0-128">Um exemplo desse conjunto de funções para o Shell do Windows começa com [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="a04b0-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
