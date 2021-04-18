---
description: O codificador de voz do Windows Media Audio é otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificador de voz do Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763855"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="9df72-104">Codificador de voz do Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="9df72-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="9df72-105">O codificador de voz do Windows Media Audio é otimizado para codificar a voz humana em altas taxas de compactação.</span><span class="sxs-lookup"><span data-stu-id="9df72-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="9df72-106">Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.</span><span class="sxs-lookup"><span data-stu-id="9df72-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="9df72-107">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="9df72-107">Class Identifier</span></span>

<span data-ttu-id="9df72-108">O CLSID (identificador de classe) do codificador de voz do Windows Media Audio é representado pelo **CLSID \_ CWMSPEncMediaObject2** de constantes.</span><span class="sxs-lookup"><span data-stu-id="9df72-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="9df72-109">Você pode criar uma instância do codificador de voz chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="9df72-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="9df72-110">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="9df72-110">Output Formats</span></span>

<span data-ttu-id="9df72-111">O conteúdo codificado de voz do Windows Media Audio é identificado pela marca de formato 0x00a.</span><span class="sxs-lookup"><span data-stu-id="9df72-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="9df72-112">Propriedades do codificador</span><span class="sxs-lookup"><span data-stu-id="9df72-112">Encoder Properties</span></span>

<span data-ttu-id="9df72-113">O codificador de voz do Windows Media Audio oferece suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9df72-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9df72-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9df72-114">Property</span></span></th>
<th><span data-ttu-id="9df72-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9df72-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9df72-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="9df72-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="9df72-117">Especifica a janela de buffer, em milissegundos, usada para o codec de voz.</span><span class="sxs-lookup"><span data-stu-id="9df72-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="9df72-118">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="9df72-118">Windows XP and later.</span></span><br />
<span data-ttu-id="9df72-119">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="9df72-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9df72-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="9df72-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="9df72-121">Especifica a latência do codificador em unidades de pacote.</span><span class="sxs-lookup"><span data-stu-id="9df72-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="9df72-122">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="9df72-122">Windows XP and later.</span></span><br />
<span data-ttu-id="9df72-123">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="9df72-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9df72-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="9df72-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="9df72-125">Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.</span><span class="sxs-lookup"><span data-stu-id="9df72-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="9df72-126">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="9df72-126">Windows XP and later.</span></span><br />
<span data-ttu-id="9df72-127">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9df72-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9df72-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="9df72-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="9df72-129">Especifica o modo do codec de voz.</span><span class="sxs-lookup"><span data-stu-id="9df72-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="9df72-130">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="9df72-130">Windows XP and later.</span></span><br />
<span data-ttu-id="9df72-131">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9df72-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9df72-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9df72-132">Requirements</span></span>



| <span data-ttu-id="9df72-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df72-133">Requirement</span></span> | <span data-ttu-id="9df72-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9df72-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9df72-135">Cliente</span><span class="sxs-lookup"><span data-stu-id="9df72-135">Client</span></span><br/> | <span data-ttu-id="9df72-136">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="9df72-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="9df72-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9df72-137">Header</span></span><br/> | <dl> <span data-ttu-id="9df72-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df72-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9df72-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9df72-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="9df72-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9df72-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df72-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9df72-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df72-142">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="9df72-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="9df72-143">Usando o codec de voz de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="9df72-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




