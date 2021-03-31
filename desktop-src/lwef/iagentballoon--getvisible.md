---
title: IAgentBalloon getVisible
description: IAgentBalloon getVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822997"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="f024c-103">IAgentBalloon:: getVisible</span><span class="sxs-lookup"><span data-stu-id="f024c-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="f024c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f024c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="f024c-105">Determina se o balão de palavra está visível ou oculto.</span><span class="sxs-lookup"><span data-stu-id="f024c-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="f024c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f024c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f024c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="f024c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="f024c-108">Endereço de uma variável que recebe **true** se a palavra balão estiver visível e **false** se estiver oculta.</span><span class="sxs-lookup"><span data-stu-id="f024c-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f024c-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f024c-109">See Also</span></span>

[<span data-ttu-id="f024c-110">**IAgentBalloon:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="f024c-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




