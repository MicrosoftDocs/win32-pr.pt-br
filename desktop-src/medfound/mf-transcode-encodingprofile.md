---
description: Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Atributo MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502107"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="8b154-103">\_Atributo ENCODINGPROFILE de rescodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="8b154-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="8b154-104">Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="8b154-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b154-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8b154-105">Data type</span></span>

<span data-ttu-id="8b154-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8b154-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="8b154-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="8b154-107">Get/set</span></span>

<span data-ttu-id="8b154-108">Para obter esse atributo, chame [**IMFAttributes:: Getallocatestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="8b154-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="8b154-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="8b154-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b154-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b154-110">Remarks</span></span>

<span data-ttu-id="8b154-111">Use esse atributo ao transcodificar para um dispositivo que dá suporte à mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b154-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="8b154-112">Se esse atributo for definido, o codificador usará o perfil de conformidade do dispositivo, ou modelo, para os codecs de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b154-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="8b154-113">Defina o atributo no perfil transcodificar antes de criar a topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="8b154-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="8b154-114">O valor desse atributo pode ser qualquer uma das cadeias de caracteres do modelo de conformidade listadas nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8b154-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="8b154-115">Modelos de conformidade do dispositivo de áudio</span><span class="sxs-lookup"><span data-stu-id="8b154-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="8b154-116">Modelos de conformidade de dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="8b154-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="8b154-117">Para a codificação de vídeo do Windows Media, o construtor de topologias usa esse atributo para definir a propriedade [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) no codificador.</span><span class="sxs-lookup"><span data-stu-id="8b154-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="8b154-118">O codificador tentará usar o modelo especificado para codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8b154-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="8b154-119">Para obter o modelo real, percorra os nós da topologia de transcodificação para obter um ponteiro para o nó do codificador.</span><span class="sxs-lookup"><span data-stu-id="8b154-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="8b154-120">Em seguida, obtenha o valor da propriedade [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) do codificador.</span><span class="sxs-lookup"><span data-stu-id="8b154-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="8b154-121">O construtor de topologias também usa o valor desse atributo para definir a propriedade "DeviceConformanceTemplate" no coletor de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="8b154-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="8b154-122">Se esse atributo for definido, o objeto de metadados do arquivo ASF será sempre gerado, independentemente do valor especificado pelo aplicativo do atributo [de \_ \_ transferência de \_ metadados \_ MF de ignorar](mf-transcode-skip-metadata-transfer.md) .</span><span class="sxs-lookup"><span data-stu-id="8b154-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="8b154-123">Os valores típicos para esse atributo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b154-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="8b154-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8b154-124">Value</span></span>   | <span data-ttu-id="8b154-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b154-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="8b154-126">PONTOS</span><span class="sxs-lookup"><span data-stu-id="8b154-126">"AP"</span></span>    | <span data-ttu-id="8b154-127">Vídeo de perfil avançado</span><span class="sxs-lookup"><span data-stu-id="8b154-127">Advanced profile video</span></span>           |
| <span data-ttu-id="8b154-128">MP</span><span class="sxs-lookup"><span data-stu-id="8b154-128">"MP"</span></span>    | <span data-ttu-id="8b154-129">Vídeo do perfil principal</span><span class="sxs-lookup"><span data-stu-id="8b154-129">Main profile video</span></span>               |
| <span data-ttu-id="8b154-130">SP3</span><span class="sxs-lookup"><span data-stu-id="8b154-130">"SP"</span></span>    | <span data-ttu-id="8b154-131">Vídeo de perfil simples</span><span class="sxs-lookup"><span data-stu-id="8b154-131">Simple profile video</span></span>             |
| <span data-ttu-id="8b154-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="8b154-132">"MP@LL"</span></span> | <span data-ttu-id="8b154-133">Perfil principal, vídeo de nível médio</span><span class="sxs-lookup"><span data-stu-id="8b154-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="8b154-134">Cache</span><span class="sxs-lookup"><span data-stu-id="8b154-134">"L2"</span></span>    | <span data-ttu-id="8b154-135">Perfil de áudio, <= 160 kbps</span><span class="sxs-lookup"><span data-stu-id="8b154-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="8b154-136">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8b154-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b154-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b154-137">Requirements</span></span>



| <span data-ttu-id="8b154-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b154-138">Requirement</span></span> | <span data-ttu-id="8b154-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8b154-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b154-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b154-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8b154-141">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8b154-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b154-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b154-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8b154-143">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8b154-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8b154-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b154-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b154-145"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b154-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b154-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b154-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b154-147">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b154-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b154-148">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="8b154-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="8b154-149">**IMFTranscodeProfile:: getaudioattributes**</span><span class="sxs-lookup"><span data-stu-id="8b154-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="8b154-150">**IMFTranscodeProfile:: setaudioattributes**</span><span class="sxs-lookup"><span data-stu-id="8b154-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="8b154-151">**IMFTranscodeProfile:: setvideoattributes**</span><span class="sxs-lookup"><span data-stu-id="8b154-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="8b154-152">**IMFTranscodeProfile:: getvideoattributes**</span><span class="sxs-lookup"><span data-stu-id="8b154-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
