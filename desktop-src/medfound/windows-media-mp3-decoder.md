---
description: O decodificador MP3 do Windows Media decodifica os arquivos de áudio que foram codificados nos formatos a seguir.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Decodificador MP3 do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763488"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="a178c-103">Decodificador MP3 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a178c-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="a178c-104">O decodificador MP3 do Windows Media decodifica os arquivos de áudio que foram codificados nos formatos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a178c-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="a178c-105">ISO/IEC 11172-3 (áudio MPEG-1) camada 3</span><span class="sxs-lookup"><span data-stu-id="a178c-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="a178c-106">ISO/IEC 13818-3 (MPEG-2 Audio) camada 3, extensão de frequência de amostragem baixa</span><span class="sxs-lookup"><span data-stu-id="a178c-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a178c-107">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="a178c-107">Class Identifier</span></span>

<span data-ttu-id="a178c-108">O CLSID (identificador de classe) para o decodificador MP3 do Windows Media é representado pela constante **CLSID \_ CMP3DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="a178c-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="a178c-109">Você pode criar uma instância do decodificador MP3 chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a178c-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="a178c-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a178c-110">Interfaces</span></span>

<span data-ttu-id="a178c-111">Um objeto de decodificador MP3 expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="a178c-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a178c-112">Um decodificador MP3 do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a178c-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a178c-113">A tabela a seguir mostra as condições sob as quais um decodificador MP3 do Windows Media se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="a178c-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a178c-114">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a178c-114">Operating system</span></span> | <span data-ttu-id="a178c-115">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="a178c-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a178c-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a178c-116">Windows XP</span></span>       | <span data-ttu-id="a178c-117">Um decodificador MP3 do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a178c-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="a178c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a178c-118">Windows Vista</span></span>    | <span data-ttu-id="a178c-119">Por padrão, um decodificador MP3 do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a178c-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="a178c-120">Se você obtiver uma interface **IMFTransform** ou uma interface **IPropertyStore** em um decodificador mp3 do Windows Media, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="a178c-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="a178c-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a178c-121">Windows 7</span></span>        | <span data-ttu-id="a178c-122">Por padrão, um decodificador MP3 do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a178c-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="a178c-123">Se você obtiver uma interface **IMFTransform** em um decodificador mp3 do Windows Media, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="a178c-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="a178c-124">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="a178c-124">Input Formats</span></span>

<span data-ttu-id="a178c-125">A tabela a seguir mostra a marca de formato de áudio que representa o tipo de entrada suportado pelo decodificador MP3 do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a178c-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="a178c-126">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="a178c-126">Format tag constant</span></span>      | <span data-ttu-id="a178c-127">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="a178c-127">Format tag value</span></span> | <span data-ttu-id="a178c-128">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="a178c-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="a178c-129">\_MPEGLAYER3 de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="a178c-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="a178c-130">0x55</span><span class="sxs-lookup"><span data-stu-id="a178c-130">0x55</span></span>             | <span data-ttu-id="a178c-131">ISO MPEG camada 3</span><span class="sxs-lookup"><span data-stu-id="a178c-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="a178c-132">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="a178c-132">Output Formats</span></span>

<span data-ttu-id="a178c-133">A tabela a seguir mostra as marcas de formato de áudio que representam os tipos de saída com suporte pelo decodificador MP3 do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a178c-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="a178c-134">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="a178c-134">Format tag constant</span></span>       | <span data-ttu-id="a178c-135">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="a178c-135">Format tag value</span></span> | <span data-ttu-id="a178c-136">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="a178c-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a178c-137">\_PCM de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="a178c-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="a178c-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="a178c-138">0x0001</span></span>           | <span data-ttu-id="a178c-139">Formato PCM (quando usado como um DMO ou MFT)</span><span class="sxs-lookup"><span data-stu-id="a178c-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="a178c-140">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="a178c-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="a178c-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="a178c-141">0x0003</span></span>           | <span data-ttu-id="a178c-142">Ponto flutuante IEEE (quando usado como um MFT)</span><span class="sxs-lookup"><span data-stu-id="a178c-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="a178c-143">\_formato Wave \_ extensível</span><span class="sxs-lookup"><span data-stu-id="a178c-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="a178c-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="a178c-144">0xFFFE</span></span>           | <span data-ttu-id="a178c-145">Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE** (quando usado como um MFT)</span><span class="sxs-lookup"><span data-stu-id="a178c-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="a178c-146">O decodificador MP3 do Windows Media dá suporte e enumera os seguintes tipos de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a178c-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="a178c-147">Um tipo de saída que tem a mesma taxa de amostragem e número de canais que o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a178c-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="a178c-148">Saída mono para entrada de estéreo.</span><span class="sxs-lookup"><span data-stu-id="a178c-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="a178c-149">Tipos de saída com profundidades de bits de 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="a178c-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="a178c-150">Saída de ponto flutuante, se o decodificador estiver se comportando como um MFT.</span><span class="sxs-lookup"><span data-stu-id="a178c-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="a178c-151">O decodificador MP3 do Windows Media dá suporte a, mas não enumera, os seguintes tipos de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a178c-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="a178c-152">Um tipo de saída que tem metade da taxa de amostragem do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a178c-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="a178c-153">Um tipo de saída que tem um quarto da taxa de amostragem do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a178c-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a178c-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a178c-154">Requirements</span></span>



| <span data-ttu-id="a178c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a178c-155">Requirement</span></span> | <span data-ttu-id="a178c-156">Valor</span><span class="sxs-lookup"><span data-stu-id="a178c-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a178c-157">Cliente</span><span class="sxs-lookup"><span data-stu-id="a178c-157">Client</span></span><br/> | <span data-ttu-id="a178c-158">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="a178c-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a178c-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a178c-159">Header</span></span><br/> | <dl> <span data-ttu-id="a178c-160"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a178c-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a178c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="a178c-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="a178c-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a178c-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a178c-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="a178c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a178c-164">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="a178c-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a178c-165">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="a178c-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




