---
title: Erro de estrutura de grade do ARIA
description: Erro de estrutura de grade do ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642923"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="8349e-104">Erro de estrutura de grade do ARIA</span><span class="sxs-lookup"><span data-stu-id="8349e-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="8349e-105">Texto</span><span class="sxs-lookup"><span data-stu-id="8349e-105">Text</span></span>

<span data-ttu-id="8349e-106">O elemento com a função **Grid** não tem uma estrutura de grade ou marcação acessível correspondente.</span><span class="sxs-lookup"><span data-stu-id="8349e-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="8349e-107">Type</span><span class="sxs-lookup"><span data-stu-id="8349e-107">Type</span></span>

<span data-ttu-id="8349e-108">Erro</span><span class="sxs-lookup"><span data-stu-id="8349e-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="8349e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8349e-109">Description</span></span>

<span data-ttu-id="8349e-110">Esse erro se aplica a elementos personalizados que têm o atributo **role** definido como "Grid".</span><span class="sxs-lookup"><span data-stu-id="8349e-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="8349e-111">Ele não se aplica a marcas de tabela HTML que têm uma **função** implícita de "Grid".</span><span class="sxs-lookup"><span data-stu-id="8349e-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="8349e-112">Um elemento que tem seu atributo de **função** definido como "grade" deve ter a estrutura definida pela função de grade WAI-ARIA (aplicativos de Internet avançados) acessíveis, incluindo o nome acessível para a grade e seus subelementos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8349e-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="8349e-113">Para corrigir esse erro, examine sua implementação para garantir que ela esteja em conformidade com a especificação WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="8349e-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="8349e-114">Especificamente, verifique se a estrutura atende às regras a seguir.</span><span class="sxs-lookup"><span data-stu-id="8349e-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="8349e-115">a **grade** contém elementos **Row** ou **rowgroup** .</span><span class="sxs-lookup"><span data-stu-id="8349e-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="8349e-116">**rowgroup** contém elementos de **linha** .</span><span class="sxs-lookup"><span data-stu-id="8349e-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="8349e-117">os **elementos de** **linha** contêm elementos **ColumnHeader** ou **gridcell** ou rowgroup.</span><span class="sxs-lookup"><span data-stu-id="8349e-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="8349e-118">Um nome acessível deve ser definido para os elementos **Grid**, **ColumnHeader**, **gridcell** e **multiheader** usando um dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8349e-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="8349e-119">atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para referenciar o elemento que contém o texto.</span><span class="sxs-lookup"><span data-stu-id="8349e-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="8349e-120">atributo [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para definir o nome acessível diretamente.</span><span class="sxs-lookup"><span data-stu-id="8349e-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="8349e-121">[**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) para criar uma dica de ferramenta que é ao mesmo tempo usada como um nome.</span><span class="sxs-lookup"><span data-stu-id="8349e-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




