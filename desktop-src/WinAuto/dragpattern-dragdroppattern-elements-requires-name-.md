---
title: Os elementos DragPattern/DragDropPattern exigem o nome
description: Os elementos DragPattern/DragDropPattern exigem o nome
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105772992"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="63a70-103">Os elementos DragPattern/DragDropPattern exigem o nome</span><span class="sxs-lookup"><span data-stu-id="63a70-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="63a70-104">Texto</span><span class="sxs-lookup"><span data-stu-id="63a70-104">Text</span></span>

<span data-ttu-id="63a70-105">Elementos que oferecem suporte a arrastar/soltar devem ter um ' name ' válido definido</span><span class="sxs-lookup"><span data-stu-id="63a70-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="63a70-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="63a70-106">Type</span></span>

<span data-ttu-id="63a70-107">Erro</span><span class="sxs-lookup"><span data-stu-id="63a70-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="63a70-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="63a70-108">Description</span></span>

<span data-ttu-id="63a70-109">O elemento dá suporte a [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou a [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mas não tem um nome válido definido.</span><span class="sxs-lookup"><span data-stu-id="63a70-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="63a70-110">Esse problema causa problemas para as pessoas que dependem de um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="63a70-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="63a70-111">O usuário não conseguirá dizer qual é esse objeto, pois a tela de leitura não lerá um nome válido para distinguir o que é esse elemento ao arrastar.</span><span class="sxs-lookup"><span data-stu-id="63a70-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="63a70-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="63a70-112">Possible causes</span></span>

-   <span data-ttu-id="63a70-113">O elemento, ou seu pai, tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="63a70-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="63a70-114">Um desenvolvedor não está ciente de que leitores de tela lêem nomes e tipos de controle.</span><span class="sxs-lookup"><span data-stu-id="63a70-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a70-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63a70-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a70-116">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="63a70-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="63a70-117">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="63a70-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="63a70-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="63a70-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="63a70-119">**IUIAutomationElement:: CurrentName**</span><span class="sxs-lookup"><span data-stu-id="63a70-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




