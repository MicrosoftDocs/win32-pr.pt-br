---
description: Esta seção contém informações sobre a organização interna de formatos de textura compactada.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formatos de textura compactados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646474"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="bd98f-103">Formatos de textura compactados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd98f-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="bd98f-104">Esta seção contém informações sobre a organização interna de formatos de textura compactada.</span><span class="sxs-lookup"><span data-stu-id="bd98f-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="bd98f-105">Você não precisa desses detalhes para usar texturas compactadas, pois você pode usar as funções D3DX para conversão de e para formatos compactados.</span><span class="sxs-lookup"><span data-stu-id="bd98f-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="bd98f-106">No entanto, essas informações são úteis se você quiser operar diretamente nos dados da superfície compactada.</span><span class="sxs-lookup"><span data-stu-id="bd98f-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="bd98f-107">O Direct3D usa um formato de compactação que divide mapas de textura em blocos de texel de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="bd98f-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="bd98f-108">Se a textura não tiver transparência - é opaca - ou se a transparência for especificada por um alfa de 1 bit, um bloco de 8 bytes representa o bloco de mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="bd98f-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="bd98f-109">Se o mapa da textura contiver texels transparentes, usando um canal alfa, um bloco de 16 bits irá representá-lo.</span><span class="sxs-lookup"><span data-stu-id="bd98f-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="bd98f-110">Texturas opacas e de 1 bit alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd98f-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="bd98f-111">Texturas com canais alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd98f-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="bd98f-112">Qualquer textura deve especificar que os dados sejam armazenados como 64 ou 128 bits por grupo de 16 texels.</span><span class="sxs-lookup"><span data-stu-id="bd98f-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="bd98f-113">Se os blocos de 64 bits-ou seja, o formato DXT1-são usados para a textura, é possível misturar os formatos opaco e de 1 bit alfa em uma base por bloco dentro da mesma textura.</span><span class="sxs-lookup"><span data-stu-id="bd98f-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="bd98f-114">Em outras palavras, a comparação da magnitude de inteiro sem sinal da cor \_ 0 e da cor \_ 1 é executada exclusivamente para cada bloco de 16 texels.</span><span class="sxs-lookup"><span data-stu-id="bd98f-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="bd98f-115">Quando blocos de 128 bits são usados, o canal alfa deve ser especificado em um modo explícito (formato DXT2 ou DXT3) ou interpolado (formato DXT4 ou DXT5) para a textura inteira.</span><span class="sxs-lookup"><span data-stu-id="bd98f-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="bd98f-116">Da mesma forma que ocorre com a cor, quando o modo interpolado é selecionado, o modo de seis ou oito alfas interpolados pode ser usado em uma base de bloco por bloco.</span><span class="sxs-lookup"><span data-stu-id="bd98f-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="bd98f-117">Novamente a comparação de magnitude de alfa \_ 0 e alfa \_ 1 é feita exclusivamente em uma base bloco a bloco.</span><span class="sxs-lookup"><span data-stu-id="bd98f-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="bd98f-118">O Tom dos formatos DXTn é diferente do que foi retornado no DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="bd98f-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="bd98f-119">A densidade agora é medida em bytes (não blocos).</span><span class="sxs-lookup"><span data-stu-id="bd98f-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="bd98f-120">Por exemplo, se você tiver uma largura de 16, terá um timbre de quatro blocos (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="bd98f-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd98f-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd98f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd98f-122">Recursos de textura compactados</span><span class="sxs-lookup"><span data-stu-id="bd98f-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



