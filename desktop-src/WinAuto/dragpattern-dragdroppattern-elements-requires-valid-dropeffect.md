---
title: Os elementos DragPattern/DragDropPattern exigem DropEffect válidos
description: Os elementos DragPattern/DragDropPattern exigem DropEffect válidos
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634790"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="e979e-103">Os elementos DragPattern/DragDropPattern exigem DropEffect válidos</span><span class="sxs-lookup"><span data-stu-id="e979e-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="e979e-104">Texto</span><span class="sxs-lookup"><span data-stu-id="e979e-104">Text</span></span>

<span data-ttu-id="e979e-105">Elementos que oferecem suporte a arrastar/soltar devem ter um conjunto ' DropEffect ' válido</span><span class="sxs-lookup"><span data-stu-id="e979e-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="e979e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e979e-106">Type</span></span>

<span data-ttu-id="e979e-107">Erro</span><span class="sxs-lookup"><span data-stu-id="e979e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="e979e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e979e-108">Description</span></span>

<span data-ttu-id="e979e-109">O elemento dá suporte a [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou a [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mas não tem um conjunto de propriedades [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) válido.</span><span class="sxs-lookup"><span data-stu-id="e979e-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="e979e-110">Esse problema causa problemas para as pessoas que dependem de um leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="e979e-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="e979e-111">O usuário não poderá informar o efeito que esse objeto tem ao arrastar.</span><span class="sxs-lookup"><span data-stu-id="e979e-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e979e-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="e979e-112">Possible causes</span></span>

-   <span data-ttu-id="e979e-113">O elemento, ou seu pai, não criou [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ou [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="e979e-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="e979e-114">Um desenvolvedor não está ciente de que os leitores de tela lêem DropEffect (s).</span><span class="sxs-lookup"><span data-stu-id="e979e-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




