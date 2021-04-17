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
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="93583-103">Requisitos de PIN para filtros de captura</span><span class="sxs-lookup"><span data-stu-id="93583-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="93583-104">Este tópico descreve os requisitos para implementar um PIN de saída em um filtro de captura do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="93583-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="93583-105">Nome do pino</span><span class="sxs-lookup"><span data-stu-id="93583-105">Pin Name</span></span>

<span data-ttu-id="93583-106">Você pode dar um PIN a qualquer nome.</span><span class="sxs-lookup"><span data-stu-id="93583-106">You can give a pin any name.</span></span> <span data-ttu-id="93583-107">Se o nome do PIN começar com o caractere de til (~), o Gerenciador do grafo de filtro não renderizará automaticamente esse PIN quando um aplicativo chamar [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span><span class="sxs-lookup"><span data-stu-id="93583-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="93583-108">Por exemplo, se o filtro tiver um PIN de captura e um PIN de visualização, você poderá nomeá-los como "~ Capture" e "Preview", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="93583-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="93583-109">Se um aplicativo renderizar esse filtro em um grafo, o pino de visualização se conectará ao seu renderizador padrão e nada se conectará ao PIN de captura, que é um comportamento padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="93583-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="93583-110">Isso também pode se aplicar a Pins que fornecem dados informativos que não devem ser renderizados ou Pins que precisam de propriedades personalizadas definidas.</span><span class="sxs-lookup"><span data-stu-id="93583-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="93583-111">Observe que os Pins com o prefixo til (~) ainda podem ser conectados manualmente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93583-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="93583-112">Fixar categoria</span><span class="sxs-lookup"><span data-stu-id="93583-112">Pin Category</span></span>

<span data-ttu-id="93583-113">Um filtro de captura sempre tem um PIN de captura e pode ter um PIN de visualização.</span><span class="sxs-lookup"><span data-stu-id="93583-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="93583-114">Alguns filtros de captura podem ter outros Pins de saída para fornecer outros tipos de dados, como informações de controle.</span><span class="sxs-lookup"><span data-stu-id="93583-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="93583-115">Cada pino de saída deve expor a interface [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="93583-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="93583-116">Os aplicativos usam essa interface para determinar a categoria do PIN.</span><span class="sxs-lookup"><span data-stu-id="93583-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="93583-117">O PIN normalmente retorna a \_ captura de categoria de PIN \_ ou a visualização de categoria de PIN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93583-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="93583-118">Para obter mais informações, consulte [Pin Property Set](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="93583-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="93583-119">O exemplo a seguir mostra como implementar [**IKsPropertySet**](ikspropertyset.md) para retornar a categoria de PIN em um PIN de captura:</span><span class="sxs-lookup"><span data-stu-id="93583-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="93583-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93583-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93583-121">Gravando filtros de captura</span><span class="sxs-lookup"><span data-stu-id="93583-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



