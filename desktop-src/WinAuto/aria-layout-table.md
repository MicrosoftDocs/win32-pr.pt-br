---
title: Erro de tabela de apresentação do ARIA
description: Erro de tabela de apresentação do ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642921"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="d25f3-104">Erro de tabela de apresentação do ARIA</span><span class="sxs-lookup"><span data-stu-id="d25f3-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="d25f3-105">Texto</span><span class="sxs-lookup"><span data-stu-id="d25f3-105">Text</span></span>

<span data-ttu-id="d25f3-106">A tabela usada para layout não deve ter informações de cabeçalho, nome acessível ou resumo definidas (**th**, **Summary**, **Aria-DescribedBy**, **Aria-labelledby**, **Aria-Label**, **title**, atributos de **legenda** ).</span><span class="sxs-lookup"><span data-stu-id="d25f3-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="d25f3-107">Type</span><span class="sxs-lookup"><span data-stu-id="d25f3-107">Type</span></span>

<span data-ttu-id="d25f3-108">Erro</span><span class="sxs-lookup"><span data-stu-id="d25f3-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d25f3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d25f3-109">Description</span></span>

<span data-ttu-id="d25f3-110">Esse erro se aplica a marcas de tabela HTML que têm o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) definido como "Presentation", ou com uma tabela que tem uma única célula (1 × 1 tabela).</span><span class="sxs-lookup"><span data-stu-id="d25f3-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="d25f3-111">Esse erro indica que uma tabela está marcada como somente layout (tem `role="presentation"` ), mas também contém informações de acessibilidade como se fosse uma tabela de dados, o que pode ser confuso para os usuários do leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="d25f3-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="d25f3-112">Para resolver esse erro, determine se a tabela realmente é apenas uma tabela de layout e, em caso afirmativo, remova a marcação acessível:</span><span class="sxs-lookup"><span data-stu-id="d25f3-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="d25f3-113">Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou atributos [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="d25f3-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="d25f3-114">atributos de [**Resumo**](https://www.bing.com/search?q=**summary**) ou [**Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="d25f3-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="d25f3-115">Marcas do [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .</span><span class="sxs-lookup"><span data-stu-id="d25f3-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="d25f3-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d25f3-116">Example</span></span>

![<span data-ttu-id="d25f3-117">HTML para um elemento table, com atributos como resumo que disparam o erro de tabela de apresentação do Aria mostrado como marcação HTML com traço e saída</span><span class="sxs-lookup"><span data-stu-id="d25f3-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="d25f3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d25f3-118">Remarks</span></span>

<span data-ttu-id="d25f3-119">Se você determinar que uma tabela precisa de informações de acessibilidade, remova o atributo de [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) ou defina-o com um valor diferente de "apresentação".</span><span class="sxs-lookup"><span data-stu-id="d25f3-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




