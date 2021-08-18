---
title: Tela xps OM e interfaces visuais
description: Este tópico descreve como usar as interfaces relacionadas à tela da API de Documento XPS em um OM XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f7214a06779d997331f57a22ae29217e5cabdd635d0c3feac85bd8a3070065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469265"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Trabalhando com interfaces visuais e tela do OM XPS

Este tópico descreve como usar as interfaces relacionadas à tela da API de Documento XPS em um OM XPS.

| Nome da interface                                  | Interfaces filho lógicas                                                                                                                    | Descrição                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | A classe base das interfaces que definem objetos visuais, como texto e elementos gráficos.<br/> Objetos visuais podem ser coletados em uma interface [**IXpsOMVisualCollection.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Uma coleção de objetos visuais que podem ser tratados como um único objeto visual.<br/>                                                                                                                                |

[**IXpsOMVisual é**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) a interface base; os objetos visíveis de uma página herdam dela. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) herda de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) e permite que muitos outros elementos visuais sejam agrupados e agidos como um único elemento visual. Por exemplo, você pode usar uma interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para criar uma faixa de página que contém uma coleção de texto e elementos gráficos. Essa faixa pode conter um logotipo, o logotipo da empresa e o endereço da empresa. Você pode colocar todos esses elementos na [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) de uma interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) e, em seguida, aplicar uma única transformação ao objeto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) para reeslizá-la em uma página específica. Isso é muito mais simples do que computar e aplicar uma transformação a cada componente visual individual na faixa.

Você também pode usar uma tela para reescala o conteúdo da página para se ajustar ao tamanho atual da página. Para fazer isso, coloque todo o conteúdo da página em uma única tela e aplique a transformação apropriada para ajustar a tela ao tamanho atual da página. Isso também é muito mais simples do que tentar reorganizar cada elemento visual na coleção de visuais na página.

## <a name="move-page-contents-to-a-canvas"></a>Mover o conteúdo da página para uma tela

O exemplo de código a seguir move o conteúdo de uma página para uma tela.

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> 
  <dt>[**Interface IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
