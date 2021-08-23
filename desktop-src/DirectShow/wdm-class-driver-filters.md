---
description: Filtros de driver de classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtros de driver de classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd93db09c638ed7a8a217bec28a565086dcbfcae2b5702c9e1d07778c338646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071890"
---
# <a name="wdm-class-driver-filters"></a>Filtros de driver de classe WDM

Se um dispositivo de captura usar Windows driver WDM (Driver Model), o grafo poderá exigir determinados filtros upstream do filtro de captura. Esses filtros são chamados de filtros de driver de classe de fluxo ou filtros WDM. Eles suportam funcionalidades adicionais fornecidas pelo hardware. Por exemplo, uma placa de ajuste de TV tem funções para definir o canal. O filtro correspondente é o [filtro TV Tuner,](tv-tuner-filter.md) que expõe a interface [**IAMTVTuner.**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) Para disponibilizar essa funcionalidade para o aplicativo, você deve conectar o filtro Tv Tuner ao filtro de captura.

A interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fornece a maneira mais fácil de adicionar filtros WDM ao grafo. Em algum momento, ao criar o grafo, [**chame FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ou [**RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Qualquer um desses métodos localizará automaticamente os filtros de WDM necessários e os conectará ao filtro de captura. O restante desta seção descreve como adicionar filtros WDM manualmente. No entanto, esteja ciente de que a abordagem de recomendação é simplesmente chamar um desses **métodos ICaptureGraphBuilder2.**

Os pinos em um filtro WDM suportam uma ou mais mídias. Uma mídia define um método de comunicação, como um barramento. Você deve conectar pinos que suportam a mesma mídia. A [**estrutura REGPINMEDIUM,**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) que é equivalente à estrutura **KSPIN \_ MEDIUM** usada para drivers de streaming de kernel, define uma mídia em DirectShow. O **membro clsMedium** da estrutura **REGPINMEDIUM** especifica o CLSID (identificador de classe) para o meio. Para recuperar o meio de um pino, chame o [**método IKsPin::KsQueryMediums.**](ikspin-ksquerymediums.md) Esse método retorna um ponteiro para um bloco de memória que contém uma estrutura [**DE \_ ITEM KSMULTIPLE,**](ksmultiple-item.md) seguida por zero ou mais estruturas **REGPINMEDIUM.** Cada **estrutura REGPINMEDIUM** identifica uma mídia compatível com o pino.

Não conecte um pino se a mídia tiver uma CLSID de GUID \_ NULL ou KSMEDIUMSETID \_ Standard. Esses são valores padrão que indicam que o pino não dá suporte a mídias.

Além disso, não conecte um pino, a menos que o filtro exija exatamente uma instância conectada desse pino. Caso contrário, seu aplicativo pode tentar conectar vários pinos que não devem ter conexões, o que pode fazer com que o programa pare de responder. Para descobrir o número de instâncias necessárias, recupere o conjunto de propriedades KSPROPERTY \_ PIN NECESSARYINSTANCES, conforme mostrado no \_ exemplo de código a seguir. (Por brevidade, este exemplo não testa nenhum código de retorno nem libera nenhuma interface. Seu aplicativo deve fazer ambos, é claro.)


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



O pseudocódigo a seguir é um contorno extremamente breve mostrando como encontrar e conectar os filtros WDM. Ele omite muitos detalhes e é destinado apenas a mostrar as etapas gerais que seu aplicativo precisaria seguir.


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

 

 



