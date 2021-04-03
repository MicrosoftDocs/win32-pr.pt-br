---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916474"
---
# <a name="iagentcharacterexgetautopopupmenu"></a><span data-ttu-id="93dd6-103">IAgentCharacterEx::GetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="93dd6-103">IAgentCharacterEx::GetAutoPopupMenu</span></span>

<span data-ttu-id="93dd6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93dd6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

<span data-ttu-id="93dd6-105">Recupera se o servidor exibe automaticamente o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="93dd6-105">Retrieves whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="93dd6-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="93dd6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="93dd6-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="93dd6-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="93dd6-108">Endereço de uma variável que recebe **true** se o servidor do Microsoft Agent manipular automaticamente a exibição do menu pop-up do caractere e **false** se não.</span><span class="sxs-lookup"><span data-stu-id="93dd6-108">Address of a variable that receives **True** if the Microsoft Agent server automatically handles displaying the character's pop-up menu and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="93dd6-109">Quando essa propriedade é definida como **false**, seu aplicativo deve exibir o menu pop-up usando o método [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="93dd6-109">When this property is set to **False**, your application must display the pop-up menu using [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

<span data-ttu-id="93dd6-110">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="93dd6-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="93dd6-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="93dd6-111">See Also</span></span>

<span data-ttu-id="93dd6-112">[**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="93dd6-112">[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




