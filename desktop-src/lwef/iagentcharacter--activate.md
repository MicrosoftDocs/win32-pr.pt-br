---
title: IAgentCharacter ativar
description: IAgentCharacter ativar
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498822"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="b4e2b-103">IAgentCharacter:: ativar</span><span class="sxs-lookup"><span data-stu-id="b4e2b-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="b4e2b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4e2b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="b4e2b-105">Define se um cliente está ativo ou se um caractere está no nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="b4e2b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="b4e2b-107">Retorna S \_ false para indicar que a operação não foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="b4e2b-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="b4e2b-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="b4e2b-109">Você pode especificar os seguintes valores para este parâmetro:</span><span class="sxs-lookup"><span data-stu-id="b4e2b-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="b4e2b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b4e2b-110">Value</span></span> | <span data-ttu-id="b4e2b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4e2b-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="b4e2b-112">0</span><span class="sxs-lookup"><span data-stu-id="b4e2b-112">0</span></span>     | <span data-ttu-id="b4e2b-113">Defina como não o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-113">Set as not the active client.</span></span> |
| <span data-ttu-id="b4e2b-114">1</span><span class="sxs-lookup"><span data-stu-id="b4e2b-114">1</span></span>     | <span data-ttu-id="b4e2b-115">Defina como o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-115">Set as the active client.</span></span>     |
| <span data-ttu-id="b4e2b-116">2</span><span class="sxs-lookup"><span data-stu-id="b4e2b-116">2</span></span>     | <span data-ttu-id="b4e2b-117">Faça o caractere superior.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="b4e2b-118">Quando vários caracteres são visíveis, apenas um dos caracteres recebe a entrada de fala de cada vez.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="b4e2b-119">Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, apenas um dos clientes recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos) de cada vez.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="b4e2b-120">O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere superior e o cliente que recebe a entrada é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="b4e2b-121">(A janela do caractere superior também aparece na parte superior da ordem z da janela de caractere.) Normalmente, o usuário determina qual caractere é mais alto selecionando-o explicitamente.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="b4e2b-122">No entanto, a ativação na extremidade superior também é alterada quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais o mais alto, respectivamente.)</span><span class="sxs-lookup"><span data-stu-id="b4e2b-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="b4e2b-123">Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe a entrada direcionada para o caractere, como quando o próprio aplicativo se torna ativo.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="b4e2b-124">Por exemplo, definir **State** como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="b4e2b-125">Portanto, ele também torna o cliente o cliente de entrada-ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="b4e2b-126">No entanto, você também pode definir o cliente ativo para um caractere sem tornar o caractere mais alto, definindo o **estado** como 1.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="b4e2b-127">Isso permite que o cliente receba entrada direcionada para esse caractere quando o caractere se tornar mais alto.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="b4e2b-128">Da mesma forma, você pode definir que o cliente não seja o cliente ativo (para não receber a entrada) quando o caractere se tornar mais alto, definindo **State** como 0.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="b4e2b-129">Você pode determinar se um caractere tem outros clientes atuais usando [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).</span><span class="sxs-lookup"><span data-stu-id="b4e2b-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="b4e2b-130">Evite chamar esse método diretamente após um método [**show**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e2b-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="b4e2b-131">**Mostrar** define automaticamente o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="b4e2b-132">Quando o caractere estiver oculto, a chamada **Ativar** poderá falhar, se for processada antes que o método **show** seja concluído.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="b4e2b-133">A tentativa de chamar esse método com o parâmetro de **estado** definido como 2 (quando o caractere especificado estiver oculto) falhará.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="b4e2b-134">Da mesma forma, se você definir **State** como 0 e seu aplicativo for o único cliente, essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="b4e2b-135">Um caractere sempre deve ter um cliente superior.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="b4e2b-136">Chamar esse método com o **estado** definido como 1 normalmente não gera um evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) , a menos que não haja nenhum outro caractere carregado ou que seu aplicativo já esteja em entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="b4e2b-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b4e2b-137">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b4e2b-137">See Also</span></span>

[<span data-ttu-id="b4e2b-138">**IAgentCharacter::HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="b4e2b-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




