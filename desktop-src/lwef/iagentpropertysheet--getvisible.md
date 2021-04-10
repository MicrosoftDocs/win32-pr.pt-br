---
title: IAgentPropertySheet getVisible
description: IAgentPropertySheet getVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292276"
---
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="f54bb-103">IAgentPropertySheet:: getVisible</span><span class="sxs-lookup"><span data-stu-id="f54bb-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="f54bb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f54bb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="f54bb-105">Determina se a folha de propriedades do Microsoft Agent está visível ou oculta.</span><span class="sxs-lookup"><span data-stu-id="f54bb-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="f54bb-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f54bb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f54bb-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="f54bb-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="f54bb-108">Endereço de uma variável que recebe **true** se a folha de propriedades estiver visível e **false** se estiver oculta.</span><span class="sxs-lookup"><span data-stu-id="f54bb-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f54bb-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f54bb-109">See Also</span></span>

[<span data-ttu-id="f54bb-110">**IAgentPropertySheet:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="f54bb-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




