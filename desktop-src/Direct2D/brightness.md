---
title: Efeito de brilho
description: Use o efeito de brilho para controlar o brilho da imagem.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- efeito de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104563971"
---
# <a name="brightness-effect"></a><span data-ttu-id="ef2cb-104">Efeito de brilho</span><span class="sxs-lookup"><span data-stu-id="ef2cb-104">Brightness effect</span></span>

<span data-ttu-id="ef2cb-105">Use o efeito de brilho para controlar o brilho da imagem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="ef2cb-106">O CLSID para esse efeito é CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="ef2cb-107">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ef2cb-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ef2cb-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ef2cb-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ef2cb-109">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="ef2cb-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ef2cb-110">Requirements</span><span class="sxs-lookup"><span data-stu-id="ef2cb-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ef2cb-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef2cb-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ef2cb-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="ef2cb-112">Example image</span></span>



| <span data-ttu-id="ef2cb-113">Antes</span><span class="sxs-lookup"><span data-stu-id="ef2cb-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)  |
| <span data-ttu-id="ef2cb-115">After (após)</span><span class="sxs-lookup"><span data-stu-id="ef2cb-115">After</span></span>                                                       |
| ![a imagem após a transformação.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="ef2cb-117">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ef2cb-117">Effect properties</span></span>



| <span data-ttu-id="ef2cb-118">Nome de exibição da propriedade</span><span class="sxs-lookup"><span data-stu-id="ef2cb-118">Property Display Name</span></span>                                                 | <span data-ttu-id="ef2cb-119">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="ef2cb-119">Type and default value</span></span>                              | <span data-ttu-id="ef2cb-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef2cb-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2cb-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="ef2cb-121">WhitePoint</span></span><br/> <span data-ttu-id="ef2cb-122">\_ \_ \_ Ponto branco de prop \_ d2d1 de brilho</span><span class="sxs-lookup"><span data-stu-id="ef2cb-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="ef2cb-123">\_Vetor d2d1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="ef2cb-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="ef2cb-124">{1,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="ef2cb-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="ef2cb-125">A parte superior da curva de transferência de brilho.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="ef2cb-126">O ponto branco ajusta a aparência das partes mais brilhantes da imagem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="ef2cb-127">Essa propriedade é para o valor x e o valor y, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="ef2cb-128">Cada um dos valores dessa propriedade está entre 0 e 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="ef2cb-129">BlackPoint</span><span class="sxs-lookup"><span data-stu-id="ef2cb-129">BlackPoint</span></span><br/> <span data-ttu-id="ef2cb-130">\_ \_ \_ Ponto preto de prop \_ d2d1 de brilho</span><span class="sxs-lookup"><span data-stu-id="ef2cb-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="ef2cb-131">\_Vetor d2d1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="ef2cb-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="ef2cb-132">{0,0 f, 0,0 f}</span><span class="sxs-lookup"><span data-stu-id="ef2cb-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="ef2cb-133">A parte inferior da curva de transferência de brilho.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="ef2cb-134">O ponto preto ajusta a aparência das partes mais escuras da imagem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="ef2cb-135">Essa propriedade é para o valor x e o valor y, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="ef2cb-136">Cada um dos valores dessa propriedade está entre 0 e 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="ef2cb-137">Esse efeito usa os pontos branco e preto especificados para gerar uma função de transferência usada para ajustar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="ef2cb-138">A próxima equação descreve a função de transferência.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="ef2cb-139">As intensidades de entrada são definidas entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-139">The input intensities are defined between 0 and 1.</span></span>

![algoritmo de brilho](images/brightness-formula1.png)

<span data-ttu-id="ef2cb-141">O algoritmo de efeito implementa uma equação que cria a função de transferência.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="ef2cb-142">Usamos essa função para ajustar os pixels da imagem.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="ef2cb-143">Os valores x e y do ponto preto e do ponto branco são as coordenadas em duas dimensões que estão conectadas para formar a transformação.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="ef2cb-144">Cada parte da equação de saída final:</span><span class="sxs-lookup"><span data-stu-id="ef2cb-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="ef2cb-145">Converte os dados de imagem do espaço linear em espaço não linear usando esta equação:</span><span class="sxs-lookup"><span data-stu-id="ef2cb-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![função auxiliar 1](images/brightness-formula2.png)

2.  <span data-ttu-id="ef2cb-147">Ajusta a imagem de acordo com estes valores:</span><span class="sxs-lookup"><span data-stu-id="ef2cb-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="ef2cb-148">*entrada* são os valores de intensidade de pixel da imagem de entrada de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="ef2cb-149">*Pt branca. (x, y)* o local da curva de transformação para intensidades de pixel mais brilhantes.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="ef2cb-150">*Black pt. (x, y)* é o local da curva de transformação para intensidades de pixel do DIMM.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="ef2cb-151">Converte os dados da imagem de volta em espaço linear usando esta equação:</span><span class="sxs-lookup"><span data-stu-id="ef2cb-151">Converts the image data back to linear space using this equation:</span></span> ![função auxiliar 2](images/brightness-formula3.png)

<span data-ttu-id="ef2cb-153">A equação de saída final e as partes do componente são mostradas aqui.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-153">The final output equation and the component parts are shown here.</span></span>

![os cálculos completos para o ajuste de brilho](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="ef2cb-155">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="ef2cb-155">Output bitmap</span></span>

<span data-ttu-id="ef2cb-156">O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2cb-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef2cb-157">Requirements</span></span>



| <span data-ttu-id="ef2cb-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2cb-158">Requirement</span></span> | <span data-ttu-id="ef2cb-159">Valor</span><span class="sxs-lookup"><span data-stu-id="ef2cb-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2cb-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef2cb-160">Minimum supported client</span></span> | <span data-ttu-id="ef2cb-161">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ef2cb-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ef2cb-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef2cb-162">Minimum supported server</span></span> | <span data-ttu-id="ef2cb-163">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ef2cb-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ef2cb-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef2cb-164">Header</span></span>                   | <span data-ttu-id="ef2cb-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ef2cb-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ef2cb-166">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef2cb-166">Library</span></span>                  | <span data-ttu-id="ef2cb-167">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ef2cb-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ef2cb-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef2cb-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef2cb-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ef2cb-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

