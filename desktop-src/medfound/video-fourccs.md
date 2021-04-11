---
description: FOURCC de vídeo
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: FOURCC de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296619"
---
# <a name="video-fourccs"></a><span data-ttu-id="f11cc-103">FOURCC de vídeo</span><span class="sxs-lookup"><span data-stu-id="f11cc-103">Video FOURCCs</span></span>

<span data-ttu-id="f11cc-104">Muitos formatos de vídeo têm códigos FOURCC atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="f11cc-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="f11cc-105">Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="f11cc-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="f11cc-106">Por exemplo, o código FOURCC para vídeo YUY2 é ' YUY2 '.</span><span class="sxs-lookup"><span data-stu-id="f11cc-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="f11cc-107">Várias macros C/C++ são definidas para declarar valores FOURCC no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f11cc-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="f11cc-108">A macro **MAKEFOURCC** é definida no mmsystem. h e a macro da **FCC** é definida em Aviriff. h e em vários outros arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="f11cc-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="f11cc-109">Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="f11cc-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="f11cc-110">Portanto, as instruções a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="f11cc-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="f11cc-111">(No último exemplo, reverter a ordem de bytes é necessário porque o Windows usa uma arquitetura little-endian.</span><span class="sxs-lookup"><span data-stu-id="f11cc-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="f11cc-112">' Y ' = 0x59, ' U ' = 0x55 e ' 2 ' = 0x32, portanto, ' 2YUY ' é 0x32595559.)</span><span class="sxs-lookup"><span data-stu-id="f11cc-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="f11cc-113">Algumas das APIs de [aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md) usam um valor **D3DFORMAT** para descrever um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f11cc-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="f11cc-114">Um código FOURCC também pode ser usado neste contexto:</span><span class="sxs-lookup"><span data-stu-id="f11cc-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="f11cc-115">Constantes FOURCC</span><span class="sxs-lookup"><span data-stu-id="f11cc-115">FOURCC Constants</span></span>

<span data-ttu-id="f11cc-116">A tabela a seguir lista alguns códigos FOURCC comuns.</span><span class="sxs-lookup"><span data-stu-id="f11cc-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="f11cc-117">Valor FOURCC</span><span class="sxs-lookup"><span data-stu-id="f11cc-117">FOURCC value</span></span> | <span data-ttu-id="f11cc-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f11cc-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f11cc-119">Taxas</span><span class="sxs-lookup"><span data-stu-id="f11cc-119">'H264'</span></span>       | <span data-ttu-id="f11cc-120">Vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="f11cc-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="f11cc-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="f11cc-121">'I420'</span></span>       | <span data-ttu-id="f11cc-122">Vídeo YUV armazenado no formato planar 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="f11cc-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="f11cc-123">'IYUV'</span><span class="sxs-lookup"><span data-stu-id="f11cc-123">'IYUV'</span></span>       | <span data-ttu-id="f11cc-124">Vídeo YUV armazenado no formato planar 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="f11cc-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="f11cc-125">' 4S2 '</span><span class="sxs-lookup"><span data-stu-id="f11cc-125">'M4S2'</span></span>       | <span data-ttu-id="f11cc-126">Vídeo MPEG-4 parte 2.</span><span class="sxs-lookup"><span data-stu-id="f11cc-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="f11cc-127">MP4S</span><span class="sxs-lookup"><span data-stu-id="f11cc-127">'MP4S'</span></span>       | <span data-ttu-id="f11cc-128">Microsoft MPEG 4 codec versão 3.</span><span class="sxs-lookup"><span data-stu-id="f11cc-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="f11cc-129">Não há mais suporte para esse codec.</span><span class="sxs-lookup"><span data-stu-id="f11cc-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="f11cc-130">'MP4V'</span><span class="sxs-lookup"><span data-stu-id="f11cc-130">'MP4V'</span></span>       | <span data-ttu-id="f11cc-131">Vídeo MPEG-4 parte 2.</span><span class="sxs-lookup"><span data-stu-id="f11cc-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="f11cc-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="f11cc-132">'MPG1'</span></span>       | <span data-ttu-id="f11cc-133">Vídeo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f11cc-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="f11cc-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="f11cc-134">'MSS1'</span></span>       | <span data-ttu-id="f11cc-135">Conteúdo codificado com o codec de tela do Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="f11cc-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="f11cc-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="f11cc-136">'MSS2'</span></span>       | <span data-ttu-id="f11cc-137">Conteúdo codificado com o codec de tela do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="f11cc-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="f11cc-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="f11cc-138">'UYVY'</span></span>       | <span data-ttu-id="f11cc-139">Vídeo YUV armazenado no formato 4:2:2 embalado.</span><span class="sxs-lookup"><span data-stu-id="f11cc-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="f11cc-140">Semelhante a YUY2, mas com ordem de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="f11cc-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="f11cc-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="f11cc-141">'WMV1'</span></span>       | <span data-ttu-id="f11cc-142">Conteúdo codificado com o codec do Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="f11cc-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="f11cc-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="f11cc-143">'WMV2'</span></span>       | <span data-ttu-id="f11cc-144">Conteúdo codificado com o codec do Windows Media Video 8.</span><span class="sxs-lookup"><span data-stu-id="f11cc-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="f11cc-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="f11cc-145">'WMV3'</span></span>       | <span data-ttu-id="f11cc-146">Conteúdo codificado com o codec do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="f11cc-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="f11cc-147">'WMVA'</span><span class="sxs-lookup"><span data-stu-id="f11cc-147">'WMVA'</span></span>       | <span data-ttu-id="f11cc-148">Conteúdo codificado com a versão mais antiga e obsoleta do codec de perfil avançado do vídeo do Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="f11cc-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="f11cc-149">'WMVP'</span><span class="sxs-lookup"><span data-stu-id="f11cc-149">'WMVP'</span></span>       | <span data-ttu-id="f11cc-150">Conteúdo codificado com o codec de imagem do Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="f11cc-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="f11cc-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="f11cc-151">'WVC1'</span></span>       | <span data-ttu-id="f11cc-152">SMPTE 421M ("VC-1").</span><span class="sxs-lookup"><span data-stu-id="f11cc-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="f11cc-153">Conteúdo codificado com o perfil avançado do vídeo do Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="f11cc-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="f11cc-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="f11cc-154">'WVP2'</span></span>       | <span data-ttu-id="f11cc-155">Conteúdo codificado com o codec Windows Media Video 9,1 Image v2.</span><span class="sxs-lookup"><span data-stu-id="f11cc-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="f11cc-156">YUY2</span><span class="sxs-lookup"><span data-stu-id="f11cc-156">'YUY2'</span></span>       | <span data-ttu-id="f11cc-157">Vídeo YUV armazenado no formato 4:2:2 embalado.</span><span class="sxs-lookup"><span data-stu-id="f11cc-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="f11cc-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="f11cc-158">'YV12'</span></span>       | <span data-ttu-id="f11cc-159">Vídeo YUV armazenado no formato planar 4:2:0 ou 4:1:1.</span><span class="sxs-lookup"><span data-stu-id="f11cc-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="f11cc-160">Idêntico a I420/IYUV, exceto que os planos de você e V são alternados.</span><span class="sxs-lookup"><span data-stu-id="f11cc-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="f11cc-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="f11cc-161">'YVU9'</span></span>       | <span data-ttu-id="f11cc-162">Vídeo YUV armazenado no formato planar 16:1:1.</span><span class="sxs-lookup"><span data-stu-id="f11cc-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="f11cc-163">YVYU</span><span class="sxs-lookup"><span data-stu-id="f11cc-163">'YVYU'</span></span>       | <span data-ttu-id="f11cc-164">Vídeo YUV armazenado no formato 4:2:2 embalado.</span><span class="sxs-lookup"><span data-stu-id="f11cc-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="f11cc-165">Semelhante a YUY2, mas com ordem de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="f11cc-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="f11cc-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f11cc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11cc-167">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="f11cc-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="f11cc-168">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="f11cc-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



