---
title: Efeito de bloco
description: Use o efeito de bloco para repetir a região especificada da imagem.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- efeito de bloco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009448"
---
# <a name="tile-effect"></a><span data-ttu-id="5dd3e-104">Efeito de bloco</span><span class="sxs-lookup"><span data-stu-id="5dd3e-104">Tile effect</span></span>

<span data-ttu-id="5dd3e-105">Use o efeito de bloco para repetir a região especificada da imagem.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="5dd3e-106">O CLSID para esse efeito é CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="5dd3e-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="5dd3e-107">Example image</span></span>



| <span data-ttu-id="5dd3e-108">Antes</span><span class="sxs-lookup"><span data-stu-id="5dd3e-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="5dd3e-110">After (após)</span><span class="sxs-lookup"><span data-stu-id="5dd3e-110">After</span></span>                                                      |
| ![a imagem após a transformação.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="5dd3e-112">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="5dd3e-112">Effect properties</span></span>



| <span data-ttu-id="5dd3e-113">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="5dd3e-113">Display name and index enumeration</span></span>                | <span data-ttu-id="5dd3e-114">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="5dd3e-114">Type and default value</span></span>                                              | <span data-ttu-id="5dd3e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5dd3e-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd3e-116">Rect</span><span class="sxs-lookup"><span data-stu-id="5dd3e-116">Rect</span></span><br/> <span data-ttu-id="5dd3e-117">D2D1 de \_ prop Tile de bloco \_ \_</span><span class="sxs-lookup"><span data-stu-id="5dd3e-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="5dd3e-118">\_4F de vetor d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="5dd3e-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="5dd3e-119">{0,0 f, 0,0 f, 100.0 f, 100.0 f}</span><span class="sxs-lookup"><span data-stu-id="5dd3e-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="5dd3e-120">A região da imagem a ser sublado.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-120">The region of the image to be tiled.</span></span> <span data-ttu-id="5dd3e-121">Essa propriedade é um \_ 4F de vetor d2d1 \_ definido como: (Left, Top, direita, Bottom).</span><span class="sxs-lookup"><span data-stu-id="5dd3e-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="5dd3e-122">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="5dd3e-123">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="5dd3e-123">Output bitmap</span></span>

<span data-ttu-id="5dd3e-124">Esse efeito gera um bitmap de tamanho logicamente infinito.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="5dd3e-125">Você pode colocar uma imagem em bloco e gerar um determinado tamanho sem efeitos adicionais definindo o tamanho ao chamar [**ID2D1DeviceContext::D RawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span><span class="sxs-lookup"><span data-stu-id="5dd3e-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd3e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dd3e-126">Requirements</span></span>



| <span data-ttu-id="5dd3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dd3e-127">Requirement</span></span> | <span data-ttu-id="5dd3e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5dd3e-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd3e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dd3e-129">Minimum supported client</span></span> | <span data-ttu-id="5dd3e-130">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="5dd3e-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5dd3e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dd3e-131">Minimum supported server</span></span> | <span data-ttu-id="5dd3e-132">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="5dd3e-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5dd3e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dd3e-133">Header</span></span>                   | <span data-ttu-id="5dd3e-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="5dd3e-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="5dd3e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dd3e-135">Library</span></span>                  | <span data-ttu-id="5dd3e-136">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="5dd3e-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="5dd3e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dd3e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd3e-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="5dd3e-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

