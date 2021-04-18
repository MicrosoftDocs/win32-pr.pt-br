---
title: Exemplo de textura DDS
description: Para uma textura não compactada, use os \_ sinalizadores DDSD pitch e DDPF \_ RGB; para uma textura compactada, use os \_ sinalizadores DDSD LINEARSIZE e DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788670"
---
# <a name="dds-texture-example"></a><span data-ttu-id="28f05-103">Exemplo de textura DDS</span><span class="sxs-lookup"><span data-stu-id="28f05-103">DDS Texture Example</span></span>

<span data-ttu-id="28f05-104">Para uma textura não compactada, use os \_ sinalizadores DDSD pitch e DDPF \_ RGB; para uma textura compactada, use os \_ sinalizadores DDSD LINEARSIZE e DDPF \_ FOURCC.</span><span class="sxs-lookup"><span data-stu-id="28f05-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="28f05-105">Para uma textura mipmapped, use os \_ sinalizadores DDSD MIPMAPCOUNT, DDSCAPS \_ MIPMAP e DDSCAPS \_ Complex também, bem como o membro de contagem MIPMAP.</span><span class="sxs-lookup"><span data-stu-id="28f05-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="28f05-106">Se mipmaps forem gerados, todos os níveis de até 1-por-1 serão normalmente gravados.</span><span class="sxs-lookup"><span data-stu-id="28f05-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="28f05-107">Para uma textura compactada, o tamanho de cada imagem de nível de mipmap normalmente é um quarto do tamanho do anterior, com um mínimo de 8 (DXT1) ou 16 (DXT2-5) bytes (para texturas quadradas).</span><span class="sxs-lookup"><span data-stu-id="28f05-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="28f05-108">Use a fórmula a seguir para calcular o tamanho de cada nível de uma textura não quadrada:</span><span class="sxs-lookup"><span data-stu-id="28f05-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="28f05-109">Esta tabela lista a quantidade de espaço ocupado por cada camada para uma textura de 256 por 256 R8G8B8, sem usar a compactação.</span><span class="sxs-lookup"><span data-stu-id="28f05-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="28f05-110">Componentes do DDS</span><span class="sxs-lookup"><span data-stu-id="28f05-110">DDS Components</span></span>          | <span data-ttu-id="28f05-111">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="28f05-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="28f05-112">header</span><span class="sxs-lookup"><span data-stu-id="28f05-112">header</span></span>                  | <span data-ttu-id="28f05-113">128</span><span class="sxs-lookup"><span data-stu-id="28f05-113">128</span></span>      |
| <span data-ttu-id="28f05-114">imagem principal de 256 por-256</span><span class="sxs-lookup"><span data-stu-id="28f05-114">256-by-256 main image</span></span>   | <span data-ttu-id="28f05-115">196608</span><span class="sxs-lookup"><span data-stu-id="28f05-115">196608</span></span>   |
| <span data-ttu-id="28f05-116">imagem de 128 por 128 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="28f05-117">49152</span><span class="sxs-lookup"><span data-stu-id="28f05-117">49152</span></span>    |
| <span data-ttu-id="28f05-118">imagem de 64 por 64 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="28f05-119">12288</span><span class="sxs-lookup"><span data-stu-id="28f05-119">12288</span></span>    |
| <span data-ttu-id="28f05-120">imagem de 32 por 32 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="28f05-121">3072</span><span class="sxs-lookup"><span data-stu-id="28f05-121">3072</span></span>     |
| <span data-ttu-id="28f05-122">imagem de 16 por 16 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="28f05-123">768</span><span class="sxs-lookup"><span data-stu-id="28f05-123">768</span></span>      |
| <span data-ttu-id="28f05-124">imagem de 8 por 8 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="28f05-125">192</span><span class="sxs-lookup"><span data-stu-id="28f05-125">192</span></span>      |
| <span data-ttu-id="28f05-126">imagem mipmap de 4 por 4</span><span class="sxs-lookup"><span data-stu-id="28f05-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="28f05-127">48</span><span class="sxs-lookup"><span data-stu-id="28f05-127">48</span></span>       |
| <span data-ttu-id="28f05-128">imagem 2-por-2 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="28f05-129">12</span><span class="sxs-lookup"><span data-stu-id="28f05-129">12</span></span>       |
| <span data-ttu-id="28f05-130">imagem 1-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="28f05-131">3</span><span class="sxs-lookup"><span data-stu-id="28f05-131">3</span></span>        |



 

<span data-ttu-id="28f05-132">Esta tabela lista a quantidade de espaço ocupado por cada camada para a mesma textura usando a compactação (DXT1).</span><span class="sxs-lookup"><span data-stu-id="28f05-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="28f05-133">Componentes do DDS</span><span class="sxs-lookup"><span data-stu-id="28f05-133">DDS Components</span></span>         | <span data-ttu-id="28f05-134">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="28f05-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="28f05-135">header</span><span class="sxs-lookup"><span data-stu-id="28f05-135">header</span></span>                 | <span data-ttu-id="28f05-136">128</span><span class="sxs-lookup"><span data-stu-id="28f05-136">128</span></span>      |
| <span data-ttu-id="28f05-137">imagem principal de 256 por-64</span><span class="sxs-lookup"><span data-stu-id="28f05-137">256-by-64 main image</span></span>   | <span data-ttu-id="28f05-138">8192</span><span class="sxs-lookup"><span data-stu-id="28f05-138">8192</span></span>     |
| <span data-ttu-id="28f05-139">imagem de 128 por 32 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="28f05-140">2.048</span><span class="sxs-lookup"><span data-stu-id="28f05-140">2048</span></span>     |
| <span data-ttu-id="28f05-141">imagem de 64 por 16 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="28f05-142">512</span><span class="sxs-lookup"><span data-stu-id="28f05-142">512</span></span>      |
| <span data-ttu-id="28f05-143">imagem de 32 por 8 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="28f05-144">128</span><span class="sxs-lookup"><span data-stu-id="28f05-144">128</span></span>      |
| <span data-ttu-id="28f05-145">imagem mipmap de 16 por 4</span><span class="sxs-lookup"><span data-stu-id="28f05-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="28f05-146">32</span><span class="sxs-lookup"><span data-stu-id="28f05-146">32</span></span>       |
| <span data-ttu-id="28f05-147">imagem de 8 por 2 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="28f05-148">16</span><span class="sxs-lookup"><span data-stu-id="28f05-148">16</span></span>       |
| <span data-ttu-id="28f05-149">imagem 4-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="28f05-150">8</span><span class="sxs-lookup"><span data-stu-id="28f05-150">8</span></span>        |
| <span data-ttu-id="28f05-151">imagem 2-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="28f05-152">8</span><span class="sxs-lookup"><span data-stu-id="28f05-152">8</span></span>        |
| <span data-ttu-id="28f05-153">imagem 1-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="28f05-154">8</span><span class="sxs-lookup"><span data-stu-id="28f05-154">8</span></span>        |



 

<span data-ttu-id="28f05-155">Esta tabela lista a quantidade de espaço ocupado por cada camada para a mesma textura usando um formato de compactação DXGI (nesse caso \_ , BC3 UNORM) que, portanto, requer o cabeçalho estendido:</span><span class="sxs-lookup"><span data-stu-id="28f05-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="28f05-156">Componentes do DDS</span><span class="sxs-lookup"><span data-stu-id="28f05-156">DDS Components</span></span>                                                | <span data-ttu-id="28f05-157">\# Bytes</span><span class="sxs-lookup"><span data-stu-id="28f05-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="28f05-158">Header (FourCC definido como "DX10")</span><span class="sxs-lookup"><span data-stu-id="28f05-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="28f05-159">128</span><span class="sxs-lookup"><span data-stu-id="28f05-159">128</span></span>      |
| <span data-ttu-id="28f05-160">cabeçalho estendido (formato DXGI definido como \_ formato dxgi \_ BC3 \_ UNORM)</span><span class="sxs-lookup"><span data-stu-id="28f05-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="28f05-161">20</span><span class="sxs-lookup"><span data-stu-id="28f05-161">20</span></span>       |
| <span data-ttu-id="28f05-162">imagem principal de 256 por-64</span><span class="sxs-lookup"><span data-stu-id="28f05-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="28f05-163">16384</span><span class="sxs-lookup"><span data-stu-id="28f05-163">16384</span></span>    |
| <span data-ttu-id="28f05-164">imagem de 128 por 32 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="28f05-165">4096</span><span class="sxs-lookup"><span data-stu-id="28f05-165">4096</span></span>     |
| <span data-ttu-id="28f05-166">imagem de 64 por 16 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="28f05-167">1024</span><span class="sxs-lookup"><span data-stu-id="28f05-167">1024</span></span>     |
| <span data-ttu-id="28f05-168">imagem de 32 por 8 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="28f05-169">256</span><span class="sxs-lookup"><span data-stu-id="28f05-169">256</span></span>      |
| <span data-ttu-id="28f05-170">imagem mipmap de 16 por 4</span><span class="sxs-lookup"><span data-stu-id="28f05-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="28f05-171">64</span><span class="sxs-lookup"><span data-stu-id="28f05-171">64</span></span>       |
| <span data-ttu-id="28f05-172">imagem de 8 por 2 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="28f05-173">32</span><span class="sxs-lookup"><span data-stu-id="28f05-173">32</span></span>       |
| <span data-ttu-id="28f05-174">imagem 4-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="28f05-175">16</span><span class="sxs-lookup"><span data-stu-id="28f05-175">16</span></span>       |
| <span data-ttu-id="28f05-176">imagem 2-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="28f05-177">16</span><span class="sxs-lookup"><span data-stu-id="28f05-177">16</span></span>       |
| <span data-ttu-id="28f05-178">imagem 1-por-1 mipmap</span><span class="sxs-lookup"><span data-stu-id="28f05-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="28f05-179">16</span><span class="sxs-lookup"><span data-stu-id="28f05-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="28f05-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28f05-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f05-181">Guia de programação para DDS</span><span class="sxs-lookup"><span data-stu-id="28f05-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




