---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120741"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="fae14-103">IAgentPropertySheet:: SetPage</span><span class="sxs-lookup"><span data-stu-id="fae14-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="fae14-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fae14-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="fae14-105">Define a página atual da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fae14-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="fae14-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fae14-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fae14-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="fae14-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="fae14-108">Um BSTR que define a página atual da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fae14-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="fae14-109">O parâmetro pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="fae14-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="fae14-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fae14-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="fae14-111">**Palestra**</span><span class="sxs-lookup"><span data-stu-id="fae14-111">**"Speech"**</span></span>    | <span data-ttu-id="fae14-112">A página de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="fae14-112">The Speech Input page.</span></span> |
| <span data-ttu-id="fae14-113">**Der**</span><span class="sxs-lookup"><span data-stu-id="fae14-113">**"Output"**</span></span>    | <span data-ttu-id="fae14-114">A página saída.</span><span class="sxs-lookup"><span data-stu-id="fae14-114">The Output page.</span></span>       |
| <span data-ttu-id="fae14-115">**Internacionais**</span><span class="sxs-lookup"><span data-stu-id="fae14-115">**"Copyright"**</span></span> | <span data-ttu-id="fae14-116">A página de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="fae14-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fae14-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fae14-117">See Also</span></span>

[<span data-ttu-id="fae14-118">**IAgentPropertySheet:: GetPage**</span><span class="sxs-lookup"><span data-stu-id="fae14-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




