---
description: As GUIDs a seguir definem extensões de carga para fluxos ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUIDs de extensão de carga ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501203"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="d6f9d-103">GUIDs de extensão de carga ASF</span><span class="sxs-lookup"><span data-stu-id="d6f9d-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="d6f9d-104">As GUIDs a seguir definem extensões de carga para fluxos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d6f9d-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="d6f9d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d6f9d-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="d6f9d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f9d-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="d6f9d-107"><dt>**MFASFSampleExtension \_ SampleDuration**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="d6f9d-108">Os dados indicam a duração, em milissegundos, do exemplo contido no objeto de buffer.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="d6f9d-109"><dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="d6f9d-110">Os dados indicam se o exemplo é um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="d6f9d-111">Um valor de zero indica que o exemplo não é um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="d6f9d-112">Um valor diferente de zero indica que se trata de um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="d6f9d-113"><dt>**MFASFSampleExtension \_ SMPTE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="d6f9d-114">Os dados são um código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="d6f9d-115"><dt>**\_Nome de arquivo MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="d6f9d-116">Os dados na extensão de exemplo especificam o nome do arquivo do qual o conteúdo no exemplo foi tirado.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="d6f9d-117"><dt>**\_ContentType MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="d6f9d-118">Os dados identificam o tipo de conteúdo que o exemplo contém.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="d6f9d-119"><dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="d6f9d-120">Os dados indicam a taxa de proporção de pixel do conteúdo no exemplo.</span><span class="sxs-lookup"><span data-stu-id="d6f9d-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="d6f9d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f9d-121">Requirements</span></span>



| <span data-ttu-id="d6f9d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f9d-122">Requirement</span></span> | <span data-ttu-id="d6f9d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f9d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f9d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f9d-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6f9d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d6f9d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f9d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6f9d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6f9d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6f9d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f9d-129"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9d-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f9d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6f9d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f9d-131">**IMFASFStreamConfig::AddPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="d6f9d-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="d6f9d-132">**IMFASFStreamConfig::GetPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="d6f9d-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="d6f9d-133">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="d6f9d-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




