---
title: Efeito de saturação
description: Use esse efeito para alterar a saturação de uma imagem.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- efeito de saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009242"
---
# <a name="saturation-effect"></a><span data-ttu-id="c2e09-104">Efeito de saturação</span><span class="sxs-lookup"><span data-stu-id="c2e09-104">Saturation effect</span></span>

<span data-ttu-id="c2e09-105">Use esse efeito para alterar a saturação de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="c2e09-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="c2e09-106">O efeito de saturação é uma especialização do efeito da [matriz de cores](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="c2e09-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="c2e09-107">O CLSID para esse efeito é CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="c2e09-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="c2e09-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c2e09-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c2e09-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c2e09-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c2e09-110">Requirements</span><span class="sxs-lookup"><span data-stu-id="c2e09-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c2e09-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2e09-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c2e09-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="c2e09-112">Example image</span></span>

<span data-ttu-id="c2e09-113">O exemplo aqui mostra as imagens de entrada e saída do efeito de saturação com uma saturação de 0%.</span><span class="sxs-lookup"><span data-stu-id="c2e09-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="c2e09-114">Antes</span><span class="sxs-lookup"><span data-stu-id="c2e09-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)  |
| <span data-ttu-id="c2e09-116">After (após)</span><span class="sxs-lookup"><span data-stu-id="c2e09-116">After</span></span>                                                       |
| ![a imagem após a transformação.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="c2e09-118">O efeito calcula uma matriz de cores com base no valor de saturação (*s* na equação aqui) que você especifica com a \_ Propriedade saturação de d2d1 saturação \_ prop \_ .</span><span class="sxs-lookup"><span data-stu-id="c2e09-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="c2e09-119">A equação de matriz é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="c2e09-119">The matrix equation is shown here.</span></span>

![fórmula para calcular uma matriz de saturação.](images/saturation-formula.png)

<span data-ttu-id="c2e09-121">A matriz criada depende apenas do valor de saturação.</span><span class="sxs-lookup"><span data-stu-id="c2e09-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="c2e09-122">Você pode usar o efeito de [matriz de cores](color-matrix.md) se precisar de uma matriz específica.</span><span class="sxs-lookup"><span data-stu-id="c2e09-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="c2e09-123">Esse efeito consome e gera imagens alfa multiplicadas.</span><span class="sxs-lookup"><span data-stu-id="c2e09-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="c2e09-124">O efeito não funcionará em imagens alfa retas, a menos que elas sejam totalmente opacas.</span><span class="sxs-lookup"><span data-stu-id="c2e09-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c2e09-125">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="c2e09-125">Effect properties</span></span>



| <span data-ttu-id="c2e09-126">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="c2e09-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="c2e09-127">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="c2e09-127">Type and default value</span></span>           | <span data-ttu-id="c2e09-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e09-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e09-129">Saturação</span><span class="sxs-lookup"><span data-stu-id="c2e09-129">Saturation</span></span><br/> <span data-ttu-id="c2e09-130">\_Saturação de \_ prop d2d1 saturação \_</span><span class="sxs-lookup"><span data-stu-id="c2e09-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="c2e09-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c2e09-131">FLOAT</span></span><br/> <span data-ttu-id="c2e09-132">0,5 f</span><span class="sxs-lookup"><span data-stu-id="c2e09-132">0.5f</span></span><br/> | <span data-ttu-id="c2e09-133">A saturação da imagem.</span><span class="sxs-lookup"><span data-stu-id="c2e09-133">The saturation of the image.</span></span> <span data-ttu-id="c2e09-134">Você pode definir a saturação para um valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="c2e09-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="c2e09-135">Se você defini-lo como 1, a imagem de saída será totalmente saturada.</span><span class="sxs-lookup"><span data-stu-id="c2e09-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="c2e09-136">Se você defini-lo como 0, a imagem de saída será monocromática.</span><span class="sxs-lookup"><span data-stu-id="c2e09-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="c2e09-137">O valor de saturação não é unitário.</span><span class="sxs-lookup"><span data-stu-id="c2e09-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c2e09-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e09-138">Requirements</span></span>



| <span data-ttu-id="c2e09-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e09-139">Requirement</span></span> | <span data-ttu-id="c2e09-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c2e09-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e09-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e09-141">Minimum supported client</span></span> | <span data-ttu-id="c2e09-142">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c2e09-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2e09-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e09-143">Minimum supported server</span></span> | <span data-ttu-id="c2e09-144">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c2e09-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2e09-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2e09-145">Header</span></span>                   | <span data-ttu-id="c2e09-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c2e09-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c2e09-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2e09-147">Library</span></span>                  | <span data-ttu-id="c2e09-148">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c2e09-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c2e09-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2e09-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e09-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c2e09-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

