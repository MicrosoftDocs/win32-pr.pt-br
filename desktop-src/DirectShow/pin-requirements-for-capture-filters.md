---
description: Este tópico descreve os requisitos para implementar um PIN de saída em um filtro de captura do DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisitos de PIN para filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105761979"
---
# <a name="pin-requirements-for-capture-filters"></a>Requisitos de PIN para filtros de captura

Este tópico descreve os requisitos para implementar um PIN de saída em um filtro de captura do DirectShow.

## <a name="pin-name"></a>Nome do pino

Você pode dar um PIN a qualquer nome. Se o nome do PIN começar com o caractere de til (~), o Gerenciador do grafo de filtro não renderizará automaticamente esse PIN quando um aplicativo chamar [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Por exemplo, se o filtro tiver um PIN de captura e um PIN de visualização, você poderá nomeá-los como "~ Capture" e "Preview", respectivamente. Se um aplicativo renderizar esse filtro em um grafo, o pino de visualização se conectará ao seu renderizador padrão e nada se conectará ao PIN de captura, que é um comportamento padrão razoável. Isso também pode se aplicar a Pins que fornecem dados informativos que não devem ser renderizados ou Pins que precisam de propriedades personalizadas definidas. Observe que os Pins com o prefixo til (~) ainda podem ser conectados manualmente pelo aplicativo.

## <a name="pin-category"></a>Fixar categoria

Um filtro de captura sempre tem um PIN de captura e pode ter um PIN de visualização. Alguns filtros de captura podem ter outros Pins de saída para fornecer outros tipos de dados, como informações de controle. Cada pino de saída deve expor a interface [**IKsPropertySet**](ikspropertyset.md) . Os aplicativos usam essa interface para determinar a categoria do PIN. O PIN normalmente retorna a \_ captura de categoria de PIN \_ ou a visualização de categoria de PIN \_ \_ . Para obter mais informações, consulte [Pin Property Set](pin-property-set.md).

O exemplo a seguir mostra como implementar [**IKsPropertySet**](ikspropertyset.md) para retornar a categoria de PIN em um PIN de captura:


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



