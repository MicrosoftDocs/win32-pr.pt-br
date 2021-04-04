---
title: IAgentCharacterEx getactive
description: IAgentCharacterEx getactive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822888"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="90df4-103">IAgentCharacterEx:: getactive</span><span class="sxs-lookup"><span data-stu-id="90df4-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="90df4-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90df4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="90df4-105">Recupera se o aplicativo cliente é o cliente ativo do caractere e se o caractere está no nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="90df4-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="90df4-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="90df4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="90df4-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span><span class="sxs-lookup"><span data-stu-id="90df4-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="90df4-108">Endereço de uma variável que recebe um dos seguintes valores para a configuração de Estado:</span><span class="sxs-lookup"><span data-stu-id="90df4-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="90df4-109">Valor</span><span class="sxs-lookup"><span data-stu-id="90df4-109">Value</span></span>                                                              | <span data-ttu-id="90df4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="90df4-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="90df4-111">**const não assinada curto ativar não** **\_ ativo = 0;**</span><span class="sxs-lookup"><span data-stu-id="90df4-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="90df4-112">O cliente não é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="90df4-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="90df4-113">**const não assinada curto** **Ativar \_ ativa = 1;**</span><span class="sxs-lookup"><span data-stu-id="90df4-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="90df4-114">O cliente é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="90df4-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="90df4-115">**const não assinada curto** **Ativar \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="90df4-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="90df4-116">O cliente está em entrada-ativo (cliente ativo do caractere superior).</span><span class="sxs-lookup"><span data-stu-id="90df4-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="90df4-117">Essa configuração permite que você saiba se você é o cliente ativo do caractere ou se o caractere é o caractere ativo de entrada.</span><span class="sxs-lookup"><span data-stu-id="90df4-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="90df4-118">Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos).</span><span class="sxs-lookup"><span data-stu-id="90df4-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="90df4-119">Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="90df4-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="90df4-120">Use o método [**Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada ativo (o que também torna o caractere mais alto).</span><span class="sxs-lookup"><span data-stu-id="90df4-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="90df4-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="90df4-121">See Also</span></span>

<span data-ttu-id="90df4-122">[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="90df4-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





