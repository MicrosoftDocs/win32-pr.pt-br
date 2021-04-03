---
title: Efeito de compensação de DPI
description: Use o efeito de compensação de DPI para ajustar automaticamente um bitmap de entrada para corresponder ao DPI do contexto. Isso é útil para situações em que um bitmap é criado ou carregado em um DPI diferente da tela.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824833"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="ea9e4-104">Efeito de compensação de DPI</span><span class="sxs-lookup"><span data-stu-id="ea9e4-104">DPI compensation effect</span></span>

<span data-ttu-id="ea9e4-105">Use o efeito de compensação de DPI para ajustar automaticamente um bitmap de entrada para corresponder ao DPI do contexto.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="ea9e4-106">Isso é útil para situações em que um bitmap é criado ou carregado em um DPI diferente da tela.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="ea9e4-107">O CLSID para esse efeito é CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ea9e4-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="ea9e4-108">Effect properties</span></span>



| <span data-ttu-id="ea9e4-109">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="ea9e4-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="ea9e4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea9e4-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9e4-111">Interpolação</span><span class="sxs-lookup"><span data-stu-id="ea9e4-111">InterpolationMode</span></span><br/> <span data-ttu-id="ea9e4-112">\_Modo de \_ \_ interpolação de prop d2d1 DPICOMPENSATION \_</span><span class="sxs-lookup"><span data-stu-id="ea9e4-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="ea9e4-113">O modo de interpolação que o efeito usa para dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="ea9e4-114">O tipo é o \_ \_ modo de interpolação d2d1 DPICOMPENSATION \_ .</span><span class="sxs-lookup"><span data-stu-id="ea9e4-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="ea9e4-115">O valor padrão é D2D1 \_ DPICOMPENSATION \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="ea9e4-116">Bordermode</span><span class="sxs-lookup"><span data-stu-id="ea9e4-116">BorderMode</span></span><br/> <span data-ttu-id="ea9e4-117">\_Modo de \_ borda de prop d2d1 DPICOMPENSATION \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea9e4-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="ea9e4-118">O modo usado para calcular a borda da imagem, suave ou difícil.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="ea9e4-119">Consulte [modos de borda](https://www.bing.com/search?q=Border+modes) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="ea9e4-120">O tipo é o \_ modo de borda d2d1 \_ .</span><span class="sxs-lookup"><span data-stu-id="ea9e4-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="ea9e4-121">O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ea9e4-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="ea9e4-122">InputDpi</span><span class="sxs-lookup"><span data-stu-id="ea9e4-122">InputDpi</span></span><br/> <span data-ttu-id="ea9e4-123">\_Dpi de entrada d2d1 DPICOMPENSATION \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea9e4-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="ea9e4-124">O DPI da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="ea9e4-125">O tipo é FLOAT.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="ea9e4-126">O valor padrão é 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="ea9e4-127">Modos de interpolação</span><span class="sxs-lookup"><span data-stu-id="ea9e4-127">Interpolation modes</span></span>



| <span data-ttu-id="ea9e4-128">Enumeração</span><span class="sxs-lookup"><span data-stu-id="ea9e4-128">Enumeration</span></span>                                                       | <span data-ttu-id="ea9e4-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea9e4-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9e4-130">D2D1 \_ DPICOMPENSATION \_ modo de interpolação \_ \_ mais próximo \_</span><span class="sxs-lookup"><span data-stu-id="ea9e4-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="ea9e4-131">Amostra o ponto único mais próximo e o usa.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="ea9e4-132">Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="ea9e4-133">\_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="ea9e4-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="ea9e4-134">Usa uma amostra de quatro pontos e uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="ea9e4-135">Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="ea9e4-136">\_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="ea9e4-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="ea9e4-137">Usa um kernel cúbico de 16 amostras para interpolação.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="ea9e4-138">Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="ea9e4-139">\_Modo de \_ interpolação d2d1 DPICOMPENSATION com \_ \_ várias \_ amostras \_ lineares</span><span class="sxs-lookup"><span data-stu-id="ea9e4-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="ea9e4-140">Usa quatro amostras lineares em um único pixel para suavização de multialias de borda.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="ea9e4-141">Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="ea9e4-142">\_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="ea9e4-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="ea9e4-143">Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="ea9e4-144">\_Modo de \_ interpolação d2d1 DPICOMPENSATION de \_ \_ alta \_ qualidade \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="ea9e4-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="ea9e4-145">Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="ea9e4-146">Em seguida, usa o modo de interpolação cúbica para a saída final.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ea9e4-147">Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ DPICOMPENSTION \_ modo de interpolação \_ \_ linear.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="ea9e4-148">Modos de borda</span><span class="sxs-lookup"><span data-stu-id="ea9e4-148">Border modes</span></span>



| <span data-ttu-id="ea9e4-149">Nome</span><span class="sxs-lookup"><span data-stu-id="ea9e4-149">Name</span></span>                     | <span data-ttu-id="ea9e4-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea9e4-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9e4-151">\_Modo de borda d2d1 \_ \_ Soft</span><span class="sxs-lookup"><span data-stu-id="ea9e4-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="ea9e4-152">Os pixels fora dos limites de entrada são gerados pelo [efeito de borda de espelho](border.md).</span><span class="sxs-lookup"><span data-stu-id="ea9e4-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="ea9e4-153">\_Modo de borda d2d1 \_ \_ Hard</span><span class="sxs-lookup"><span data-stu-id="ea9e4-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="ea9e4-154">Os pixels fora dos limites de entrada são pretos transparentes.</span><span class="sxs-lookup"><span data-stu-id="ea9e4-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="ea9e4-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea9e4-155">Requirements</span></span>



| <span data-ttu-id="ea9e4-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea9e4-156">Requirement</span></span> | <span data-ttu-id="ea9e4-157">Valor</span><span class="sxs-lookup"><span data-stu-id="ea9e4-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9e4-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea9e4-158">Minimum supported client</span></span> | <span data-ttu-id="ea9e4-159">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ea9e4-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ea9e4-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea9e4-160">Minimum supported server</span></span> | <span data-ttu-id="ea9e4-161">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ea9e4-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ea9e4-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea9e4-162">Header</span></span>                   | <span data-ttu-id="ea9e4-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ea9e4-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ea9e4-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea9e4-164">Library</span></span>                  | <span data-ttu-id="ea9e4-165">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ea9e4-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ea9e4-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea9e4-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9e4-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ea9e4-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

