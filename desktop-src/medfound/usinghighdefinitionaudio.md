---
description: Usando High-Definition áudio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Usando High-Definition áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661816"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="fc730-103">Usando High-Definition áudio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="fc730-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="fc730-104">Áudio de alta definição, no contexto dos codecs de áudio do Windows Media, é qualquer tipo de áudio com mais de dois canais ou mais de 16 bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="fc730-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="fc730-105">O áudio de alta definição tem suporte nas categorias Professional e Lossless do [codificador de áudio do Windows Media](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="fc730-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="fc730-106">Tipos de áudio de alta definição não compactados são definidos usando a estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fc730-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="fc730-107">**WAVEFORMATEXTENSIBLE** é uma extensão estruturada da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fc730-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="fc730-108">Quando você estiver usando DMOs, o membro **formatType** da estrutura [**do \_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que descreve um tipo de áudio de alta definição deve ser definido como WMCFORMAT \_ WaveFormatEx, assim como é para o áudio normal; não há nenhum identificador de formato especial para **WAVEFORMATEXTENSIBLE**.</span><span class="sxs-lookup"><span data-stu-id="fc730-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="fc730-109">Se um formato usar **WAVEFORMATEXTENSIBLE** , você deverá definir o membro **CbSize** da estrutura **WAVEFORMATEX** como 22.</span><span class="sxs-lookup"><span data-stu-id="fc730-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="fc730-110">Ao usar Media Foundation, você pode construir o tipo de mídia correto de uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) usando a função [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span><span class="sxs-lookup"><span data-stu-id="fc730-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="fc730-111">Os tipos de saída multicanal com suporte do codec Windows Media Audio 10 Professional não usam [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), mas relatam o número correto de canais e bits por amostra na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fc730-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="fc730-112">Assim como acontece com todos os tipos de áudio que descrevem o conteúdo compactado de áudio do Windows Media, há informações adicionais acrescentadas à estrutura **WAVEFORMATEX** que é usada pelo decodificador para descompactação.</span><span class="sxs-lookup"><span data-stu-id="fc730-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="fc730-113">Decodificando High-Definition áudio</span><span class="sxs-lookup"><span data-stu-id="fc730-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="fc730-114">Para decodificar áudio de alta definição, você deve definir a propriedade [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="fc730-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="fc730-115">Se essa propriedade não for definida, o decodificador fornecerá conteúdo estéreo com um máximo de 16 bits por amostra, independentemente do formato compactado.</span><span class="sxs-lookup"><span data-stu-id="fc730-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="fc730-116">O áudio de alta definição tem suporte apenas para Windows XP, Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="fc730-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="fc730-117">Em versões anteriores do Windows, o conteúdo de áudio do Windows Media codificado com alta definição é renderizado como áudio de dois canais com um máximo de 16 bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="fc730-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fc730-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc730-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc730-119">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="fc730-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
