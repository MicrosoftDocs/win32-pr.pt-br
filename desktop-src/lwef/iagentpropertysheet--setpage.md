---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636186"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="604dc-103">IAgentPropertySheet:: SetPage</span><span class="sxs-lookup"><span data-stu-id="604dc-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="604dc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="604dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="604dc-105">Define a página atual da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="604dc-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="604dc-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="604dc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="604dc-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="604dc-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="604dc-108">Um BSTR que define a página atual da propriedade.</span><span class="sxs-lookup"><span data-stu-id="604dc-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="604dc-109">O parâmetro pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="604dc-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="604dc-110">**Palestra**</span><span class="sxs-lookup"><span data-stu-id="604dc-110">**"Speech"**</span></span>    | <span data-ttu-id="604dc-111">A página de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="604dc-111">The Speech Input page.</span></span> |
| <span data-ttu-id="604dc-112">**Der**</span><span class="sxs-lookup"><span data-stu-id="604dc-112">**"Output"**</span></span>    | <span data-ttu-id="604dc-113">A página saída.</span><span class="sxs-lookup"><span data-stu-id="604dc-113">The Output page.</span></span>       |
| <span data-ttu-id="604dc-114">**Internacionais**</span><span class="sxs-lookup"><span data-stu-id="604dc-114">**"Copyright"**</span></span> | <span data-ttu-id="604dc-115">A página de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="604dc-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="604dc-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="604dc-116">See Also</span></span>

[<span data-ttu-id="604dc-117">**IAgentPropertySheet:: GetPage**</span><span class="sxs-lookup"><span data-stu-id="604dc-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




