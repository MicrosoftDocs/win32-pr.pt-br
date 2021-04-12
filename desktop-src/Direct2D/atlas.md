---
title: Efeito do Atlas
description: Você pode usar esse efeito para gerar uma parte de uma imagem, mas manter a região fora da parte para uso em operações subsequentes.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455652"
---
# <a name="atlas-effect"></a><span data-ttu-id="0860c-103">Efeito do Atlas</span><span class="sxs-lookup"><span data-stu-id="0860c-103">Atlas effect</span></span>

<span data-ttu-id="0860c-104">Você pode usar esse efeito para gerar uma parte de uma imagem, mas manter a região fora da parte para uso em operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0860c-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="0860c-105">O CLSID para esse efeito é CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="0860c-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="0860c-106">O efeito do Atlas será útil se você quiser carregar uma imagem grande composta por muitas imagens menores, como vários quadros de um Sprite.</span><span class="sxs-lookup"><span data-stu-id="0860c-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="0860c-107">Para criar a saída do efeito:</span><span class="sxs-lookup"><span data-stu-id="0860c-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="0860c-108">Corta a entrada para a propriedade *InputRect* fornecida.</span><span class="sxs-lookup"><span data-stu-id="0860c-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="0860c-109">Traduz a origem do resultado para (0, 0).</span><span class="sxs-lookup"><span data-stu-id="0860c-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="0860c-110">A propriedade *InputPaddingRect* só deverá ser maior se e somente se os pixels entre os dois retângulos forem transparentes em preto na entrada.</span><span class="sxs-lookup"><span data-stu-id="0860c-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="0860c-111">Isso pode resultar em Direct2D executando o grafo de forma mais ideal.</span><span class="sxs-lookup"><span data-stu-id="0860c-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="0860c-112">Aqui está um exemplo do efeito.</span><span class="sxs-lookup"><span data-stu-id="0860c-112">Here is an example of the effect.</span></span> <span data-ttu-id="0860c-113">Essa imagem é pequena e simples para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="0860c-113">This image is small and simple for illustration purposes.</span></span>

![imagem de entrada.](images/atlas.png)

<span data-ttu-id="0860c-115">A imagem anterior é a entrada para o efeito.</span><span class="sxs-lookup"><span data-stu-id="0860c-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="0860c-116">O código aqui cria um efeito do Atlas, define a entrada, define o retângulo de entrada e, em seguida, desenha a saída.</span><span class="sxs-lookup"><span data-stu-id="0860c-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="0860c-117">O código anterior seleciona um retângulo que está ao seu lado no segundo triângulo.</span><span class="sxs-lookup"><span data-stu-id="0860c-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="0860c-118">O preenchimento em volta dele é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0860c-118">The padding around it is ignored.</span></span> <span data-ttu-id="0860c-119">Aqui está a imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="0860c-119">Here is the resulting image.</span></span>

![imagem de saída.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="0860c-121">Essa é uma situação em que você pode optar por especificar um *InputPaddingRect* porque o preenchimento é preto transparente.</span><span class="sxs-lookup"><span data-stu-id="0860c-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="0860c-122">O retângulo seria `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="0860c-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="0860c-123">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="0860c-123">Effect properties</span></span>



| <span data-ttu-id="0860c-124">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="0860c-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="0860c-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0860c-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0860c-126">InputRect</span><span class="sxs-lookup"><span data-stu-id="0860c-126">InputRect</span></span><br/> <span data-ttu-id="0860c-127">\_Rect de \_ entrada de prop \_ \_ do d2d1 Atlas</span><span class="sxs-lookup"><span data-stu-id="0860c-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="0860c-128">A parte da imagem foi passada para o próximo efeito.</span><span class="sxs-lookup"><span data-stu-id="0860c-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="0860c-129">Type é D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="0860c-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="0860c-130">O valor padrão é (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).</span><span class="sxs-lookup"><span data-stu-id="0860c-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="0860c-131">InputPaddingRect</span><span class="sxs-lookup"><span data-stu-id="0860c-131">InputPaddingRect</span></span><br/> <span data-ttu-id="0860c-132">\_Preenchimento de \_ entrada de prop d2d1 Atlas \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0860c-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="0860c-133">O tamanho máximo de amostra para o retângulo de saída.</span><span class="sxs-lookup"><span data-stu-id="0860c-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="0860c-134">Type é D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="0860c-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="0860c-135">O valor padrão é (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).</span><span class="sxs-lookup"><span data-stu-id="0860c-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="0860c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0860c-136">Requirements</span></span>



| <span data-ttu-id="0860c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0860c-137">Requirement</span></span> | <span data-ttu-id="0860c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0860c-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0860c-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0860c-139">Minimum supported client</span></span> | <span data-ttu-id="0860c-140">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0860c-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0860c-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0860c-141">Minimum supported server</span></span> | <span data-ttu-id="0860c-142">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0860c-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0860c-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0860c-143">Header</span></span>                   | <span data-ttu-id="0860c-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0860c-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0860c-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0860c-145">Library</span></span>                  | <span data-ttu-id="0860c-146">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0860c-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0860c-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0860c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0860c-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0860c-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

