---
title: IAgentPropertySheet setVisible
description: IAgentPropertySheet setVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807831"
---
# <a name="iagentpropertysheetsetvisible"></a><span data-ttu-id="2fbc1-103">IAgentPropertySheet:: setVisible</span><span class="sxs-lookup"><span data-stu-id="2fbc1-103">IAgentPropertySheet::SetVisible</span></span>

<span data-ttu-id="2fbc1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2fbc1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

<span data-ttu-id="2fbc1-105">Define a propriedade [**Visible**](visible-property.md) para a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2fbc1-105">Sets the [**Visible**](visible-property.md) property for the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="2fbc1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2fbc1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2fbc1-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="2fbc1-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2fbc1-108">Configuração da propriedade visível.</span><span class="sxs-lookup"><span data-stu-id="2fbc1-108">Visible property setting.</span></span> <span data-ttu-id="2fbc1-109">Um valor **true** exibe a folha de propriedades; um valor de **false** oculta-o.</span><span class="sxs-lookup"><span data-stu-id="2fbc1-109">A value of **True** displays the property sheet; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2fbc1-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2fbc1-110">See Also</span></span>

[<span data-ttu-id="2fbc1-111">**IAgentPropertySheet:: getVisible**</span><span class="sxs-lookup"><span data-stu-id="2fbc1-111">**IAgentPropertySheet::GetVisible**</span></span>](iagentpropertysheet--getvisible.md)


 

 




