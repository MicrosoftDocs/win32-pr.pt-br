---
title: Efeito de metadados de opacidade
description: Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, para que as otimizações de renderização internas para o grafo sejam possíveis.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086145"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="88efe-103">Efeito de metadados de opacidade</span><span class="sxs-lookup"><span data-stu-id="88efe-103">Opacity metadata effect</span></span>

<span data-ttu-id="88efe-104">Você pode usar esse efeito para marcar uma área de uma imagem de entrada como opaca, para que as otimizações de renderização internas para o grafo sejam possíveis.</span><span class="sxs-lookup"><span data-stu-id="88efe-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="88efe-105">Esse efeito não modifica a imagem em si para ser opaco.</span><span class="sxs-lookup"><span data-stu-id="88efe-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="88efe-106">Ele modifica os dados associados à imagem para que o renderizador assuma que a região especificada é opaca.</span><span class="sxs-lookup"><span data-stu-id="88efe-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="88efe-107">O CLSID para esse efeito é CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="88efe-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="88efe-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="88efe-108">Effect properties</span></span>



| <span data-ttu-id="88efe-109">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="88efe-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="88efe-110">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="88efe-110">Type and default value</span></span>                                                             | <span data-ttu-id="88efe-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="88efe-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88efe-112">OutputRect</span><span class="sxs-lookup"><span data-stu-id="88efe-112">OutputRect</span></span><br/> <span data-ttu-id="88efe-113">D2D1 \_ OPACITYMETADATA \_ propu \_ entrada \_ opaca com \_ Rect</span><span class="sxs-lookup"><span data-stu-id="88efe-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="88efe-114">\_4F de vetor d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="88efe-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="88efe-115">(-FLT \_ MAX,-FLT \_ Max, FLT \_ Max, FLT \_ Max)</span><span class="sxs-lookup"><span data-stu-id="88efe-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="88efe-116">A parte da imagem de origem opaca.</span><span class="sxs-lookup"><span data-stu-id="88efe-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="88efe-117">O padrão é a imagem de entrada inteira.</span><span class="sxs-lookup"><span data-stu-id="88efe-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="88efe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88efe-118">Requirements</span></span>



| <span data-ttu-id="88efe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88efe-119">Requirement</span></span> | <span data-ttu-id="88efe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="88efe-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88efe-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88efe-121">Minimum supported client</span></span> | <span data-ttu-id="88efe-122">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="88efe-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="88efe-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88efe-123">Minimum supported server</span></span> | <span data-ttu-id="88efe-124">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="88efe-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="88efe-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88efe-125">Header</span></span>                   | <span data-ttu-id="88efe-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="88efe-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="88efe-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88efe-127">Library</span></span>                  | <span data-ttu-id="88efe-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="88efe-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="88efe-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88efe-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88efe-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="88efe-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

