---
title: Inconsistent, inconsistent
description: Inconsistent, inconsistent
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635311"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="910a0-103">Inconsistent, inconsistent</span><span class="sxs-lookup"><span data-stu-id="910a0-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="910a0-104">Texto</span><span class="sxs-lookup"><span data-stu-id="910a0-104">Text</span></span>

<span data-ttu-id="910a0-105">Um controle tem Estados/propriedades que são inconsistentes {0} e {1}</span><span class="sxs-lookup"><span data-stu-id="910a0-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="910a0-106">Type</span><span class="sxs-lookup"><span data-stu-id="910a0-106">Type</span></span>

<span data-ttu-id="910a0-107">Erro</span><span class="sxs-lookup"><span data-stu-id="910a0-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="910a0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="910a0-108">Description</span></span>

<span data-ttu-id="910a0-109">Um elemento está relatando Estados de MSAA inconsistentes ou conflitantes ou propriedades de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="910a0-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="910a0-110">Por exemplo, quando o método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) retorna qualquer uma das combinações a seguir.</span><span class="sxs-lookup"><span data-stu-id="910a0-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="910a0-111">\_Sistema \_ de estado expandido e sistema de estado \_ \_ recolhido</span><span class="sxs-lookup"><span data-stu-id="910a0-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="910a0-112">\_Sistema \_ de estado selecionado e não \_ sistema de estado \_ selecionável</span><span class="sxs-lookup"><span data-stu-id="910a0-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="910a0-113">Estado do sistema com foco \_ \_ e não estado do \_ sistema \_</span><span class="sxs-lookup"><span data-stu-id="910a0-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="910a0-114">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um estado de elemento incorreto pode ser relatado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="910a0-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="910a0-115">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="910a0-115">Possible causes</span></span>

<span data-ttu-id="910a0-116">O elemento ou seu pai tem um estado de MSAA definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="910a0-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="910a0-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="910a0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="910a0-118">**IAccessible:: obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="910a0-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="910a0-119">**Constantes de estado do objeto**</span><span class="sxs-lookup"><span data-stu-id="910a0-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="910a0-120">Estados e propriedades</span><span class="sxs-lookup"><span data-stu-id="910a0-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




