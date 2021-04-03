---
description: Efeito de setter alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efeito de setter alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645867"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="d1d8a-103">Efeito de setter alfa</span><span class="sxs-lookup"><span data-stu-id="d1d8a-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="d1d8a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-104">\[Deprecated.</span></span> <span data-ttu-id="d1d8a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1d8a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d1d8a-106">O efeito de setter alfa define os bits alfa em uma imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="d1d8a-107">ID de classe (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="d1d8a-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="d1d8a-108">Nome da variável CLSID: CLSID \_ DxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="d1d8a-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="d1d8a-109">Nome amigável: "DxtAlphaSetter"</span><span class="sxs-lookup"><span data-stu-id="d1d8a-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="d1d8a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1d8a-110">Properties</span></span>



| <span data-ttu-id="d1d8a-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d1d8a-111">Property</span></span>  | <span data-ttu-id="d1d8a-112">Type</span><span class="sxs-lookup"><span data-stu-id="d1d8a-112">Type</span></span>   | <span data-ttu-id="d1d8a-113">Padrão</span><span class="sxs-lookup"><span data-stu-id="d1d8a-113">Default</span></span> | <span data-ttu-id="d1d8a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1d8a-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="d1d8a-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="d1d8a-115">Alpha</span></span>     | <span data-ttu-id="d1d8a-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="d1d8a-116">BYTE</span></span>   | <span data-ttu-id="d1d8a-117">-1</span><span class="sxs-lookup"><span data-stu-id="d1d8a-117">-1</span></span>      | <span data-ttu-id="d1d8a-118">Define o alfa para a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="d1d8a-119">AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="d1d8a-119">AlphaRamp</span></span> | <span data-ttu-id="d1d8a-120">double</span><span class="sxs-lookup"><span data-stu-id="d1d8a-120">double</span></span> | <span data-ttu-id="d1d8a-121">-1,0</span><span class="sxs-lookup"><span data-stu-id="d1d8a-121">-1.0</span></span>    | <span data-ttu-id="d1d8a-122">Define o alfa como um percentual do valor alfa original.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1d8a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d8a-123">Remarks</span></span>

<span data-ttu-id="d1d8a-124">Uma propriedade com um valor negativo é ignorada.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="d1d8a-125">Apenas uma propriedade pode ter um valor não negativo.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="d1d8a-126">A propriedade Alpha especifica um valor alfa constante para cada pixel na imagem.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="d1d8a-127">Essa propriedade substitui os valores Alfa da imagem original.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="d1d8a-128">A propriedade AlphaRamp especifica o valor alfa de cada pixel como uma porcentagem do valor original do pixel, de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d1d8a-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1d8a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1d8a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d8a-130">Mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="d1d8a-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



