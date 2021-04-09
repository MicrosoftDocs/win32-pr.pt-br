---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822799"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="67b46-103">IAgentCharacterEx::ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="67b46-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="67b46-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67b46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="67b46-105">Exibe o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="67b46-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="67b46-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="67b46-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="67b46-107"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="67b46-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="67b46-108">A coordenada x do menu pop-up do caractere em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="67b46-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="67b46-109"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="67b46-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="67b46-110">A coordenada y do menu pop-up do caractere em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="67b46-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="67b46-111">Quando você define [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) como **false**, o servidor não exibe mais automaticamente o menu quando o caractere ou o ícone da barra de tarefas é clicado com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="67b46-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="67b46-112">Você pode usar esse método para exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="67b46-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="67b46-113">O menu é exibido até que o usuário selecione um comando ou exiba outro menu.</span><span class="sxs-lookup"><span data-stu-id="67b46-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="67b46-114">Somente um menu pop-up pode ser exibido de cada vez; Portanto, as chamadas para esse método irão cancelar (remover) o menu anterior.</span><span class="sxs-lookup"><span data-stu-id="67b46-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="67b46-115">Esse método deve ser chamado somente quando o aplicativo cliente é o cliente ativo do caractere; caso contrário, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="67b46-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="67b46-116">**IAgentCharacterEx::SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="67b46-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




