---
description: Filtros de driver de classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtros de driver de classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827527"
---
# <a name="wdm-class-driver-filters"></a>Filtros de driver de classe WDM

Se um dispositivo de captura usar um driver de Windows Driver Model (WDM), o grafo poderá exigir certos filtros upstream do filtro de captura. Esses filtros são chamados de filtros de driver de classe de fluxo ou filtros WDM. Eles dão suporte a funcionalidades adicionais fornecidas pelo hardware. Por exemplo, um cartão sintonizador de TV tem funções para definir o canal. O filtro correspondente é o filtro de [sintonizador de TV](tv-tuner-filter.md) , que expõe a interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . Para disponibilizar essa funcionalidade para o aplicativo, você deve conectar o filtro de sintonizador de TV ao filtro de captura.

A interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fornece a maneira mais fácil de adicionar filtros WDM ao grafo. Em algum momento, ao criar o grafo, chame [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ou [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Qualquer um desses métodos localizará automaticamente os filtros WDM necessários e os conectará ao filtro de captura. O restante desta seção descreve como adicionar filtros WDM manualmente. No entanto, lembre-se de que a abordagem recomendada é simplesmente chamar um desses métodos **ICaptureGraphBuilder2** .

Os Pins em um filtro WDM dão suporte a um ou mais meios. Um meio define um método de comunicação, como um barramento. Você deve conectar Pins que dão suporte à mesma mídia. A estrutura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , que é equivalente à estrutura **\_ média KSPIN** usada para drivers de streaming de kernel, define um meio no DirectShow. O membro **clsMedium** da estrutura **REGPINMEDIUM** especifica o identificador de classe (CLSID) para a mídia. Para recuperar a mídia de um PIN, chame o método [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) . Esse método retorna um ponteiro para um bloco de memória que contém uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) , seguida por zero ou mais estruturas **REGPINMEDIUM** . Cada estrutura **REGPINMEDIUM** identifica um meio ao qual o PIN dá suporte.

Não conecte um PIN se o meio tiver um CLSID de GUID \_ NULL ou KSMEDIUMSETID \_ standard. Esses são valores padrão que indicam que o PIN não oferece suporte a meios.

Além disso, não conecte um PIN, a menos que o filtro exija exatamente uma instância conectada desse PIN. Caso contrário, seu aplicativo pode tentar conectar vários Pins que não devem ter conexões, o que pode fazer com que o programa pare de responder. Para descobrir o número de instâncias necessárias, recupere o conjunto de \_ Propriedades do KSPROPERTY PIN \_ NECESSARYINSTANCES, conforme mostrado no exemplo de código a seguir. (Para fins de brevidade, este exemplo não testa nenhum código de retorno nem libera interfaces. O aplicativo deve fazer ambos, é claro.)


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



O pseudocódigo a seguir é uma estrutura de tópicos extremamente breve que mostra como localizar e conectar os filtros WDM. Ele omite muitos detalhes e tem o objetivo de mostrar as etapas gerais que seu aplicativo precisaria executar.


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> </dl>

 

 



