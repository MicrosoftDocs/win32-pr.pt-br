---
description: Esta seção descreve a sintaxe e o uso de manipulação de exceção estruturada conforme implementado no compilador de otimização do Microsoft C/C++. As seguintes palavras-chave são interpretadas pelo compilador como parte do mecanismo de manipulação de exceção estruturado.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintaxe do manipulador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826170"
---
# <a name="handler-syntax"></a><span data-ttu-id="76bf9-104">Sintaxe do manipulador</span><span class="sxs-lookup"><span data-stu-id="76bf9-104">Handler Syntax</span></span>

<span data-ttu-id="76bf9-105">Esta seção descreve a sintaxe e o uso de manipulação de exceção estruturada conforme implementado no compilador de otimização do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="76bf9-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="76bf9-106">As seguintes palavras-chave são interpretadas pelo compilador como parte do mecanismo de manipulação de exceção estruturado.</span><span class="sxs-lookup"><span data-stu-id="76bf9-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="76bf9-107">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="76bf9-107">Keyword</span></span>         | <span data-ttu-id="76bf9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="76bf9-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76bf9-109">**\_\_Tente**</span><span class="sxs-lookup"><span data-stu-id="76bf9-109">**\_\_try**</span></span>     | <span data-ttu-id="76bf9-110">Inicia um corpo de código protegido.</span><span class="sxs-lookup"><span data-stu-id="76bf9-110">Begins a guarded body of code.</span></span> <span data-ttu-id="76bf9-111">Usado com a palavra-chave **\_ \_ Except** para construir um [manipulador de exceção](exception-handler-syntax.md)ou com a palavra-chave **\_ \_ finally** para construir um [manipulador de terminação](termination-handler-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="76bf9-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="76bf9-112">**\_\_excepção**</span><span class="sxs-lookup"><span data-stu-id="76bf9-112">**\_\_except**</span></span>  | <span data-ttu-id="76bf9-113">Inicia um bloco de código que é executado somente quando ocorre uma exceção dentro de seu bloco **\_ \_ try** associado.</span><span class="sxs-lookup"><span data-stu-id="76bf9-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="76bf9-114">**\_\_disso**</span><span class="sxs-lookup"><span data-stu-id="76bf9-114">**\_\_finally**</span></span> | <span data-ttu-id="76bf9-115">Inicia um bloco de código que é executado sempre que o fluxo de controle deixa seu bloco **\_ \_ try** associado.</span><span class="sxs-lookup"><span data-stu-id="76bf9-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="76bf9-116">**\_\_Deixe**</span><span class="sxs-lookup"><span data-stu-id="76bf9-116">**\_\_leave**</span></span>   | <span data-ttu-id="76bf9-117">Permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho.</span><span class="sxs-lookup"><span data-stu-id="76bf9-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="76bf9-118">O compilador também interpreta as funções [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)e [**AbnormalTermination**](abnormaltermination.md) como palavras-chave, e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.</span><span class="sxs-lookup"><span data-stu-id="76bf9-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="76bf9-119">Veja a seguir as breves descrições dessas funções.</span><span class="sxs-lookup"><span data-stu-id="76bf9-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="76bf9-120">Função</span><span class="sxs-lookup"><span data-stu-id="76bf9-120">Function</span></span>                                                   | <span data-ttu-id="76bf9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="76bf9-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76bf9-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="76bf9-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="76bf9-123">Retorna um código que identifica o tipo de exceção.</span><span class="sxs-lookup"><span data-stu-id="76bf9-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="76bf9-124">Essa função pode ser chamada somente de dentro da expressão de filtro ou do bloco de manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="76bf9-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="76bf9-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="76bf9-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="76bf9-126">Retorna um ponteiro para uma [**exceção que \_ aponta**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para uma estrutura contendo ponteiros para o registro de contexto e o registro de exceção.</span><span class="sxs-lookup"><span data-stu-id="76bf9-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="76bf9-127">Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="76bf9-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="76bf9-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="76bf9-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="76bf9-129">Indica se o fluxo de controle saiu do bloco **\_ \_ try** associado sequencialmente após a execução da última instrução no bloco.</span><span class="sxs-lookup"><span data-stu-id="76bf9-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="76bf9-130">Essa função pode ser chamada somente de dentro do bloco **\_ \_ finally** de um manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="76bf9-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



