---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364071"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="7dd35-103">IAgentPropertySheet:: GetPage</span><span class="sxs-lookup"><span data-stu-id="7dd35-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="7dd35-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7dd35-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="7dd35-105">Recupera a página atual da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7dd35-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="7dd35-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7dd35-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7dd35-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="7dd35-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="7dd35-108">Endereço de uma variável que recebe a página atual da folha de Propriedades (última página exibida se a janela não estiver aberta).</span><span class="sxs-lookup"><span data-stu-id="7dd35-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="7dd35-109">O parâmetro pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7dd35-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="7dd35-110">**Palestra**</span><span class="sxs-lookup"><span data-stu-id="7dd35-110">**"Speech"**</span></span>    | <span data-ttu-id="7dd35-111">A página de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="7dd35-111">The Speech Input page.</span></span> |
| <span data-ttu-id="7dd35-112">**Der**</span><span class="sxs-lookup"><span data-stu-id="7dd35-112">**"Output"**</span></span>    | <span data-ttu-id="7dd35-113">A página saída.</span><span class="sxs-lookup"><span data-stu-id="7dd35-113">The Output page.</span></span>       |
| <span data-ttu-id="7dd35-114">**Internacionais**</span><span class="sxs-lookup"><span data-stu-id="7dd35-114">**"Copyright"**</span></span> | <span data-ttu-id="7dd35-115">A página de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="7dd35-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7dd35-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7dd35-116">See Also</span></span>

[<span data-ttu-id="7dd35-117">**IAgentPropertySheet:: SetPage**</span><span class="sxs-lookup"><span data-stu-id="7dd35-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




