---
description: Conjunto de propriedades de PIN
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Conjunto de propriedades de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370143"
---
# <a name="pin-property-set"></a><span data-ttu-id="4bf34-103">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="4bf34-103">Pin Property Set</span></span>

<span data-ttu-id="4bf34-104">O conjunto de propriedades PIN retorna a categoria de PIN de um PIN em um filtro.</span><span class="sxs-lookup"><span data-stu-id="4bf34-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="4bf34-105">A categoria é definida pelo filtro quando ele cria o PIN; a categoria indica que tipo de dados o PIN é entregue ou recebe por esse PIN.</span><span class="sxs-lookup"><span data-stu-id="4bf34-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="4bf34-106">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="4bf34-106">Property Set GUID</span></span> | <span data-ttu-id="4bf34-107">**AMPROPSETID \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="4bf34-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="4bf34-108">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="4bf34-108">Property ID</span></span>                   | <span data-ttu-id="4bf34-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bf34-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="4bf34-110">**\_categoria AMPROPERTY PIN \_**</span><span class="sxs-lookup"><span data-stu-id="4bf34-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="4bf34-111">Especifica a categoria de um PIN.</span><span class="sxs-lookup"><span data-stu-id="4bf34-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="4bf34-112">O DirectShow define as seguintes categorias de PIN no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="4bf34-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="4bf34-113">GUID da categoria</span><span class="sxs-lookup"><span data-stu-id="4bf34-113">Category GUID</span></span>                     | <span data-ttu-id="4bf34-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bf34-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf34-115">**FIXAR \_ categoria \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="4bf34-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="4bf34-116">Pino de entrada do filtro de captura que usa analógico e digitalizado.</span><span class="sxs-lookup"><span data-stu-id="4bf34-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="4bf34-117">**FIXAR \_ captura de categoria \_**</span><span class="sxs-lookup"><span data-stu-id="4bf34-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="4bf34-118">Capturar PIN.</span><span class="sxs-lookup"><span data-stu-id="4bf34-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4bf34-119">**FIXAR \_ categoria \_ CC**</span><span class="sxs-lookup"><span data-stu-id="4bf34-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="4bf34-120">PIN fornecendo dados de legenda codificada da linha 21.</span><span class="sxs-lookup"><span data-stu-id="4bf34-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4bf34-121">**FIXAR \_ categoria \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="4bf34-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="4bf34-122">PIN fornecendo serviços de dados estendidos (linha 21, até mesmo campos).</span><span class="sxs-lookup"><span data-stu-id="4bf34-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4bf34-123">**FIXAR \_ categoria \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="4bf34-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="4bf34-124">PIN que fornece dados padrão do norte da América do Videotext.</span><span class="sxs-lookup"><span data-stu-id="4bf34-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4bf34-125">**FIXAR \_ Visualização da categoria \_**</span><span class="sxs-lookup"><span data-stu-id="4bf34-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="4bf34-126">PIN de visualização.</span><span class="sxs-lookup"><span data-stu-id="4bf34-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4bf34-127">**FIXAR \_ categoria \_ ainda**</span><span class="sxs-lookup"><span data-stu-id="4bf34-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="4bf34-128">PIN que fornece uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="4bf34-128">Pin that provides a still image.</span></span> <span data-ttu-id="4bf34-129">O PIN de captura do filtro deve ser conectado antes que o PIN da imagem ainda esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="4bf34-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="4bf34-130">**FIXAR \_ o \_ teletexto da categoria**</span><span class="sxs-lookup"><span data-stu-id="4bf34-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="4bf34-131">PIN fornecendo teletexto (uma variante de legenda oculta).</span><span class="sxs-lookup"><span data-stu-id="4bf34-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4bf34-132">**código de panela da categoria do PIN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4bf34-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="4bf34-133">PIN fornecendo dados de código de code.</span><span class="sxs-lookup"><span data-stu-id="4bf34-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4bf34-134">**FIXAR \_ categoria \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="4bf34-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="4bf34-135">PIN fornecendo dados de intervalo em branco vertical.</span><span class="sxs-lookup"><span data-stu-id="4bf34-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4bf34-136">**FIXAR \_ categoria \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="4bf34-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="4bf34-137">Pino de saída de vídeo a ser conectado ao pino de entrada zero no [mixer de sobreposição](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4bf34-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="4bf34-138">**FIXAR \_ categoria \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="4bf34-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="4bf34-139">PIN a ser conectado ao [alocador de superfície VBI](vbi-surface-allocator.md), o filtro de alocador de superfície VBI necessário para alocar a memória de vídeo correta para itens como sobreposições de legendagem oculta em cenários em que uma porta de vídeo está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="4bf34-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="4bf34-140">Cenários PCI, IEEE 1394 e USB não usam esse filtro.</span><span class="sxs-lookup"><span data-stu-id="4bf34-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="4bf34-141">**\_captura de vídeo \_ CC \_ do PINNAME**</span><span class="sxs-lookup"><span data-stu-id="4bf34-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="4bf34-142">Fatia de hardware-pino de legenda fechado</span><span class="sxs-lookup"><span data-stu-id="4bf34-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="4bf34-143">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4bf34-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="4bf34-144">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="4bf34-144">Example Code</span></span>

<span data-ttu-id="4bf34-145">O código a seguir mostra como verificar se um PIN dá suporte a esse conjunto de propriedades e, nesse caso, como obter a categoria do PIN:</span><span class="sxs-lookup"><span data-stu-id="4bf34-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="4bf34-146">Este exemplo usa a função [SafeRelease](../medfound/saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="4bf34-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4bf34-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4bf34-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf34-148">Requisitos de PIN para filtros de captura</span><span class="sxs-lookup"><span data-stu-id="4bf34-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="4bf34-149">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="4bf34-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="4bf34-150">Trabalhando com categorias de PIN</span><span class="sxs-lookup"><span data-stu-id="4bf34-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
