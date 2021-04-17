---
title: Luminância para efeito alfa
description: Use o efeito de luminância para alfa para definir o canal alfa como a luminância da imagem e definir os canais de cor como 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminância para efeito alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561554"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="3c7ee-104">Luminância para efeito alfa</span><span class="sxs-lookup"><span data-stu-id="3c7ee-104">Luminance to alpha effect</span></span>

<span data-ttu-id="3c7ee-105">Use o efeito de luminância para alfa para definir o canal alfa como a luminância da imagem e definir os canais de cor como 0.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="3c7ee-106">Você pode usar a saída desse efeito para fazer uma sobreposição semitransparente com base no brilho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="3c7ee-107">Ou você pode usá-lo para criar uma máscara de imagem.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="3c7ee-108">Esse efeito não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-108">This effect has no properties.</span></span>

 

<span data-ttu-id="3c7ee-109">O CLSID para esse efeito é CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="3c7ee-110">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="3c7ee-110">Example image</span></span>

<span data-ttu-id="3c7ee-111">Este exemplo mostra a saída da luminância para efeito alfa composta em uma superfície branca para mostrar a opacidade.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="3c7ee-112">Antes</span><span class="sxs-lookup"><span data-stu-id="3c7ee-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)        |
| <span data-ttu-id="3c7ee-114">After (após)</span><span class="sxs-lookup"><span data-stu-id="3c7ee-114">After</span></span>                                                             |
| ![a imagem após a transformação.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="3c7ee-116">Esse efeito define o canal alfa da saída para a luminância da imagem de entrada usando essa matriz de cores.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![a matriz de cores que o efeito usa para definir o canal alfa.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="3c7ee-118">Esse efeito consome e gera imagens alfa multiplicadas.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="3c7ee-119">O efeito não funcionará em imagens alfa retas, a menos que elas sejam totalmente opacas.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="3c7ee-120">Como as imagens são armazenadas em um formato de compensação de gama, antes de calcular a luminância de uma imagem, primeiro você deve executar a correção de gama inversa para obter os valores de cor verdadeiros para a imagem.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="3c7ee-121">Como as imagens normalmente são armazenadas em 2,2 gama, você pode usar o efeito de transferência de gama com um expoente de (1/2.2) e, em seguida, usar a saída desse efeito.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c7ee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c7ee-122">Requirements</span></span>



| <span data-ttu-id="3c7ee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c7ee-123">Requirement</span></span> | <span data-ttu-id="3c7ee-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3c7ee-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7ee-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c7ee-125">Minimum supported client</span></span> | <span data-ttu-id="3c7ee-126">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3c7ee-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3c7ee-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c7ee-127">Minimum supported server</span></span> | <span data-ttu-id="3c7ee-128">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3c7ee-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3c7ee-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c7ee-129">Header</span></span>                   | <span data-ttu-id="3c7ee-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="3c7ee-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="3c7ee-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c7ee-131">Library</span></span>                  | <span data-ttu-id="3c7ee-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="3c7ee-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="3c7ee-133">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="3c7ee-133">Output bitmap</span></span>

<span data-ttu-id="3c7ee-134">A saída tem o mesmo tamanho da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c7ee-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c7ee-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c7ee-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7ee-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="3c7ee-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
