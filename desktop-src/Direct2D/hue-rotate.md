---
title: Efeito de Rotatation de matiz
description: Use o efeito de rotação de matiz para alterar o matiz de uma imagem aplicando uma matriz de cores com base no ângulo de rotação.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- efeito de Rotatation de matiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104563054"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="ef9d3-104">Efeito de Rotatation de matiz</span><span class="sxs-lookup"><span data-stu-id="ef9d3-104">Hue rotatation effect</span></span>

<span data-ttu-id="ef9d3-105">Use o efeito de rotação de matiz para alterar o matiz de uma imagem aplicando uma matriz de cores com base no ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="ef9d3-106">O CLSID para esse efeito é CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="ef9d3-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ef9d3-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ef9d3-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ef9d3-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ef9d3-109">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="ef9d3-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ef9d3-110">Requirements</span><span class="sxs-lookup"><span data-stu-id="ef9d3-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ef9d3-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef9d3-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ef9d3-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ef9d3-112">Example image</span></span>

<span data-ttu-id="ef9d3-113">O exemplo aqui mostra as imagens de entrada e saída do efeito de rotação de matiz com um ângulo de rotação de 270 graus.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="ef9d3-114">Antes</span><span class="sxs-lookup"><span data-stu-id="ef9d3-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| <span data-ttu-id="ef9d3-116">After (após)</span><span class="sxs-lookup"><span data-stu-id="ef9d3-116">After</span></span>                                                        |
| ![a imagem após a transformação.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="ef9d3-118">O efeito calcula uma matriz de cores com base no ângulo de rotação (*?*) que você especifica com a \_ propriedade de ângulo de prop d2d1 HUEROTATION \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ef9d3-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="ef9d3-119">Aqui estão as equações de matriz.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-119">Here are the matrix equations.</span></span>

![cálculos de rotação de matiz](images/hue-formula.png)

<span data-ttu-id="ef9d3-121">A matriz criada depende apenas do ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="ef9d3-122">Você pode usar o efeito de [matriz de cores](color-matrix.md) se precisar de uma matriz específica.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ef9d3-123">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ef9d3-123">Effect properties</span></span>



| <span data-ttu-id="ef9d3-124">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="ef9d3-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="ef9d3-125">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="ef9d3-125">Type and default value</span></span>           | <span data-ttu-id="ef9d3-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef9d3-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="ef9d3-127">Ângulo</span><span class="sxs-lookup"><span data-stu-id="ef9d3-127">Angle</span></span><br/> <span data-ttu-id="ef9d3-128">\_Ângulo de \_ prop d2d1 HUEROTATION \_</span><span class="sxs-lookup"><span data-stu-id="ef9d3-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="ef9d3-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ef9d3-129">FLOAT</span></span><br/> <span data-ttu-id="ef9d3-130">0,0 f</span><span class="sxs-lookup"><span data-stu-id="ef9d3-130">0.0f</span></span><br/> | <span data-ttu-id="ef9d3-131">O ângulo para girar o matiz, em graus.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="ef9d3-132">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="ef9d3-132">Output bitmap</span></span>

<span data-ttu-id="ef9d3-133">O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef9d3-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef9d3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef9d3-134">Requirements</span></span>



| <span data-ttu-id="ef9d3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef9d3-135">Requirement</span></span> | <span data-ttu-id="ef9d3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ef9d3-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9d3-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef9d3-137">Minimum supported client</span></span> | <span data-ttu-id="ef9d3-138">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ef9d3-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ef9d3-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef9d3-139">Minimum supported server</span></span> | <span data-ttu-id="ef9d3-140">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ef9d3-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ef9d3-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef9d3-141">Header</span></span>                   | <span data-ttu-id="ef9d3-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ef9d3-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ef9d3-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef9d3-143">Library</span></span>                  | <span data-ttu-id="ef9d3-144">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ef9d3-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ef9d3-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef9d3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef9d3-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ef9d3-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

