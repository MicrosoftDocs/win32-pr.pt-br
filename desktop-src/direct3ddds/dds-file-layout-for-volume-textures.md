---
title: Exemplo de textura de volume DDS
description: Para uma textura de volume, use o \_ volume complexo DDSCAPS, DDSCAPS2 \_ , DDSD \_ , flags e set e dwDepth. Uma textura de volume é uma extensão de uma textura padrão para o Direct3D 9; uma textura de volume pode ser definida com ou sem mipmaps.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812306"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="6e9c9-104">Exemplo de textura de volume DDS</span><span class="sxs-lookup"><span data-stu-id="6e9c9-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="6e9c9-105">Para uma textura de volume, use o \_ volume complexo DDSCAPS, DDSCAPS2 \_ , DDSD \_ , flags e set e dwDepth.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="6e9c9-106">Uma textura de volume é uma extensão de uma textura padrão para o Direct3D 9; uma textura de volume pode ser definida com ou sem mipmaps.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="6e9c9-107">Para volumes sem mipmaps, cada fatia de profundidade é gravada no arquivo em ordem.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="6e9c9-108">Se mipmaps forem incluídas, todas as fatias de profundidade para um determinado nível de mipmap serão escritas em conjunto, com cada nível contendo metade de fatias do nível anterior, com um mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="6e9c9-109">Por exemplo, um mapa de volume 64-por-64-by-4 usando um formato de pixel de R8G8B8 (3 bytes por pixel) com todos os níveis de mipmap teria o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6e9c9-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="6e9c9-110">Componentes do DDS</span><span class="sxs-lookup"><span data-stu-id="6e9c9-110">DDS Components</span></span>                      | <span data-ttu-id="6e9c9-111">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="6e9c9-112">header</span><span class="sxs-lookup"><span data-stu-id="6e9c9-112">header</span></span>                              | <span data-ttu-id="6e9c9-113">128 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-113">128 bytes</span></span>   |
| <span data-ttu-id="6e9c9-114">64-por-64 fatia 1 de 4 imagem principal.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="6e9c9-115">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-115">12288 bytes</span></span> |
| <span data-ttu-id="6e9c9-116">64-por-64 fatia 2 de 4 imagem principal.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="6e9c9-117">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-117">12288 bytes</span></span> |
| <span data-ttu-id="6e9c9-118">64-por-64 fatia 3 de 4 imagem principal.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="6e9c9-119">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-119">12288 bytes</span></span> |
| <span data-ttu-id="6e9c9-120">64-por-64 fatia 4 de 4 imagem principal.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="6e9c9-121">12288 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-121">12288 bytes</span></span> |
| <span data-ttu-id="6e9c9-122">32-por-32 fatia 1 de 2 mipmap imagem.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="6e9c9-123">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-123">3072 bytes</span></span>  |
| <span data-ttu-id="6e9c9-124">32-por-32 fatia 2 de 2 mipmap Image.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="6e9c9-125">3072 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-125">3072 bytes</span></span>  |
| <span data-ttu-id="6e9c9-126">16-por-16 fatia 1 de 1 imagem mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="6e9c9-127">768 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-127">768 bytes</span></span>   |
| <span data-ttu-id="6e9c9-128">8-por-8 fatia 1 de 1 imagem de mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="6e9c9-129">192 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-129">192 bytes</span></span>   |
| <span data-ttu-id="6e9c9-130">4-by-4 fatia 1 de 1 imagem mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="6e9c9-131">48 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-131">48 bytes</span></span>    |
| <span data-ttu-id="6e9c9-132">2-por-2 fatia 1 de 1 imagem mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="6e9c9-133">12 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-133">12 bytes</span></span>    |
| <span data-ttu-id="6e9c9-134">1-por-1 fatia 1 de 1 imagem mipmap.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="6e9c9-135">3 bytes</span><span class="sxs-lookup"><span data-stu-id="6e9c9-135">3 bytes</span></span>     |



 

<span data-ttu-id="6e9c9-136">Observe que o menor nível de mipmap é de apenas 3 bytes porque o BitCount é 24 e não há nenhuma compactação adicional nesse nível.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="6e9c9-137">O suporte para texturas de volume foi adicionado no DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="6e9c9-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e9c9-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e9c9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e9c9-139">Guia de programação para DDS</span><span class="sxs-lookup"><span data-stu-id="6e9c9-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




