---
description: Transição de chave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transição de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825609"
---
# <a name="key-transition"></a><span data-ttu-id="2ddf5-103">Transição de chave</span><span class="sxs-lookup"><span data-stu-id="2ddf5-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="2ddf5-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-104">\[Deprecated.</span></span> <span data-ttu-id="2ddf5-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ddf5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2ddf5-106">A transição de chave executa a criação de chaves com base no valor RGB, no valor alfa, no matiz ou na luminância.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="2ddf5-107">A imagem a seguir mostra a transição de chave:</span><span class="sxs-lookup"><span data-stu-id="2ddf5-107">The following image shows the key transition:</span></span>

![transição de chave](images/trans-key.png)

<span data-ttu-id="2ddf5-109">ID de classe (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="2ddf5-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="2ddf5-110">Nome da variável CLSID: CLSID \_ DxtKey</span><span class="sxs-lookup"><span data-stu-id="2ddf5-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="2ddf5-111">Nome amigável: "DxtKey"</span><span class="sxs-lookup"><span data-stu-id="2ddf5-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="2ddf5-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ddf5-112">Properties</span></span>



| <span data-ttu-id="2ddf5-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2ddf5-113">Property</span></span>   | <span data-ttu-id="2ddf5-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ddf5-114">Type</span></span>  | <span data-ttu-id="2ddf5-115">Intervalo válido</span><span class="sxs-lookup"><span data-stu-id="2ddf5-115">Valid range</span></span>           | <span data-ttu-id="2ddf5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ddf5-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="2ddf5-117">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="2ddf5-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2ddf5-118">Matiz</span><span class="sxs-lookup"><span data-stu-id="2ddf5-118">Hue</span></span>        | <span data-ttu-id="2ddf5-119">INT</span><span class="sxs-lookup"><span data-stu-id="2ddf5-119">int</span></span>   | <span data-ttu-id="2ddf5-120">0 – 360</span><span class="sxs-lookup"><span data-stu-id="2ddf5-120">0–360</span></span>                 | <span data-ttu-id="2ddf5-121">O valor de matiz para o qual fazer a chave.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2ddf5-122">Matiz</span><span class="sxs-lookup"><span data-stu-id="2ddf5-122">Hue</span></span>                            |
| <span data-ttu-id="2ddf5-123">Invert</span><span class="sxs-lookup"><span data-stu-id="2ddf5-123">Invert</span></span>     | <span data-ttu-id="2ddf5-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="2ddf5-124">BOOL</span></span>  | <span data-ttu-id="2ddf5-125">**False** ou **true**</span><span class="sxs-lookup"><span data-stu-id="2ddf5-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="2ddf5-126">Valor booliano que indica se a operação padrão da chave deve ser invertida.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="2ddf5-127">Se **for false**, os pixels na imagem subjacente serão tornados transparentes da maneira padrão.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="2ddf5-128">Se **for true**, a operação inverterá.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="2ddf5-129">Croma, matiz, luminância, Nonred</span><span class="sxs-lookup"><span data-stu-id="2ddf5-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="2ddf5-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="2ddf5-130">KeyType</span></span>    | <span data-ttu-id="2ddf5-131">INT</span><span class="sxs-lookup"><span data-stu-id="2ddf5-131">int</span></span>   | <span data-ttu-id="2ddf5-132">Ver comentários</span><span class="sxs-lookup"><span data-stu-id="2ddf5-132">See Remarks</span></span>           | <span data-ttu-id="2ddf5-133">Especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-133">Specifies the type of key.</span></span> <span data-ttu-id="2ddf5-134">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="2ddf5-135">Todos</span><span class="sxs-lookup"><span data-stu-id="2ddf5-135">All</span></span>                            |
| <span data-ttu-id="2ddf5-136">Luminância</span><span class="sxs-lookup"><span data-stu-id="2ddf5-136">Luminance</span></span>  | <span data-ttu-id="2ddf5-137">INT</span><span class="sxs-lookup"><span data-stu-id="2ddf5-137">int</span></span>   | <span data-ttu-id="2ddf5-138">0 – 100</span><span class="sxs-lookup"><span data-stu-id="2ddf5-138">0–100</span></span>                 | <span data-ttu-id="2ddf5-139">O valor de luminância para a chave.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="2ddf5-140">Luminância</span><span class="sxs-lookup"><span data-stu-id="2ddf5-140">Luminance</span></span>                      |
| <span data-ttu-id="2ddf5-141">RGB</span><span class="sxs-lookup"><span data-stu-id="2ddf5-141">RGB</span></span>        | <span data-ttu-id="2ddf5-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="2ddf5-142">DWORD</span></span> | <span data-ttu-id="2ddf5-143">0x0 – 0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="2ddf5-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="2ddf5-144">A cor na qual se deve ser a chave.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-144">The color on which to key.</span></span> <span data-ttu-id="2ddf5-145">O valor é um número hexadecimal com o formato 0x *RRGGBB*, em que *RR* é o valor vermelho, *gg* é o valor verde e *BB* é o valor azul.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="2ddf5-146">(Vermelho puro, verde e azul são 0xFF0000, 0x00FF00 e 0x0000FF, respectivamente.)</span><span class="sxs-lookup"><span data-stu-id="2ddf5-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="2ddf5-147">Croma</span><span class="sxs-lookup"><span data-stu-id="2ddf5-147">Chroma</span></span>                         |
| <span data-ttu-id="2ddf5-148">Similaridade</span><span class="sxs-lookup"><span data-stu-id="2ddf5-148">Similarity</span></span> | <span data-ttu-id="2ddf5-149">INT</span><span class="sxs-lookup"><span data-stu-id="2ddf5-149">int</span></span>   | <span data-ttu-id="2ddf5-150">0 – 100</span><span class="sxs-lookup"><span data-stu-id="2ddf5-150">0–100</span></span>                 | <span data-ttu-id="2ddf5-151">O intervalo de dados de cores que se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="2ddf5-152">Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="2ddf5-153">Croma, Nonred</span><span class="sxs-lookup"><span data-stu-id="2ddf5-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="2ddf5-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddf5-154">Remarks</span></span>

<span data-ttu-id="2ddf5-155">O tipo de chave executada depende do valor da propriedade **KeyType** , que deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="2ddf5-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="2ddf5-156">Valor</span><span class="sxs-lookup"><span data-stu-id="2ddf5-156">Value</span></span> | <span data-ttu-id="2ddf5-157">Enumeração</span><span class="sxs-lookup"><span data-stu-id="2ddf5-157">Enumeration</span></span>       | <span data-ttu-id="2ddf5-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ddf5-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2ddf5-159">0</span><span class="sxs-lookup"><span data-stu-id="2ddf5-159">0</span></span>     | <span data-ttu-id="2ddf5-160">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="2ddf5-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="2ddf5-161">Chave croma (chave por valor RGB).</span><span class="sxs-lookup"><span data-stu-id="2ddf5-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="2ddf5-162">1</span><span class="sxs-lookup"><span data-stu-id="2ddf5-162">1</span></span>     | <span data-ttu-id="2ddf5-163">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="2ddf5-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="2ddf5-164">Chave Nonred.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-164">Nonred key.</span></span> <span data-ttu-id="2ddf5-165">(Torna as áreas azul e verde transparentes.)</span><span class="sxs-lookup"><span data-stu-id="2ddf5-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="2ddf5-166">2</span><span class="sxs-lookup"><span data-stu-id="2ddf5-166">2</span></span>     | <span data-ttu-id="2ddf5-167">luminância de DXTKEY \_</span><span class="sxs-lookup"><span data-stu-id="2ddf5-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="2ddf5-168">Chave de luminância.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="2ddf5-169">3</span><span class="sxs-lookup"><span data-stu-id="2ddf5-169">3</span></span>     | <span data-ttu-id="2ddf5-170">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="2ddf5-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="2ddf5-171">Chave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="2ddf5-172">4</span><span class="sxs-lookup"><span data-stu-id="2ddf5-172">4</span></span>     | <span data-ttu-id="2ddf5-173">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="2ddf5-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="2ddf5-174">Chave por matiz.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="2ddf5-175">O tipo de chave usa como padrão DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="2ddf5-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



