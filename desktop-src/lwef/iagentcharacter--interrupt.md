---
title: Interrupção de IAgentCharacter
description: Interrupção de IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917167"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="0f597-103">IAgentCharacter:: Interrupt</span><span class="sxs-lookup"><span data-stu-id="0f597-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="0f597-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f597-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="0f597-105">Interrompe a animação especificada (solicitação) de outro caractere.</span><span class="sxs-lookup"><span data-stu-id="0f597-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="0f597-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f597-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="0f597-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0f597-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="0f597-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="0f597-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="0f597-109">Uma ID da solicitação a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="0f597-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="0f597-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="0f597-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="0f597-111">Endereço de uma variável que recebe a ID da solicitação de **interrupção** .</span><span class="sxs-lookup"><span data-stu-id="0f597-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="0f597-112">Se você carregar vários caracteres, poderá usar esse método para sincronizar a animação entre os caracteres.</span><span class="sxs-lookup"><span data-stu-id="0f597-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="0f597-113">Por exemplo, se outro caractere estiver em uma animação de looping, esse método irá parar a animação de looping e iniciar a próxima animação na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="0f597-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="0f597-114">A **interrupção** interrompe a animação existente, mas não libera a fila de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="0f597-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="0f597-115">Ele inicia a próxima animação na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="0f597-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="0f597-116">Para interromper e liberar a fila de um caractere, use o método [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .</span><span class="sxs-lookup"><span data-stu-id="0f597-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="0f597-117">Você não pode usar esse método para ter uma interrupção de caractere em si porque o servidor do Microsoft Agent enfileira o método de **interrupção** na fila de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="0f597-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="0f597-118">Portanto, você só pode usar a **interrupção** para interromper a animação de outro caractere que você carregou.</span><span class="sxs-lookup"><span data-stu-id="0f597-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 