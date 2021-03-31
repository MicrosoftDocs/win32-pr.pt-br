---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637239"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="3f87c-103">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="3f87c-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="3f87c-104">Texto</span><span class="sxs-lookup"><span data-stu-id="3f87c-104">Text</span></span>

<span data-ttu-id="3f87c-105">O nome irmão duplicado + role "" causará \\ {0} \\ ambiguidade entre os elementos.</span><span class="sxs-lookup"><span data-stu-id="3f87c-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="3f87c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f87c-106">Type</span></span>

<span data-ttu-id="3f87c-107">Erro</span><span class="sxs-lookup"><span data-stu-id="3f87c-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="3f87c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f87c-108">Description</span></span>

<span data-ttu-id="3f87c-109">Um elemento tem o mesmo nome e função/ControlType que outro elemento.</span><span class="sxs-lookup"><span data-stu-id="3f87c-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="3f87c-110">Esse problema pode causar confusão porque os leitores de tela lerám o mesmo texto para todos os elementos com o mesmo nome e função/ControlType.</span><span class="sxs-lookup"><span data-stu-id="3f87c-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="3f87c-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="3f87c-111">Possible causes</span></span>

-   <span data-ttu-id="3f87c-112">O nome do elemento contém texto role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="3f87c-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="3f87c-113">O nome do elemento ou o nome de seu pai não está definido ou está definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="3f87c-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f87c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f87c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f87c-115">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="3f87c-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="3f87c-116">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="3f87c-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="3f87c-117">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3f87c-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="3f87c-118">**IUIAutomationElement. CurrentName**</span><span class="sxs-lookup"><span data-stu-id="3f87c-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




