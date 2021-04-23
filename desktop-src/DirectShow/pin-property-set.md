---
description: Conjunto de propriedades de PIN
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Conjunto de propriedades de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909613"
---
# <a name="pin-property-set"></a><span data-ttu-id="94a57-103">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="94a57-103">Pin Property Set</span></span>

<span data-ttu-id="94a57-104">O conjunto de propriedades PIN retorna a categoria de PIN de um PIN em um filtro.</span><span class="sxs-lookup"><span data-stu-id="94a57-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="94a57-105">A categoria é definida pelo filtro quando ele cria o PIN; a categoria indica que tipo de dados o PIN é entregue ou recebe por esse PIN.</span><span class="sxs-lookup"><span data-stu-id="94a57-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="94a57-106">Label</span><span class="sxs-lookup"><span data-stu-id="94a57-106">Label</span></span> | <span data-ttu-id="94a57-107">Valor</span><span class="sxs-lookup"><span data-stu-id="94a57-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="94a57-108">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="94a57-108">Property Set GUID</span></span> | <span data-ttu-id="94a57-109">**AMPROPSETID \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="94a57-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="94a57-110">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="94a57-110">Property ID</span></span>                   | <span data-ttu-id="94a57-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="94a57-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="94a57-112">**\_categoria AMPROPERTY PIN \_**</span><span class="sxs-lookup"><span data-stu-id="94a57-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="94a57-113">Especifica a categoria de um PIN.</span><span class="sxs-lookup"><span data-stu-id="94a57-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="94a57-114">O DirectShow define as seguintes categorias de PIN no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="94a57-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="94a57-115">GUID da categoria</span><span class="sxs-lookup"><span data-stu-id="94a57-115">Category GUID</span></span>                     | <span data-ttu-id="94a57-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="94a57-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a57-117">**FIXAR \_ categoria \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="94a57-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="94a57-118">Pino de entrada do filtro de captura que usa analógico e digitalizado.</span><span class="sxs-lookup"><span data-stu-id="94a57-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="94a57-119">**FIXAR \_ captura de categoria \_**</span><span class="sxs-lookup"><span data-stu-id="94a57-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="94a57-120">Capturar PIN.</span><span class="sxs-lookup"><span data-stu-id="94a57-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="94a57-121">**FIXAR \_ categoria \_ CC**</span><span class="sxs-lookup"><span data-stu-id="94a57-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="94a57-122">PIN fornecendo dados de legenda codificada da linha 21.</span><span class="sxs-lookup"><span data-stu-id="94a57-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="94a57-123">**FIXAR \_ categoria \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="94a57-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="94a57-124">PIN fornecendo serviços de dados estendidos (linha 21, até mesmo campos).</span><span class="sxs-lookup"><span data-stu-id="94a57-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="94a57-125">**FIXAR \_ categoria \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="94a57-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="94a57-126">PIN que fornece dados padrão do norte da América do Videotext.</span><span class="sxs-lookup"><span data-stu-id="94a57-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="94a57-127">**FIXAR \_ Visualização da categoria \_**</span><span class="sxs-lookup"><span data-stu-id="94a57-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="94a57-128">PIN de visualização.</span><span class="sxs-lookup"><span data-stu-id="94a57-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="94a57-129">**FIXAR \_ categoria \_ ainda**</span><span class="sxs-lookup"><span data-stu-id="94a57-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="94a57-130">PIN que fornece uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="94a57-130">Pin that provides a still image.</span></span> <span data-ttu-id="94a57-131">O PIN de captura do filtro deve ser conectado antes que o PIN da imagem ainda esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="94a57-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="94a57-132">**FIXAR \_ o \_ teletexto da categoria**</span><span class="sxs-lookup"><span data-stu-id="94a57-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="94a57-133">PIN fornecendo teletexto (uma variante de legenda oculta).</span><span class="sxs-lookup"><span data-stu-id="94a57-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="94a57-134">**código de panela da categoria do PIN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94a57-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="94a57-135">PIN fornecendo dados de código de code.</span><span class="sxs-lookup"><span data-stu-id="94a57-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="94a57-136">**FIXAR \_ categoria \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="94a57-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="94a57-137">PIN fornecendo dados de intervalo em branco vertical.</span><span class="sxs-lookup"><span data-stu-id="94a57-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="94a57-138">**FIXAR \_ categoria \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="94a57-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="94a57-139">Pino de saída de vídeo a ser conectado ao pino de entrada zero no [mixer de sobreposição](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="94a57-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="94a57-140">**FIXAR \_ categoria \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="94a57-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="94a57-141">PIN a ser conectado ao [alocador de superfície VBI](vbi-surface-allocator.md), o filtro de alocador de superfície VBI necessário para alocar a memória de vídeo correta para itens como sobreposições de legendagem oculta em cenários em que uma porta de vídeo está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="94a57-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="94a57-142">Cenários PCI, IEEE 1394 e USB não usam esse filtro.</span><span class="sxs-lookup"><span data-stu-id="94a57-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="94a57-143">**\_captura de vídeo \_ CC \_ do PINNAME**</span><span class="sxs-lookup"><span data-stu-id="94a57-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="94a57-144">Fatia de hardware-pino de legenda fechado</span><span class="sxs-lookup"><span data-stu-id="94a57-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="94a57-145">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="94a57-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="94a57-146">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="94a57-146">Example Code</span></span>

<span data-ttu-id="94a57-147">O código a seguir mostra como verificar se um PIN dá suporte a esse conjunto de propriedades e, nesse caso, como obter a categoria do PIN:</span><span class="sxs-lookup"><span data-stu-id="94a57-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="94a57-148">Este exemplo usa a função [SafeRelease](../medfound/saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="94a57-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94a57-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94a57-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a57-150">Requisitos de PIN para filtros de captura</span><span class="sxs-lookup"><span data-stu-id="94a57-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="94a57-151">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="94a57-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="94a57-152">Trabalhando com categorias de PIN</span><span class="sxs-lookup"><span data-stu-id="94a57-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
