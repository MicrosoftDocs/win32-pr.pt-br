---
description: As constantes do tipo de mídia são definidas abaixo.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Constantes de TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782897"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="52fac-103">\_Constantes TAPIMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="52fac-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="52fac-104">Os seguintes tipos de mídia estão definidos:</span><span class="sxs-lookup"><span data-stu-id="52fac-104">The following media types are defined:</span></span>



| <span data-ttu-id="52fac-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="52fac-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="52fac-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="52fac-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="52fac-107"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0X8</dt> de áudio</span><span class="sxs-lookup"><span data-stu-id="52fac-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="52fac-108">Um fluxo de mídia de áudio que está entrando ou saindo do computador.</span><span class="sxs-lookup"><span data-stu-id="52fac-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="52fac-109">Um fluxo de mídia inserido normalmente seria reproduzido em alto-falantes ou enviado a um dispositivo de monofone, e um fluxo de saída normalmente seria capturado por meio de um microfone ou dispositivo de monofone.</span><span class="sxs-lookup"><span data-stu-id="52fac-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="52fac-110"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0X8000</dt> de vídeo</span><span class="sxs-lookup"><span data-stu-id="52fac-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="52fac-111">Um fluxo de mídia de vídeo que está entrando ou saindo do computador.</span><span class="sxs-lookup"><span data-stu-id="52fac-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="52fac-112">Um fluxo de mídia inserido normalmente seria renderizado em uma janela de vídeo e um fluxo de mídia de saída normalmente seria capturado com uma câmera de vídeo.</span><span class="sxs-lookup"><span data-stu-id="52fac-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="52fac-113"><dt>**TAPIMEDIATYPE \_ Datamodens**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="52fac-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="52fac-114">Um fluxo de mídia de dados associado a um modem de dados.</span><span class="sxs-lookup"><span data-stu-id="52fac-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="52fac-115"><dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="52fac-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="52fac-116">Um fluxo de mídia de dados que está associado a um fax de protocolo G3.</span><span class="sxs-lookup"><span data-stu-id="52fac-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="52fac-117"><dt>**TAPIMEDIATYPE \_ MULTITRACK**</dt> <dt>0x10000</dt></span><span class="sxs-lookup"><span data-stu-id="52fac-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="52fac-118">Um fluxo está em um terminal multitrack.</span><span class="sxs-lookup"><span data-stu-id="52fac-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="52fac-119"><dt>**\_ \_ Fluxo único de MediaType RTP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52fac-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="52fac-120">Esse GUID é usado entre um terminal fornecido pelo aplicativo e o fluxo do MSP.</span><span class="sxs-lookup"><span data-stu-id="52fac-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="52fac-121">Se o PIN do terminal der suporte a esse tipo de mídia, o fluxo irá trocar dados brutos do RTP pelo terminal.</span><span class="sxs-lookup"><span data-stu-id="52fac-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="52fac-122">Esse modo é suportado apenas pelos fluxos de vídeo no H323 MSP e no IPConf MSP para Windows 2000 SP1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="52fac-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="52fac-123">**Cabeçalho:** Declarado em ipmsp. h.</span><span class="sxs-lookup"><span data-stu-id="52fac-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="52fac-124">O cabeçalho ipmsp. h não está disponível no no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52fac-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="52fac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52fac-125">Requirements</span></span>



| <span data-ttu-id="52fac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="52fac-126">Requirement</span></span> | <span data-ttu-id="52fac-127">Valor</span><span class="sxs-lookup"><span data-stu-id="52fac-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52fac-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="52fac-128">TAPI version</span></span><br/> | <span data-ttu-id="52fac-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="52fac-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="52fac-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52fac-130">Header</span></span><br/>       | <dl> <span data-ttu-id="52fac-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fac-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52fac-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="52fac-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fac-133">**ITQOSEvent:: obter \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="52fac-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="52fac-134">**ITAMMediaFormat:: obter \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="52fac-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="52fac-135">**ITAMMediaFormat::p UT \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="52fac-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="52fac-136">**ITCallInfo:: obter \_ CallInfoLong**</span><span class="sxs-lookup"><span data-stu-id="52fac-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="52fac-137">**ITMediaSupport:: obter \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="52fac-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="52fac-138">**ITTerminalSupport:: createterminal**</span><span class="sxs-lookup"><span data-stu-id="52fac-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

