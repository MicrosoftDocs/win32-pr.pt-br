---
description: Especifica o tipo de contêiner de um arquivo codificado.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Atributo MF_TRANSCODE_CONTAINERTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781208"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="31e4a-103">\_Atributo ContainerType de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="31e4a-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="31e4a-104">Especifica o tipo de contêiner de um arquivo codificado.</span><span class="sxs-lookup"><span data-stu-id="31e4a-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="31e4a-105">Os tipos de contêiner têm suporte pelo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="31e4a-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="31e4a-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="31e4a-106">Data type</span></span>

<span data-ttu-id="31e4a-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="31e4a-107">**GUID**</span></span>

<span data-ttu-id="31e4a-108">Os valores possíveis para os tipos de contêiner fornecidos pelo Media Foundation são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="31e4a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="31e4a-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="31e4a-110">Significado</span><span class="sxs-lookup"><span data-stu-id="31e4a-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="31e4a-111"><dt>**MFTranscodeContainerType \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-112">Contêiner de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="31e4a-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="31e4a-113"><dt>**MFTranscodeContainerType \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="31e4a-114">Contêiner de arquivo MP4.</span><span class="sxs-lookup"><span data-stu-id="31e4a-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="31e4a-115"><dt>**MFTranscodeContainerType \_ mp3**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-116">Contêiner de arquivo MP3.</span><span class="sxs-lookup"><span data-stu-id="31e4a-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="31e4a-117"><dt>**MFTranscodeContainerType \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-118">contêiner de arquivos 3GP.</span><span class="sxs-lookup"><span data-stu-id="31e4a-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="31e4a-119"><dt>**MFTranscodeContainerType \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-120">Contêiner de arquivos AC3.</span><span class="sxs-lookup"><span data-stu-id="31e4a-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="31e4a-121"><dt>**MFTranscodeContainerType \_ ADTS**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="31e4a-122">Contêiner de arquivos ADTS.</span><span class="sxs-lookup"><span data-stu-id="31e4a-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="31e4a-123"><dt>**MFTranscodeContainerType \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="31e4a-124">Contêiner de arquivo MPEG2.</span><span class="sxs-lookup"><span data-stu-id="31e4a-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="31e4a-125"><dt>**MFTranscodeContainerType \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="31e4a-126">Contêiner de arquivos FMPEG4.</span><span class="sxs-lookup"><span data-stu-id="31e4a-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="31e4a-127"><dt>**\_Onda MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="31e4a-128">Contêiner de arquivo WAVE.</span><span class="sxs-lookup"><span data-stu-id="31e4a-128">WAVE file container.</span></span><br/> <span data-ttu-id="31e4a-129">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="31e4a-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="31e4a-130"><dt>**\_AVI MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-131">Contêiner de arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="31e4a-131">AVI file container.</span></span><br/> <span data-ttu-id="31e4a-132">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="31e4a-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="31e4a-133"><dt>**MFTranscodeContainerType \_ Amr**</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="31e4a-134">Contêiner de arquivo AMR.</span><span class="sxs-lookup"><span data-stu-id="31e4a-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="31e4a-135">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="31e4a-135">Get/set</span></span>

<span data-ttu-id="31e4a-136">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="31e4a-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="31e4a-137">Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="31e4a-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="31e4a-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="31e4a-138">Remarks</span></span>

<span data-ttu-id="31e4a-139">Esse atributo é usado com o recurso de transcodificação rápida e o objeto gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="31e4a-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="31e4a-140">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="31e4a-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="31e4a-141">Transcodificação rápida</span><span class="sxs-lookup"><span data-stu-id="31e4a-141">Fast Transcode</span></span>

<span data-ttu-id="31e4a-142">O aplicativo deve definir o atributo de contêiner no perfil de transcodificação antes de criar a topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="31e4a-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="31e4a-143">O construtor de topologias analisa esse atributo e carrega o coletor de mídia apropriado no pipeline.</span><span class="sxs-lookup"><span data-stu-id="31e4a-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="31e4a-144">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="31e4a-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="31e4a-145">**IMFTranscodeProfile:: getcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="31e4a-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="31e4a-146">**IMFTranscodeProfile:: setcontainerattributes**</span><span class="sxs-lookup"><span data-stu-id="31e4a-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="31e4a-147">Gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="31e4a-147">Sink Writer</span></span>

<span data-ttu-id="31e4a-148">Esse atributo pode ser usado para configurar o tipo de contêiner de arquivo para o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="31e4a-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="31e4a-149">Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="31e4a-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31e4a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31e4a-150">Requirements</span></span>



| <span data-ttu-id="31e4a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e4a-151">Requirement</span></span> | <span data-ttu-id="31e4a-152">Valor</span><span class="sxs-lookup"><span data-stu-id="31e4a-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31e4a-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e4a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="31e4a-154">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31e4a-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31e4a-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e4a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="31e4a-156">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="31e4a-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="31e4a-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31e4a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e4a-158"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e4a-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e4a-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="31e4a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e4a-160">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31e4a-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31e4a-161">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="31e4a-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




