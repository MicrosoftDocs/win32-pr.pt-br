---
description: Este tópico descreve como usar as interfaces de nível de página que fornecem acesso ao conteúdo de uma página em um OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Trabalhando com interfaces de página de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764049"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="2714a-103">Trabalhando com interfaces de página de OM XPS</span><span class="sxs-lookup"><span data-stu-id="2714a-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="2714a-104">Este tópico descreve como usar as interfaces de nível de página que fornecem acesso ao conteúdo de uma página em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="2714a-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="2714a-105">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="2714a-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="2714a-106">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="2714a-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="2714a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2714a-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2714a-108">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="2714a-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="2714a-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="2714a-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="2714a-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="2714a-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="2714a-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="2714a-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="2714a-112">O objeto raiz do conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="2714a-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="2714a-113">Esse objeto representa uma parte do documento.</span><span class="sxs-lookup"><span data-stu-id="2714a-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="2714a-114">**IXpsOMShareable**</span><span class="sxs-lookup"><span data-stu-id="2714a-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="2714a-115">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="2714a-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="2714a-116">**IXpsOMMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="2714a-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="2714a-117">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="2714a-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="2714a-118">**IXpsOMBrush**</span><span class="sxs-lookup"><span data-stu-id="2714a-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="2714a-119">As interfaces que derivam da interface [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) podem ser armazenadas em um dicionário de recursos e compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="2714a-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="2714a-120">**IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="2714a-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="2714a-121">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="2714a-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="2714a-122">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="2714a-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="2714a-123">Contém um dicionário de recursos.</span><span class="sxs-lookup"><span data-stu-id="2714a-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="2714a-124">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="2714a-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="2714a-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2714a-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="2714a-126">Faz referência aos recursos que são compartilhados por outros objetos.</span><span class="sxs-lookup"><span data-stu-id="2714a-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="2714a-127">**IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="2714a-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="2714a-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2714a-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="2714a-129">Fornece acesso ao conteúdo do fluxo de recursos da parte StoryFragments do documento.</span><span class="sxs-lookup"><span data-stu-id="2714a-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="2714a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2714a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2714a-131">**Interface IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="2714a-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="2714a-132">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="2714a-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="2714a-133">**Interface IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="2714a-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="2714a-134">**Interface IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="2714a-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="2714a-135">**Interface IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="2714a-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="2714a-136">**Interface IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="2714a-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




