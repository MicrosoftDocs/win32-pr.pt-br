---
title: Alça de tamanho (referência de elemento de interface do usuário do MSAA)
description: A alça de tamanho é um ponteiro especial do mouse no canto inferior direito de uma janela que permite que um usuário clique e arraste a alça de tamanho para redimensionar a janela.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637113"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="0c5f4-103">Alça de tamanho (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="0c5f4-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="0c5f4-104">A alça de tamanho é um ponteiro especial do mouse no canto inferior direito de uma janela que permite que um usuário clique e arraste a alça de tamanho para redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="0c5f4-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="0c5f4-105">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="0c5f4-105">IAccessible Methods</span></span>

<span data-ttu-id="0c5f4-106">A alça de tamanho dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="0c5f4-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="0c5f4-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="0c5f4-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="0c5f4-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="0c5f4-110">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="0c5f4-110">IAccessible Properties</span></span>

<span data-ttu-id="0c5f4-111">A alça de tamanho dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="0c5f4-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="0c5f4-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0c5f4-112">Property</span></span>                                                                   | <span data-ttu-id="0c5f4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c5f4-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c5f4-114">**obter \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="0c5f4-115">A propriedade **Description** é "pode ser usada para redimensionar a largura e a altura de uma janela".</span><span class="sxs-lookup"><span data-stu-id="0c5f4-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="0c5f4-116">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="0c5f4-117">A propriedade **nome** é "tamanho da caixa".</span><span class="sxs-lookup"><span data-stu-id="0c5f4-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="0c5f4-118">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="0c5f4-119">A janela que contém a alça de tamanho.</span><span class="sxs-lookup"><span data-stu-id="0c5f4-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="0c5f4-120">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="0c5f4-121">A propriedade **role** é [**\_ \_ alça do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0c5f4-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="0c5f4-122">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="0c5f4-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="0c5f4-123">O valor da propriedade de **estado** é zero, o que significa que o objeto está visível ou o [**estado do sistema é \_ \_ invisível**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0c5f4-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0c5f4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c5f4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c5f4-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="0c5f4-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




