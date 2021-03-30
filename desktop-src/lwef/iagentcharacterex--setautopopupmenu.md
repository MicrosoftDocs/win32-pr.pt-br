---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916330"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="01839-103">IAgentCharacterEx::SetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="01839-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="01839-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01839-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="01839-105">Define se o servidor exibe automaticamente o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="01839-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="01839-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="01839-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="01839-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="01839-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="01839-108">O sinalizador de exibição de menu pop-up automático.</span><span class="sxs-lookup"><span data-stu-id="01839-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="01839-109">Se esse parâmetro for **true**, o Microsoft Agent exibirá automaticamente o menu pop-up do caractere quando o usuário clicar com o botão direito do mouse no ícone da barra de tarefas do caractere ou caractere.</span><span class="sxs-lookup"><span data-stu-id="01839-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="01839-110">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="01839-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="01839-111">Ao definir essa propriedade como **false**, você pode criar seu próprio comportamento de manipulação de menus.</span><span class="sxs-lookup"><span data-stu-id="01839-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="01839-112">Para exibir o menu depois de definir essa propriedade como **false**, use o método [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="01839-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="01839-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="01839-113">See Also</span></span>

<span data-ttu-id="01839-114">[**IAgentCharacterEx:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="01839-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




