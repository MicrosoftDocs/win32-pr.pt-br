---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292756"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a><span data-ttu-id="f07d7-103">AccessibleObjectFromPointReturnedNullIAccessible</span><span class="sxs-lookup"><span data-stu-id="f07d7-103">AccessibleObjectFromPointReturnedNullIAccessible</span></span>

## <a name="text"></a><span data-ttu-id="f07d7-104">Texto</span><span class="sxs-lookup"><span data-stu-id="f07d7-104">Text</span></span>

<span data-ttu-id="f07d7-105">AccessibleObjectFromPoint ( {0} , {1} ) retornou NULL</span><span class="sxs-lookup"><span data-stu-id="f07d7-105">AccessibleObjectFromPoint({0}, {1}) returned null</span></span>

## <a name="type"></a><span data-ttu-id="f07d7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f07d7-106">Type</span></span>

<span data-ttu-id="f07d7-107">Erro</span><span class="sxs-lookup"><span data-stu-id="f07d7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f07d7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f07d7-108">Description</span></span>

<span data-ttu-id="f07d7-109">O endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do elemento de interface do usuário obtida para as coordenadas fornecidas é nulo.</span><span class="sxs-lookup"><span data-stu-id="f07d7-109">The address of the UI element's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is NULL.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f07d7-110">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="f07d7-110">Possible causes</span></span>

-   <span data-ttu-id="f07d7-111">A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.</span><span class="sxs-lookup"><span data-stu-id="f07d7-111">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="f07d7-112">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="f07d7-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f07d7-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f07d7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f07d7-114">Navegação por meio de teste de clique e local da tela</span><span class="sxs-lookup"><span data-stu-id="f07d7-114">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="f07d7-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="f07d7-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




