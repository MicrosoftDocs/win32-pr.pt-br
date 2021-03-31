---
title: Efeito de escala de cinza
description: Converte uma imagem em cinza monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644767"
---
# <a name="grayscale-effect"></a><span data-ttu-id="91cb2-103">Efeito de escala de cinza</span><span class="sxs-lookup"><span data-stu-id="91cb2-103">Grayscale effect</span></span>

<span data-ttu-id="91cb2-104">Converte uma imagem em cinza monocromático.</span><span class="sxs-lookup"><span data-stu-id="91cb2-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="91cb2-105">A escala de cinza usa o efeito de matriz de cores para converter em escala de cinza, usando a seguinte matriz:</span><span class="sxs-lookup"><span data-stu-id="91cb2-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![matriz de conversão](images/grayscale-effect-matrix.png)

<span data-ttu-id="91cb2-107">O CLSID para esse efeito é CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="91cb2-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="91cb2-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="91cb2-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="91cb2-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="91cb2-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="91cb2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91cb2-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="91cb2-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91cb2-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="91cb2-112">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="91cb2-112">Example image</span></span>

![exemplo de saída de efeito](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="91cb2-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="91cb2-114">Effect properties</span></span>

<span data-ttu-id="91cb2-115">Esse efeito não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="91cb2-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="91cb2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91cb2-116">Requirements</span></span>



| <span data-ttu-id="91cb2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91cb2-117">Requirement</span></span> | <span data-ttu-id="91cb2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="91cb2-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="91cb2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91cb2-119">Minimum supported client</span></span> | <span data-ttu-id="91cb2-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="91cb2-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="91cb2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91cb2-121">Minimum supported server</span></span> | <span data-ttu-id="91cb2-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="91cb2-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="91cb2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91cb2-123">Header</span></span>                   | <span data-ttu-id="91cb2-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="91cb2-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="91cb2-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91cb2-125">Library</span></span>                  | <span data-ttu-id="91cb2-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="91cb2-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="91cb2-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91cb2-127">Related topics</span></span>

* [<span data-ttu-id="91cb2-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="91cb2-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
