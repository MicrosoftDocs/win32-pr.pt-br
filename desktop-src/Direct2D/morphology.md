---
title: Efeito de morphology
description: Use o efeito de morphology para limites de borda fino ou THICKEN em uma imagem.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- efeitos de morphology
- efeito de didatas
- efeito de Erode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085905"
---
# <a name="morphology-effect"></a><span data-ttu-id="695a5-106">Efeito de morphology</span><span class="sxs-lookup"><span data-stu-id="695a5-106">Morphology effect</span></span>

<span data-ttu-id="695a5-107">Use o efeito de morphology para limites de borda fino ou THICKEN em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="695a5-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="695a5-108">Esse efeito cria um kernel que é 2 vezes os valores de largura e altura que você especificar.</span><span class="sxs-lookup"><span data-stu-id="695a5-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="695a5-109">Esse efeito centraliza o kernel no pixel que está calculando e retorna o valor máximo no kernel (se dilating) ou no valor mínimo no kernel (se Eroding).</span><span class="sxs-lookup"><span data-stu-id="695a5-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="695a5-110">O CLSID para esse efeito é CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="695a5-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="695a5-111">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="695a5-111">Example images</span></span>

<span data-ttu-id="695a5-112">Este exemplo mostra a saída do efeito ao usar o modo Erode.</span><span class="sxs-lookup"><span data-stu-id="695a5-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="695a5-113">Antes</span><span class="sxs-lookup"><span data-stu-id="695a5-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| <span data-ttu-id="695a5-115">After (após)</span><span class="sxs-lookup"><span data-stu-id="695a5-115">After</span></span>                                                      |
| ![a imagem após a transformação.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="695a5-117">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="695a5-117">Effect properties</span></span>



| <span data-ttu-id="695a5-118">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="695a5-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="695a5-119">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="695a5-119">Type and default value</span></span>                                                     | <span data-ttu-id="695a5-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="695a5-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695a5-121">Mode</span><span class="sxs-lookup"><span data-stu-id="695a5-121">Mode</span></span><br/> <span data-ttu-id="695a5-122">\_Modo de \_ prop d2d1 MORPHOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="695a5-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="695a5-123">\_Modo de MORPHOLOGY d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="695a5-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="695a5-124">\_Modo d2d1 \_ MORPHOLOGY \_ Erode</span><span class="sxs-lookup"><span data-stu-id="695a5-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="695a5-125">O modo morphology.</span><span class="sxs-lookup"><span data-stu-id="695a5-125">The morphology mode.</span></span> <span data-ttu-id="695a5-126">Os modos disponíveis são Erode (achatar) e tardia (THICKEN).</span><span class="sxs-lookup"><span data-stu-id="695a5-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="695a5-127">Consulte [modos de morphology](#morphology-modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="695a5-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="695a5-128">Largura</span><span class="sxs-lookup"><span data-stu-id="695a5-128">Width</span></span><br/> <span data-ttu-id="695a5-129">\_Largura de \_ prop d2d1 MORPHOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="695a5-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="695a5-130">UINT</span><span class="sxs-lookup"><span data-stu-id="695a5-130">UINT</span></span><br/> <span data-ttu-id="695a5-131">1</span><span class="sxs-lookup"><span data-stu-id="695a5-131">1</span></span><br/>                                               | <span data-ttu-id="695a5-132">Tamanho do kernel na direção X.</span><span class="sxs-lookup"><span data-stu-id="695a5-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="695a5-133">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="695a5-133">The units are in DIPs.</span></span> <span data-ttu-id="695a5-134">Os valores devem estar entre 1 e 100, inclusive.</span><span class="sxs-lookup"><span data-stu-id="695a5-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="695a5-135">Altura</span><span class="sxs-lookup"><span data-stu-id="695a5-135">Height</span></span><br/> <span data-ttu-id="695a5-136">\_Altura de \_ prop d2d1 MORPHOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="695a5-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="695a5-137">UINT</span><span class="sxs-lookup"><span data-stu-id="695a5-137">UINT</span></span><br/> <span data-ttu-id="695a5-138">1</span><span class="sxs-lookup"><span data-stu-id="695a5-138">1</span></span><br/>                                               | <span data-ttu-id="695a5-139">Tamanho do kernel na direção Y.</span><span class="sxs-lookup"><span data-stu-id="695a5-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="695a5-140">As unidades estão em DIPs.</span><span class="sxs-lookup"><span data-stu-id="695a5-140">The units are in DIPs.</span></span> <span data-ttu-id="695a5-141">Os valores devem estar entre 1 e 100, inclusive.</span><span class="sxs-lookup"><span data-stu-id="695a5-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="695a5-142">Modos de morphology</span><span class="sxs-lookup"><span data-stu-id="695a5-142">Morphology modes</span></span>



| <span data-ttu-id="695a5-143">Name</span><span class="sxs-lookup"><span data-stu-id="695a5-143">Name</span></span>                           | <span data-ttu-id="695a5-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="695a5-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="695a5-145">\_Modo d2d1 \_ MORPHOLOGY \_ Erode</span><span class="sxs-lookup"><span data-stu-id="695a5-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="695a5-146">O valor máximo de cada canal RGB no kernel é usado.</span><span class="sxs-lookup"><span data-stu-id="695a5-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="695a5-147">D2D1 \_ \_ modo MORPHOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="695a5-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="695a5-148">O valor mínimo de cada canal RGB no kernel é usado.</span><span class="sxs-lookup"><span data-stu-id="695a5-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="695a5-149">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="695a5-149">Output bitmap</span></span>

<span data-ttu-id="695a5-150">Para o modo de atraso, o tamanho do bitmap de saída aumenta:</span><span class="sxs-lookup"><span data-stu-id="695a5-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="695a5-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="695a5-151">Requirement</span></span> | <span data-ttu-id="695a5-152">Valor</span><span class="sxs-lookup"><span data-stu-id="695a5-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="695a5-153">Crescimento do bitmap de saída X =</span><span class="sxs-lookup"><span data-stu-id="695a5-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="695a5-154">INT (FLOAT (Width) \* ((User DPI)/96))</span><span class="sxs-lookup"><span data-stu-id="695a5-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="695a5-155">Crescimento de bitmap de saída Y =</span><span class="sxs-lookup"><span data-stu-id="695a5-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="695a5-156">INT (FLOAT (Height) \* ((DPI do usuário)/96))</span><span class="sxs-lookup"><span data-stu-id="695a5-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="695a5-157">Para o modo ERODE, o tamanho do bitmap de saída é reduzido:</span><span class="sxs-lookup"><span data-stu-id="695a5-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="695a5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="695a5-158">Requirement</span></span> | <span data-ttu-id="695a5-159">Valor</span><span class="sxs-lookup"><span data-stu-id="695a5-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="695a5-160">Crescimento do bitmap de saída X =</span><span class="sxs-lookup"><span data-stu-id="695a5-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="695a5-161">INT (FLOAT (-Width) \* ((User DPI)/96))</span><span class="sxs-lookup"><span data-stu-id="695a5-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="695a5-162">Crescimento de bitmap de saída Y =</span><span class="sxs-lookup"><span data-stu-id="695a5-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="695a5-163">INT (FLOAT (-Height) \* ((User DPI)/96))</span><span class="sxs-lookup"><span data-stu-id="695a5-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="695a5-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="695a5-164">Requirements</span></span>



| <span data-ttu-id="695a5-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="695a5-165">Requirement</span></span> | <span data-ttu-id="695a5-166">Valor</span><span class="sxs-lookup"><span data-stu-id="695a5-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="695a5-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="695a5-167">Minimum supported client</span></span> | <span data-ttu-id="695a5-168">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="695a5-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="695a5-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="695a5-169">Minimum supported server</span></span> | <span data-ttu-id="695a5-170">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="695a5-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="695a5-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="695a5-171">Header</span></span>                   | <span data-ttu-id="695a5-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="695a5-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="695a5-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="695a5-173">Library</span></span>                  | <span data-ttu-id="695a5-174">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="695a5-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="695a5-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="695a5-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695a5-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="695a5-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

