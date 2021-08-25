---
description: Este tópico fornece um exemplo de uso de gradientes em um OM XPS.
ms.assetid: c58c9e5a-c871-4b44-a1be-0aceafa2f805
title: Gradientes de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267d053ef0e9b98408119870cb723ceb1170d4905aab81b0dc3db7969c356c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823606"
---
# <a name="xps-om-gradients"></a>Gradientes de OM XPS

Este tópico fornece um exemplo de uso de gradientes em um OM XPS.

## <a name="add-a-new-stop-to-an-existing-gradient"></a>Adicionar uma nova parada a um gradiente existente

O exemplo de código a seguir adiciona uma nova parada ao gradiente de um pincel de gradiente linear.


```C++
    // brush is the pointer to the gradient brush that will get 
    //  the new gradient and is initialized outside of this code example

    // this is the start of the method that updates the brush
    HRESULT                           hr = S_OK;
    XPS_COLOR                         xpsColorStop;
    IXpsOMGradientStopCollection      *stops;
    IXpsOMGradientStop                *xpsNewGradientStop = NULL, *thisStop = NULL, *nextStop = NULL;
    UINT32                            thisStopIdx, numStops;
    FLOAT                             thisStopOffset, nextStopOffset, newStopOffset;
    BOOL                              bUpdated = FALSE;

    // define the new stop color to be yellow
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xFF;
    xpsColorStop.value.sRGB.green = 0xFF;
    xpsColorStop.value.sRGB.blue  = 0x00;
    
    // create a new gradient stop by setting the color and location 
    // this stop will be half way between the start and end point
    newStopOffset = 0.5f;
    hr = xpsFactory->CreateGradientStop(&xpsColorStop, NULL, newStopOffset, &xpsNewGradientStop);

    // get the collection of gradient stops from the brush
    hr = brush->GetGradientStops (&stops);

    hr = stops->GetCount (&numStops);
    // there will never be less than two stops
    
    // insert the new stop so that the stops are sorted by offset
    // if an existing stop has the same offset as the new one,
    // overwrite the existing stop with the new stop.
    for (thisStopIdx = 0; thisStopIdx < (numStops-1); thisStopIdx++) {
        hr = stops->GetAt(thisStopIdx, &thisStop);
        hr = stops->GetAt(thisStopIdx+1, &nextStop);
    
        hr = thisStop->GetOffset (&thisStopOffset);
        hr = nextStop->GetOffset (&nextStopOffset);

        if (newStopOffset < thisStopOffset) {
            // insert at thisStopIdx
            stops->InsertAt(thisStopIdx, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        } 
        if ((newStopOffset > thisStopOffset) && (newStopOffset < nextStopOffset)) {
            // the new stop goes in between them
            stops->InsertAt (thisStopIdx+1, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        } 

        if (newStopOffset == thisStopOffset ) {
            // then overwrite the old one
            stops->SetAt (thisStopIdx, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        }

        if (newStopOffset == nextStopOffset ) {
            // then overwrite the old one
            stops->SetAt (thisStopIdx+1, xpsNewGradientStop);
            bUpdated = TRUE;
            break; // done, so leave loop
        }

        // on the last entry, see if this stop is greater than the last entry
        // in the collection. If so, append the new one to the end.
        if ((thisStopIdx == (numStops-2)) && (newStopOffset > nextStopOffset )) {
            // then overwrite the old one
            stops->Append ( xpsNewGradientStop );
            bUpdated = TRUE;
            break; // done, so leave loop
        }
        if (NULL != thisStop) {thisStop->Release(); thisStop = NULL;}
        if (NULL != nextStop) {nextStop->Release(); nextStop = NULL;}
    }
    if (NULL != thisStop) {thisStop->Release(); thisStop = NULL;}
    if (NULL != nextStop) {nextStop->Release(); nextStop = NULL;}

    // make sure that the new stop was put somewhere in the collection
    _ASSERT (bUpdated);
    return S_OK;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IXpsOMGradientStop Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)
</dt> <dt>

[**IXpsOMGradientStopCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)
</dt> </dl>

 

 



