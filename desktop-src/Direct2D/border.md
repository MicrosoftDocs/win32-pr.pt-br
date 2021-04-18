---
title: Efeito de borda
description: Use o efeito de borda para estender uma imagem das bordas.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efeito de borda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104506314"
---
# <a name="border-effect"></a><span data-ttu-id="48c76-104">Efeito de borda</span><span class="sxs-lookup"><span data-stu-id="48c76-104">Border effect</span></span>

<span data-ttu-id="48c76-105">Use o efeito de borda para estender uma imagem das bordas.</span><span class="sxs-lookup"><span data-stu-id="48c76-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="48c76-106">Você pode usar esse efeito para repetir os pixels das bordas da imagem, encapsular os pixels da extremidade oposta da imagem ou espelhar os pixels na borda do bitmap para estender a região do bitmap.</span><span class="sxs-lookup"><span data-stu-id="48c76-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="48c76-107">O CLSID para esse efeito é CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="48c76-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="48c76-108">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="48c76-108">Example images</span></span>

<span data-ttu-id="48c76-109">Os exemplos aqui mostram a saída do efeito de borda usando cada modo.</span><span class="sxs-lookup"><span data-stu-id="48c76-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="48c76-110">O tamanho de saída é infinito, mas essas imagens de exemplo são cortadas para duas vezes o tamanho.</span><span class="sxs-lookup"><span data-stu-id="48c76-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="48c76-111">Espelho</span><span class="sxs-lookup"><span data-stu-id="48c76-111">Mirror</span></span>



| <span data-ttu-id="48c76-112">Antes</span><span class="sxs-lookup"><span data-stu-id="48c76-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito.](images/border-before.jpg) |
| <span data-ttu-id="48c76-114">After (após)</span><span class="sxs-lookup"><span data-stu-id="48c76-114">After</span></span>                                                     |
| ![Captura de tela que mostra a imagem após a transformação.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="48c76-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="48c76-116">Clamp</span></span>



| <span data-ttu-id="48c76-117">Antes</span><span class="sxs-lookup"><span data-stu-id="48c76-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um fixe.](images/border-before.jpg)     |
| <span data-ttu-id="48c76-119">After (após)</span><span class="sxs-lookup"><span data-stu-id="48c76-119">After</span></span>                                                         |
| ![Captura de tela que mostra a imagem após a transformação de um fixe.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="48c76-121">Encapsular</span><span class="sxs-lookup"><span data-stu-id="48c76-121">Wrap</span></span>



| <span data-ttu-id="48c76-122">Antes</span><span class="sxs-lookup"><span data-stu-id="48c76-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um encapsulamento.](images/border-before.jpg)    |
| <span data-ttu-id="48c76-124">After (após)</span><span class="sxs-lookup"><span data-stu-id="48c76-124">After</span></span>                                                        |
| ![Captura de tela que mostra a imagem após a transformação de um encapsulamento.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="48c76-126">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="48c76-126">Effect properties</span></span>



| <span data-ttu-id="48c76-127">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="48c76-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="48c76-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="48c76-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c76-129">Modo de borda X</span><span class="sxs-lookup"><span data-stu-id="48c76-129">Edge Mode X</span></span><br/> <span data-ttu-id="48c76-130">D2D1 \_ Border \_ prop \_ modo de borda \_ \_ X</span><span class="sxs-lookup"><span data-stu-id="48c76-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="48c76-131">O modo de borda na direção X para o efeito.</span><span class="sxs-lookup"><span data-stu-id="48c76-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="48c76-132">Você pode definir isso como fixe, wrap ou Mirror.</span><span class="sxs-lookup"><span data-stu-id="48c76-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="48c76-133">Consulte [modos de borda](#edge-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48c76-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="48c76-134">O tipo é o modo de borda de borda D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48c76-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="48c76-135">O valor padrão é D2D1 \_ borda do modo de borda \_ \_ \_ fixe.</span><span class="sxs-lookup"><span data-stu-id="48c76-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="48c76-136">Modo de borda Y</span><span class="sxs-lookup"><span data-stu-id="48c76-136">Edge Mode Y</span></span><br/> <span data-ttu-id="48c76-137">D2D1 \_ Border \_ prop \_ modo de borda \_ \_ Y</span><span class="sxs-lookup"><span data-stu-id="48c76-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="48c76-138">O modo de borda na direção Y para o efeito.</span><span class="sxs-lookup"><span data-stu-id="48c76-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="48c76-139">Você pode definir isso como fixe, wrap ou Mirror.</span><span class="sxs-lookup"><span data-stu-id="48c76-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="48c76-140">Consulte [modos de borda](#edge-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48c76-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="48c76-141">O tipo é o modo de borda de borda D2D1 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48c76-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="48c76-142">O valor padrão é D2D1 \_ borda do modo de borda \_ \_ \_ fixe.</span><span class="sxs-lookup"><span data-stu-id="48c76-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="48c76-143">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="48c76-143">Edge modes</span></span>



| <span data-ttu-id="48c76-144">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="48c76-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="48c76-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="48c76-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48c76-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="48c76-146">Clamp</span></span><br/> <span data-ttu-id="48c76-147">Modo de borda de \_ borda d2d1 \_ \_ \_ fixe</span><span class="sxs-lookup"><span data-stu-id="48c76-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="48c76-148">Repete os pixels das bordas da imagem.</span><span class="sxs-lookup"><span data-stu-id="48c76-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="48c76-149">Encapsular</span><span class="sxs-lookup"><span data-stu-id="48c76-149">Wrap</span></span><br/> <span data-ttu-id="48c76-150">\_ \_ \_ Encapsulamento do modo \_ de borda de borda d2d1</span><span class="sxs-lookup"><span data-stu-id="48c76-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="48c76-151">Usa pixels da borda final oposta da imagem.</span><span class="sxs-lookup"><span data-stu-id="48c76-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="48c76-152">Espelho</span><span class="sxs-lookup"><span data-stu-id="48c76-152">Mirror</span></span><br/> <span data-ttu-id="48c76-153">\_Espelho do \_ \_ modo \_ de borda de borda d2d1</span><span class="sxs-lookup"><span data-stu-id="48c76-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="48c76-154">Reflete pixels sobre a borda da imagem.</span><span class="sxs-lookup"><span data-stu-id="48c76-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="48c76-155">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="48c76-155">Output bitmap</span></span>

<span data-ttu-id="48c76-156">O tamanho do bitmap de saída é infinito para todas as entradas, exceto uma imagem de entrada de tamanho 0.</span><span class="sxs-lookup"><span data-stu-id="48c76-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="48c76-157">Se a altura ou a largura de uma imagem de entrada for 0, o tamanho de saída será 0.</span><span class="sxs-lookup"><span data-stu-id="48c76-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c76-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48c76-158">Requirements</span></span>



| <span data-ttu-id="48c76-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c76-159">Requirement</span></span> | <span data-ttu-id="48c76-160">Valor</span><span class="sxs-lookup"><span data-stu-id="48c76-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48c76-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48c76-161">Minimum supported client</span></span> | <span data-ttu-id="48c76-162">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="48c76-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48c76-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48c76-163">Minimum supported server</span></span> | <span data-ttu-id="48c76-164">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="48c76-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48c76-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48c76-165">Header</span></span>                   | <span data-ttu-id="48c76-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="48c76-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="48c76-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48c76-167">Library</span></span>                  | <span data-ttu-id="48c76-168">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="48c76-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="48c76-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48c76-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48c76-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="48c76-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

