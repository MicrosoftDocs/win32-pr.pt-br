---
title: Tela e interfaces visuais do XPS OM
description: Este tópico descreve como usar as interfaces relacionadas à tela da API de documento XPS em um OM XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8bd15333c2786801900b09b32eb6cd59121af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761000"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="dae0f-103">Trabalhando com interfaces visuais e telas do XPS OM</span><span class="sxs-lookup"><span data-stu-id="dae0f-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="dae0f-104">Este tópico descreve como usar as interfaces relacionadas à tela da API de documento XPS em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="dae0f-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="dae0f-105">Nome da interface</span><span class="sxs-lookup"><span data-stu-id="dae0f-105">Interface name</span></span>                                  | <span data-ttu-id="dae0f-106">Interfaces filho lógicas</span><span class="sxs-lookup"><span data-stu-id="dae0f-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="dae0f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dae0f-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dae0f-108">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="dae0f-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="dae0f-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="dae0f-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="dae0f-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="dae0f-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="dae0f-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="dae0f-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="dae0f-112">A classe base das interfaces que definem objetos visuais, como texto e elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="dae0f-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="dae0f-113">Os objetos visuais podem ser coletados em uma interface [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .</span><span class="sxs-lookup"><span data-stu-id="dae0f-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="dae0f-114">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="dae0f-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="dae0f-115">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="dae0f-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="dae0f-116">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="dae0f-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="dae0f-117">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="dae0f-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="dae0f-118">Uma coleção de objetos visuais que pode ser tratada como um único objeto visual.</span><span class="sxs-lookup"><span data-stu-id="dae0f-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |
<span data-ttu-id="dae0f-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) é a interface base; os objetos visíveis de uma página herdam dele.</span><span class="sxs-lookup"><span data-stu-id="dae0f-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="dae0f-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) herda de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) e permite que muitos outros elementos visuais sejam agrupados e tratados como um único elemento visual.</span><span class="sxs-lookup"><span data-stu-id="dae0f-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="dae0f-121">Por exemplo, você pode usar uma interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para criar uma faixa de página que contém uma coleção de texto e elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="dae0f-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="dae0f-122">Essa faixa pode conter um logotipo, o slogan da empresa e o endereço da empresa.</span><span class="sxs-lookup"><span data-stu-id="dae0f-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="dae0f-123">Você poderia posicionar todos esses elementos no [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) de uma interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) e, em seguida, aplicar uma única transformação ao objeto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para redimensioná-lo para uma página específica.</span><span class="sxs-lookup"><span data-stu-id="dae0f-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="dae0f-124">Isso é muito mais simples do que a computação e a aplicação de uma transformação a cada componente Visual individual na faixa.</span><span class="sxs-lookup"><span data-stu-id="dae0f-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="dae0f-125">Você também pode usar uma tela para redimensionar o conteúdo da página de acordo com o tamanho da página atual.</span><span class="sxs-lookup"><span data-stu-id="dae0f-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="dae0f-126">Para fazer isso, coloque todo o conteúdo da página em uma única tela e aplique a transformação apropriada para ajustar a tela ao tamanho da página atual.</span><span class="sxs-lookup"><span data-stu-id="dae0f-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="dae0f-127">Isso também é muito mais simples do que tentar redimensionar cada elemento visual na coleção de visuais na página.</span><span class="sxs-lookup"><span data-stu-id="dae0f-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="dae0f-128">Mover o conteúdo da página para uma tela</span><span class="sxs-lookup"><span data-stu-id="dae0f-128">Move page contents to a canvas</span></span>

<span data-ttu-id="dae0f-129">O exemplo de código a seguir move o conteúdo de uma página para uma tela.</span><span class="sxs-lookup"><span data-stu-id="dae0f-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="dae0f-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dae0f-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="dae0f-131">Interface <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="dae0f-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
