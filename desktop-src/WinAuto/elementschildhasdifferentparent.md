---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292853"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="f1ad9-103">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="f1ad9-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="f1ad9-104">Texto</span><span class="sxs-lookup"><span data-stu-id="f1ad9-104">Text</span></span>

<span data-ttu-id="f1ad9-105">O filho do elemento ( {0} ) tem um elemento pai ( {1} ) diferente</span><span class="sxs-lookup"><span data-stu-id="f1ad9-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="f1ad9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1ad9-106">Type</span></span>

<span data-ttu-id="f1ad9-107">Erro</span><span class="sxs-lookup"><span data-stu-id="f1ad9-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f1ad9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1ad9-108">Description</span></span>

<span data-ttu-id="f1ad9-109">Esse erro indica que, quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado nos filhos do elemento Target, os filhos não relatam um pai consistente.</span><span class="sxs-lookup"><span data-stu-id="f1ad9-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![um exemplo dos filhos de um elemento que relata um pai inconsistente](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="f1ad9-111">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="f1ad9-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f1ad9-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="f1ad9-112">Possible causes</span></span>

<span data-ttu-id="f1ad9-113">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="f1ad9-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1ad9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1ad9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1ad9-115">**AccessibleChildren**</span><span class="sxs-lookup"><span data-stu-id="f1ad9-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




