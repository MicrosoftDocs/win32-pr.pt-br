---
title: Efeito de corte
description: Use o efeito de corte para gerar uma região especificada de uma imagem.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efeito de corte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824388"
---
# <a name="crop-effect"></a><span data-ttu-id="d7b06-104">Efeito de corte</span><span class="sxs-lookup"><span data-stu-id="d7b06-104">Crop effect</span></span>

<span data-ttu-id="d7b06-105">Use o efeito de corte para gerar uma região especificada de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d7b06-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="d7b06-106">O CLSID para esse efeito é CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="d7b06-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="d7b06-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d7b06-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="d7b06-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d7b06-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d7b06-109">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="d7b06-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="d7b06-110">Requirements</span><span class="sxs-lookup"><span data-stu-id="d7b06-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d7b06-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b06-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="d7b06-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d7b06-112">Example image</span></span>



| <span data-ttu-id="d7b06-113">Antes</span><span class="sxs-lookup"><span data-stu-id="d7b06-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="d7b06-115">After (após)</span><span class="sxs-lookup"><span data-stu-id="d7b06-115">After</span></span>                                                      |
| ![a imagem após a transformação.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="d7b06-117">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d7b06-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7b06-118">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="d7b06-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="d7b06-119">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="d7b06-119">Type and default value</span></span></th>
<th><span data-ttu-id="d7b06-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b06-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7b06-121">Rect</span><span class="sxs-lookup"><span data-stu-id="d7b06-121">Rect</span></span><br/></td>
<td><span data-ttu-id="d7b06-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="d7b06-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="d7b06-123">A região a ser cortada especificada como um vetor no formulário (esquerda, superior, largura, altura).</span><span class="sxs-lookup"><span data-stu-id="d7b06-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7b06-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="d7b06-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="d7b06-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="d7b06-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="d7b06-126">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="d7b06-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="d7b06-127">O Rect será truncado se sobrepuser os limites de borda da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7b06-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7b06-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="d7b06-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="d7b06-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="d7b06-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="d7b06-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="d7b06-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="d7b06-131">D2D1_BORDER_MODE_SOFT: se o retângulo de corte cair em coordenadas de pixel fracionários, o efeito aplicará a anti-aliasing, o que resulta em uma borda suave.</span><span class="sxs-lookup"><span data-stu-id="d7b06-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="d7b06-132">D2D1_BORDER_MODE_HARD: se o retângulo de corte cair em coordenadas de pixel fracionários, o efeito coloca que resulta em uma borda fixa.</span><span class="sxs-lookup"><span data-stu-id="d7b06-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="d7b06-133">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="d7b06-133">Output bitmap</span></span>

<span data-ttu-id="d7b06-134">A saída desse efeito é o tamanho da Propriedade Rect.</span><span class="sxs-lookup"><span data-stu-id="d7b06-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="d7b06-135">O comprimento e a largura são Calc.</span><span class="sxs-lookup"><span data-stu-id="d7b06-135">The length and width are calc</span></span>

<span data-ttu-id="d7b06-136">ulated usando as equações aqui:</span><span class="sxs-lookup"><span data-stu-id="d7b06-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="d7b06-137">Comprimento de saída em pixels = (Rect. Right-Rect. Left) \* (DPI do usuário/96)</span><span class="sxs-lookup"><span data-stu-id="d7b06-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="d7b06-138">Altura da saída em pixels = (Rect. Bottom-Rect.Top) \* (DPI do usuário/96)</span><span class="sxs-lookup"><span data-stu-id="d7b06-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="d7b06-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b06-139">Requirements</span></span>



| <span data-ttu-id="d7b06-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b06-140">Requirement</span></span> | <span data-ttu-id="d7b06-141">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b06-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b06-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b06-142">Minimum supported client</span></span> | <span data-ttu-id="d7b06-143">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d7b06-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d7b06-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b06-144">Minimum supported server</span></span> | <span data-ttu-id="d7b06-145">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d7b06-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d7b06-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7b06-146">Header</span></span>                   | <span data-ttu-id="d7b06-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d7b06-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d7b06-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7b06-148">Library</span></span>                  | <span data-ttu-id="d7b06-149">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d7b06-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d7b06-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b06-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b06-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d7b06-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

