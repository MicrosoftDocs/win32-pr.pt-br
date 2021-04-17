---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763019"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="fc2e1-103">IAgentNotifySinkEx::ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="fc2e1-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="fc2e1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc2e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="fc2e1-105">Notifica um aplicativo cliente se seu cliente ativo não for mais o cliente ativo de um caractere.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="fc2e1-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fc2e1-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="fc2e1-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="fc2e1-108">Identificador do caractere para o qual o status do cliente ativo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="fc2e1-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span><span class="sxs-lookup"><span data-stu-id="fc2e1-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="fc2e1-110">Alteração de estado ativo do cliente, que pode ser uma combinação de qualquer um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fc2e1-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="fc2e1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="fc2e1-111">Value</span></span>                                                              | <span data-ttu-id="fc2e1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc2e1-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="fc2e1-113">**const não assinada curto ativar não** **\_ ativo = 0;**</span><span class="sxs-lookup"><span data-stu-id="fc2e1-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="fc2e1-114">O cliente não é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="fc2e1-115">**const não assinada curto** **Ativar \_ ativa = 1;**</span><span class="sxs-lookup"><span data-stu-id="fc2e1-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="fc2e1-116">O cliente é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="fc2e1-117">**const não assinada curto** **Ativar \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="fc2e1-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="fc2e1-118">O cliente está em entrada-ativo (cliente ativo do caractere superior).</span><span class="sxs-lookup"><span data-stu-id="fc2e1-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="fc2e1-119">Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos).</span><span class="sxs-lookup"><span data-stu-id="fc2e1-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="fc2e1-120">Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="fc2e1-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="fc2e1-121">Quando o cliente ativo de um caractere é alterado, esse evento retorna a ID desse caractere e **true** se o aplicativo se tornou o cliente ativo do caractere ou **false** se não for mais o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="fc2e1-122">Um aplicativo cliente pode receber esse evento quando o usuário seleciona a entrada de outro aplicativo cliente no menu pop-up do caractere ou por comando de voz, o aplicativo cliente altera seu status ativo ou outro aplicativo cliente encerra sua conexão com o Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="fc2e1-123">O Agent envia esse evento somente para os aplicativos cliente que são diretamente afetados – aqueles que se tornam o cliente ativo ou que param de ser o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="fc2e1-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="fc2e1-124">Você pode usar o método [**Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada-ativo (o que também torna o caractere mais alto).</span><span class="sxs-lookup"><span data-stu-id="fc2e1-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc2e1-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fc2e1-125">See Also</span></span>

<span data-ttu-id="fc2e1-126">[**IAgentCharacter:: ativar**](iagentcharacter--activate.md), [**IAgentCharacterEx:: getactive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="fc2e1-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





