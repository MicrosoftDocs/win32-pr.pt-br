---
description: Este tópico descreve os requisitos para implementar um pino de saída em um DirectShow de captura.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Fixar requisitos para filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e72c74f06970bf6124d0e5dffea458bb41bcd0a19db44acc71a51615aa2fee8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316106"
---
# <a name="pin-requirements-for-capture-filters"></a>Fixar requisitos para filtros de captura

Este tópico descreve os requisitos para implementar um pino de saída em um DirectShow de captura.

## <a name="pin-name"></a>Nome do pino

Você pode dar a um pin qualquer nome. Se o nome do pino começar com o caractere til (~), o Gerenciador de Graph do Filtro não renderizará automaticamente esse pin quando um aplicativo chamar [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Por exemplo, se o filtro tiver um pin de captura e um pin de visualização, você poderá nomeá-los como "~Capture" e "Preview", respectivamente. Se um aplicativo renderizar esse filtro em um grafo, o pino de visualização se conectará ao renderdor padrão e nada se conectará ao pino de captura, que é um comportamento padrão razoável. Isso também pode se aplicar a pinos que entregam dados informacionais que não devem ser renderizados ou a pinos que precisam de propriedades personalizadas definidas. Observe que os pinos com o prefixo til (~) ainda podem ser conectados manualmente pelo aplicativo.

## <a name="pin-category"></a>Categoria de pino

Um filtro de captura sempre tem um pino de captura e pode ter um pino de visualização. Alguns filtros de captura podem ter outros pinos de saída para fornecer outros tipos de dados, como informações de controle. Cada pino de saída deve expor a interface [**IKsPropertySet.**](ikspropertyset.md) Os aplicativos usam essa interface para determinar a categoria de pino. O pino normalmente retorna PIN \_ CATEGORY CAPTURE ou PIN CATEGORY \_ \_ \_ PREVIEW. Para obter mais informações, consulte [Fixar conjunto de propriedades](pin-property-set.md).

O exemplo a seguir mostra como implementar [**IKsPropertySet para**](ikspropertyset.md) retornar a categoria de pino em um pin de captura:


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

[Escrevendo filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



