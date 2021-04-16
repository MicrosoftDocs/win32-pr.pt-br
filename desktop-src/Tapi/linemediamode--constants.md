---
description: As \_ constantes LINEMEDIAMODE descrevem os tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes de LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758401"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="76e91-103">\_Constantes LINEMEDIAMODE</span><span class="sxs-lookup"><span data-stu-id="76e91-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="76e91-104">As **constantes \_ LINEMEDIAMODE** descrevem os tipos de mídia (ou modos) de uma sessão ou chamada de comunicação.</span><span class="sxs-lookup"><span data-stu-id="76e91-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="76e91-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**</span><span class="sxs-lookup"><span data-stu-id="76e91-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-106">A energia de voz foi detectada na chamada, e a voz é manipulada localmente por um aplicativo automatizado, como com um aplicativo de secretária automática.</span><span class="sxs-lookup"><span data-stu-id="76e91-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="76e91-107">Quando um provedor de serviços não pode distinguir entre voz interativa e automatizada em uma chamada de entrada, ele relatará a chamada como voz interativa.</span><span class="sxs-lookup"><span data-stu-id="76e91-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAmode**</span><span class="sxs-lookup"><span data-stu-id="76e91-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-109">Uma sessão de modem de dados na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-109">A data modem session on the call.</span></span> <span data-ttu-id="76e91-110">Os protocolos de modem atuais exigem que a estação chamada inicie o handshake.</span><span class="sxs-lookup"><span data-stu-id="76e91-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="76e91-111">Para uma chamada de modem de dados de entrada, o aplicativo normalmente pode não fazer nenhuma detecção positiva.</span><span class="sxs-lookup"><span data-stu-id="76e91-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="76e91-112">Como o provedor de serviços faz essa determinação é sua escolha.</span><span class="sxs-lookup"><span data-stu-id="76e91-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="76e91-113">Por exemplo, um período de silêncio logo após responder a uma chamada de entrada pode ser usado como uma heurística para decidir que isso pode ser uma chamada de modem de dados.</span><span class="sxs-lookup"><span data-stu-id="76e91-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="76e91-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-115">Uma sessão ADSI (interface de serviços de vídeo analógico) na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="76e91-116">A ADSI aprimora chamadas de voz com informações alfanuméricas baixadas para o telefone e o uso de botões suaves no telefone.</span><span class="sxs-lookup"><span data-stu-id="76e91-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**</span><span class="sxs-lookup"><span data-stu-id="76e91-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-118">Um fluxo de dados digital de formato não especificado.</span><span class="sxs-lookup"><span data-stu-id="76e91-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="76e91-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-120">Um fax do grupo 3 está sendo enviado ou recebido pela chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="76e91-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-122">Um fax do grupo 4 está sendo enviado ou recebido pela chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**</span><span class="sxs-lookup"><span data-stu-id="76e91-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-124">A energia de voz foi detectada na chamada, e a chamada é tratada como uma chamada de voz interativa com seres humanos em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="76e91-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ misto**</span><span class="sxs-lookup"><span data-stu-id="76e91-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-126">Uma sessão mista na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-126">A mixed session on the call.</span></span> <span data-ttu-id="76e91-127">Misto é um dos serviços ISDN telemática.</span><span class="sxs-lookup"><span data-stu-id="76e91-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**\_TDD LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="76e91-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-129">Uma sessão TDD (dispositivos de telefonia para a surdo) na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ Teletex**</span><span class="sxs-lookup"><span data-stu-id="76e91-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-131">Uma sessão Teletex na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-131">A teletex session on the call.</span></span> <span data-ttu-id="76e91-132">Teletex é um dos serviços telemáticas.</span><span class="sxs-lookup"><span data-stu-id="76e91-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**TELEX do LINEMEDIAMODE \_**</span><span class="sxs-lookup"><span data-stu-id="76e91-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-134">Uma sessão de telex na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-134">A telex session on the call.</span></span> <span data-ttu-id="76e91-135">O telex é um dos serviços telemáticas.</span><span class="sxs-lookup"><span data-stu-id="76e91-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**vídeo do LINEMEDIAMODE \_**</span><span class="sxs-lookup"><span data-stu-id="76e91-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-137">O tipo de mídia da chamada é vídeo.</span><span class="sxs-lookup"><span data-stu-id="76e91-137">The media type of the call is video.</span></span> <span data-ttu-id="76e91-138">(TAPI versões 2,1 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="76e91-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**</span><span class="sxs-lookup"><span data-stu-id="76e91-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-140">Uma sessão videotex na chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-140">A videotex session on the call.</span></span> <span data-ttu-id="76e91-141">Videotex é um dos serviços telemáticas.</span><span class="sxs-lookup"><span data-stu-id="76e91-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**</span><span class="sxs-lookup"><span data-stu-id="76e91-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-143">O tipo de mídia da chamada é VoiceView.</span><span class="sxs-lookup"><span data-stu-id="76e91-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="76e91-144">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="76e91-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76e91-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="76e91-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76e91-146">Um fluxo de mídia existe, mas seu modo não é conhecido no momento e pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="76e91-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="76e91-147">Isso corresponderia a uma chamada com um tipo de mídia não classificado.</span><span class="sxs-lookup"><span data-stu-id="76e91-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="76e91-148">Em ambientes de telefonia analógicos típicos, o tipo de mídia de uma chamada de entrada pode ser desconhecido até que a chamada tenha sido respondida e o fluxo de mídia tenha sido filtrado para fazer uma determinação.</span><span class="sxs-lookup"><span data-stu-id="76e91-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="76e91-149">Se o sinalizador de modo de mídia desconhecido for definido, outros sinalizadores de mídia também poderão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="76e91-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="76e91-150">Isso é usado para significar que a mídia é desconhecida, mas é provável que seja um dos outros tipos de mídia selecionados.</span><span class="sxs-lookup"><span data-stu-id="76e91-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76e91-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="76e91-151">Remarks</span></span>

<span data-ttu-id="76e91-152">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="76e91-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="76e91-153">Observe que o modo de portador e o tipo de mídia são noções diferentes.</span><span class="sxs-lookup"><span data-stu-id="76e91-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="76e91-154">O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede.</span><span class="sxs-lookup"><span data-stu-id="76e91-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="76e91-155">O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado nessa chamada.</span><span class="sxs-lookup"><span data-stu-id="76e91-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="76e91-156">O fax do grupo 3 ou o modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="76e91-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="76e91-157">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esse valor de LINEMEDIAMODE \_ se não houver suporte na versão negociada.</span><span class="sxs-lookup"><span data-stu-id="76e91-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e91-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76e91-158">Requirements</span></span>



| <span data-ttu-id="76e91-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="76e91-159">Requirement</span></span> | <span data-ttu-id="76e91-160">Valor</span><span class="sxs-lookup"><span data-stu-id="76e91-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76e91-161">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="76e91-161">TAPI version</span></span><br/> | <span data-ttu-id="76e91-162">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="76e91-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="76e91-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76e91-163">Header</span></span><br/>       | <dl> <span data-ttu-id="76e91-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="76e91-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




