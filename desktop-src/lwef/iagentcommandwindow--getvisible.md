---
title: IAgentCommandWindow getVisible
description: IAgentCommandWindow getVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105785933"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="c29a7-103">IAgentCommandWindow:: getVisible</span><span class="sxs-lookup"><span data-stu-id="c29a7-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="c29a7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c29a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="c29a7-105">Determina se a janela de comandos de voz está visível ou oculta.</span><span class="sxs-lookup"><span data-stu-id="c29a7-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="c29a7-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c29a7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c29a7-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="c29a7-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="c29a7-108">Endereço de uma variável que recebe **true** se a janela de comandos de voz estiver visível ou **false** se estiver oculta.</span><span class="sxs-lookup"><span data-stu-id="c29a7-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c29a7-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c29a7-109">See Also</span></span>

[<span data-ttu-id="c29a7-110">**IAgentCommandWindow:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="c29a7-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 




