---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119861"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="47ee2-103">IAgentPropertySheet:: GetPage</span><span class="sxs-lookup"><span data-stu-id="47ee2-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="47ee2-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47ee2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="47ee2-105">Recupera a página atual da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="47ee2-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="47ee2-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47ee2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="47ee2-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="47ee2-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="47ee2-108">Endereço de uma variável que recebe a página atual da folha de Propriedades (última página exibida se a janela não estiver aberta).</span><span class="sxs-lookup"><span data-stu-id="47ee2-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="47ee2-109">O parâmetro pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="47ee2-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="47ee2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="47ee2-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="47ee2-111">**Palestra**</span><span class="sxs-lookup"><span data-stu-id="47ee2-111">**"Speech"**</span></span>    | <span data-ttu-id="47ee2-112">A página de entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="47ee2-112">The Speech Input page.</span></span> |
| <span data-ttu-id="47ee2-113">**Der**</span><span class="sxs-lookup"><span data-stu-id="47ee2-113">**"Output"**</span></span>    | <span data-ttu-id="47ee2-114">A página saída.</span><span class="sxs-lookup"><span data-stu-id="47ee2-114">The Output page.</span></span>       |
| <span data-ttu-id="47ee2-115">**Internacionais**</span><span class="sxs-lookup"><span data-stu-id="47ee2-115">**"Copyright"**</span></span> | <span data-ttu-id="47ee2-116">A página de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="47ee2-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="47ee2-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="47ee2-117">See Also</span></span>

[<span data-ttu-id="47ee2-118">**IAgentPropertySheet:: SetPage**</span><span class="sxs-lookup"><span data-stu-id="47ee2-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




