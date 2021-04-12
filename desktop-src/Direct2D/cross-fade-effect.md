---
title: Efeito de esmaecimento cruzado
description: Esse efeito combina duas imagens adicionando pixels ponderados de imagens de entrada. Ele tem duas entradas, chamadas de destino e origem.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499358"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="48484-104">Efeito de esmaecimento cruzado</span><span class="sxs-lookup"><span data-stu-id="48484-104">Cross-fade effect</span></span>

<span data-ttu-id="48484-105">Esse efeito combina duas imagens adicionando pixels ponderados de imagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="48484-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="48484-106">Ele tem duas entradas, chamadas de destino e origem.</span><span class="sxs-lookup"><span data-stu-id="48484-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="48484-107">A fórmula de esmaecimento cruzada é **saída = \* destino de peso + (1-peso) \* fonte**.</span><span class="sxs-lookup"><span data-stu-id="48484-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="48484-108">O CLSID para esse efeito é CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="48484-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="48484-109">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="48484-109">Effect properties</span></span>

| <span data-ttu-id="48484-110">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="48484-110">Display name and index enumeration</span></span>             | <span data-ttu-id="48484-111">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="48484-111">Type and default value</span></span> | <span data-ttu-id="48484-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="48484-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48484-113">\_Peso de prop WeightD2D1 fading cruzado \_ \_</span><span class="sxs-lookup"><span data-stu-id="48484-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="48484-114">FLUTUAr 0,5 f</span><span class="sxs-lookup"><span data-stu-id="48484-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="48484-115">Quanto avaliar os valores de cor da imagem de origem versus a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="48484-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="48484-116">O valor mínimo é de 0,0 f (Use exclusivamente a imagem de destino para determinar a saída) e o valor máximo é 1,0 f (Use exclusivamente a imagem de origem para determinar a saída).</span><span class="sxs-lookup"><span data-stu-id="48484-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="48484-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48484-117">Requirements</span></span>



| <span data-ttu-id="48484-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48484-118">Requirement</span></span> | <span data-ttu-id="48484-119">Valor</span><span class="sxs-lookup"><span data-stu-id="48484-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="48484-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48484-120">Minimum supported client</span></span> | <span data-ttu-id="48484-121">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="48484-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48484-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48484-122">Minimum supported server</span></span> | <span data-ttu-id="48484-123">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="48484-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48484-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48484-124">Header</span></span>                   | <span data-ttu-id="48484-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="48484-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="48484-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48484-126">Library</span></span>                  | <span data-ttu-id="48484-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="48484-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="48484-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48484-128">Related topics</span></span>

* [<span data-ttu-id="48484-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="48484-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
