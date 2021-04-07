---
title: Efeito de inundação
description: Use o efeito de inundação para gerar um bitmap com base na cor especificada e no valor alfa. Você pode usar esse efeito quando desejar uma cor específica como uma entrada para um efeito, como uma cor de fundo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- efeito de inundação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918832"
---
# <a name="flood-effect"></a><span data-ttu-id="68785-105">Efeito de inundação</span><span class="sxs-lookup"><span data-stu-id="68785-105">Flood effect</span></span>

<span data-ttu-id="68785-106">Use o efeito de inundação para gerar um bitmap com base na cor especificada e no valor alfa.</span><span class="sxs-lookup"><span data-stu-id="68785-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="68785-107">Você pode usar esse efeito quando desejar uma cor específica como uma entrada para um efeito, como uma cor de fundo.</span><span class="sxs-lookup"><span data-stu-id="68785-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="68785-108">O efeito é transmitido ao longo do valor de cor especificado, conforme especificado.</span><span class="sxs-lookup"><span data-stu-id="68785-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="68785-109">Você deve multiplicar manualmente os valores se planeja passar a saída para efeitos que esperam uma entrada previamente multiplicada.</span><span class="sxs-lookup"><span data-stu-id="68785-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="68785-110">O CLSID para esse efeito é CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="68785-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="68785-111">O efeito de inundação não tem nenhuma imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="68785-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="68785-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="68785-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="68785-113">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="68785-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="68785-114">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="68785-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="68785-115">Requirements</span><span class="sxs-lookup"><span data-stu-id="68785-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="68785-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68785-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="68785-117">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="68785-117">Example image</span></span>

![imagem de exemplo da saída do efeito de inundação verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="68785-119">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="68785-119">Effect properties</span></span>



| <span data-ttu-id="68785-120">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="68785-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="68785-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="68785-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68785-122">Cor</span><span class="sxs-lookup"><span data-stu-id="68785-122">Color</span></span><br/> <span data-ttu-id="68785-123">\_Cor de \_ prop d2d1 Flood \_</span><span class="sxs-lookup"><span data-stu-id="68785-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="68785-124">A cor e a opacidade do bitmap.</span><span class="sxs-lookup"><span data-stu-id="68785-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="68785-125">Essa propriedade é um \_ 4F de vetor d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="68785-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="68785-126">Os valores individuais para cada canal são do tipo flutuante, não vinculado e sem unidade.</span><span class="sxs-lookup"><span data-stu-id="68785-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="68785-127">O efeito não modifica os valores dos canais.</span><span class="sxs-lookup"><span data-stu-id="68785-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="68785-128">Os valores RGBA para cada canal variam de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="68785-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="68785-129">O tipo é \_ 4F de vetor d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="68785-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="68785-130">O valor padrão é {0,0 f, 0,0 f, 0,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="68785-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="68785-131">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="68785-131">Output bitmap</span></span>

<span data-ttu-id="68785-132">Esse efeito gera um bitmap de tamanho logicamente infinito.</span><span class="sxs-lookup"><span data-stu-id="68785-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="68785-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68785-133">Requirements</span></span>



| <span data-ttu-id="68785-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="68785-134">Requirement</span></span> | <span data-ttu-id="68785-135">Valor</span><span class="sxs-lookup"><span data-stu-id="68785-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68785-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68785-136">Minimum supported client</span></span> | <span data-ttu-id="68785-137">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="68785-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="68785-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68785-138">Minimum supported server</span></span> | <span data-ttu-id="68785-139">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="68785-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="68785-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68785-140">Header</span></span>                   | <span data-ttu-id="68785-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="68785-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="68785-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68785-142">Library</span></span>                  | <span data-ttu-id="68785-143">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="68785-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="68785-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68785-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68785-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="68785-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

