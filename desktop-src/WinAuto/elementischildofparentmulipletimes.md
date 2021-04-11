---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160506"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="bbbc6-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="bbbc6-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="bbbc6-104">Texto</span><span class="sxs-lookup"><span data-stu-id="bbbc6-104">Text</span></span>

<span data-ttu-id="bbbc6-105">AccParent do elemento é ( {0} ), mas o elemento original é um {1} período filho</span><span class="sxs-lookup"><span data-stu-id="bbbc6-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="bbbc6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbbc6-106">Type</span></span>

<span data-ttu-id="bbbc6-107">Erro</span><span class="sxs-lookup"><span data-stu-id="bbbc6-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="bbbc6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbbc6-108">Description</span></span>

<span data-ttu-id="bbbc6-109">Quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado no elemento de destino, ele relata ser filho do mesmo pai várias vezes.</span><span class="sxs-lookup"><span data-stu-id="bbbc6-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="bbbc6-110">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="bbbc6-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bbbc6-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="bbbc6-111">Possible causes</span></span>

<span data-ttu-id="bbbc6-112">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="bbbc6-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbbc6-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbbc6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbbc6-114">**IAccessible:: obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="bbbc6-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




