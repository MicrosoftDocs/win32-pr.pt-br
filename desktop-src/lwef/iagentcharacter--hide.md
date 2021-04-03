---
title: Ocultar IAgentCharacter
description: Ocultar IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007471"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="c46b5-103">IAgentCharacter:: Hide</span><span class="sxs-lookup"><span data-stu-id="c46b5-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="c46b5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c46b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c46b5-105">Oculta o caractere.</span><span class="sxs-lookup"><span data-stu-id="c46b5-105">Hides the character.</span></span>

-   <span data-ttu-id="c46b5-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c46b5-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="c46b5-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c46b5-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="c46b5-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="c46b5-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="c46b5-109">Sinalizador de animação de estado **oculto** .</span><span class="sxs-lookup"><span data-stu-id="c46b5-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="c46b5-110">Se esse parâmetro for **true**, a animação de **ocultação** não será reproduzida antes que o quadro de caracteres fique oculto; Se **for false**, a animação será reproduzida.</span><span class="sxs-lookup"><span data-stu-id="c46b5-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="c46b5-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="c46b5-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c46b5-112">Endereço de uma variável que recebe a ID da solicitação de **ocultação** .</span><span class="sxs-lookup"><span data-stu-id="c46b5-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c46b5-113">O servidor enfileira a animação associada ao método **Hide** na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="c46b5-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="c46b5-114">Isso permite que você o use para ocultar o caractere após uma sequência de outras animações.</span><span class="sxs-lookup"><span data-stu-id="c46b5-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="c46b5-115">Você pode executar a ação imediatamente usando o método [**Stop**](iagentcharacter--stop.md) antes de chamar o método **Hide** .</span><span class="sxs-lookup"><span data-stu-id="c46b5-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="c46b5-116">Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade da animação de estado **oculto** antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="c46b5-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="c46b5-117">Ocultar um caractere também pode resultar no disparo do evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) de outro caractere visível.</span><span class="sxs-lookup"><span data-stu-id="c46b5-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="c46b5-118">Os caracteres ocultos não podem acessar o canal de áudio.</span><span class="sxs-lookup"><span data-stu-id="c46b5-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="c46b5-119">O servidor passará um status de falha no evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) se você gerar uma solicitação de animação e o caractere estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="c46b5-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="c46b5-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c46b5-120">See Also</span></span>

[<span data-ttu-id="c46b5-121">**IAgentCharacter:: mostrar**</span><span class="sxs-lookup"><span data-stu-id="c46b5-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 