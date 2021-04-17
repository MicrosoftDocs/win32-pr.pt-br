---
description: As \_ constantes de sinalizador de bit LINEBEARERMODE descrevem diferentes modos de portador de uma chamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes de LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779901"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="fb494-103">\_Constantes LINEBEARERMODE</span><span class="sxs-lookup"><span data-stu-id="fb494-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="fb494-104">As constantes de sinalizador de bit **LINEBEARERMODE \_** descrevem diferentes modos de portador de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="fb494-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="fb494-105">Quando um aplicativo faz uma chamada, ele pode solicitar um modo de portador específico.</span><span class="sxs-lookup"><span data-stu-id="fb494-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="fb494-106">Esses modos são usados para selecionar uma determinada qualidade de serviço para a conexão solicitada da rede de telefone subjacente.</span><span class="sxs-lookup"><span data-stu-id="fb494-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="fb494-107">Os modos de portador disponíveis em uma determinada linha são uma funcionalidade de dispositivo da linha.</span><span class="sxs-lookup"><span data-stu-id="fb494-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="fb494-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**</span><span class="sxs-lookup"><span data-stu-id="fb494-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-109">A transferência alternativa de dados de fala ou irrestrito na mesma chamada (ISDN).</span><span class="sxs-lookup"><span data-stu-id="fb494-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**dados do LINEBEARERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="fb494-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-111">A transferência de dados irrestrita na chamada.</span><span class="sxs-lookup"><span data-stu-id="fb494-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="fb494-112">A taxa de dados é especificada separadamente.</span><span class="sxs-lookup"><span data-stu-id="fb494-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**</span><span class="sxs-lookup"><span data-stu-id="fb494-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-114">O modo Multiuse definido pela ISDN.</span><span class="sxs-lookup"><span data-stu-id="fb494-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**</span><span class="sxs-lookup"><span data-stu-id="fb494-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-116">Isso corresponde a uma conexão de sinalização não associada à chamada do aplicativo ao provedor de serviços ou comutador (Tratado como um fluxo de mídia pela TAPI).</span><span class="sxs-lookup"><span data-stu-id="fb494-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**passagem de LINEBEARERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="fb494-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-118">Quando uma chamada está ativa no LINEBEARERMODE \_ PassThrough, o provedor de serviços fornece acesso direto ao hardware anexado para controle pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb494-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="fb494-119">Esse modo é usado principalmente por aplicativos que desejam o controle direto temporário sobre modems assíncronos, acessados por meio das [funções de comunicação](/windows/desktop/DevIO/communications-functions), com a finalidade de configurar ou usar recursos especiais que de outra forma não têm suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="fb494-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**</span><span class="sxs-lookup"><span data-stu-id="fb494-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-121">Serviço de portador para dados digitais em que somente os sete bits de ordem inferior de cada octeto podem conter dados do usuário (por exemplo, para o serviço 56Kbit/s comutado).</span><span class="sxs-lookup"><span data-stu-id="fb494-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ fala**</span><span class="sxs-lookup"><span data-stu-id="fb494-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-123">Isso corresponde à transmissão de fala G. 711 na chamada.</span><span class="sxs-lookup"><span data-stu-id="fb494-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="fb494-124">A rede pode usar técnicas de processamento como transmissão analógica, cancelamento de eco e compactação/descompactação.</span><span class="sxs-lookup"><span data-stu-id="fb494-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="fb494-125">A integridade do bit não é garantida.</span><span class="sxs-lookup"><span data-stu-id="fb494-125">Bit integrity is not assured.</span></span> <span data-ttu-id="fb494-126">A fala não tem o objetivo de oferecer suporte a tipos de mídia de fax e modem.</span><span class="sxs-lookup"><span data-stu-id="fb494-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb494-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**</span><span class="sxs-lookup"><span data-stu-id="fb494-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb494-128">Este é um serviço de portador de taxa de voz analógica de 3,1 kHz regular.</span><span class="sxs-lookup"><span data-stu-id="fb494-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="fb494-129">A integridade do bit não é garantida.</span><span class="sxs-lookup"><span data-stu-id="fb494-129">Bit integrity is not assured.</span></span> <span data-ttu-id="fb494-130">A voz pode dar suporte a tipos de mídia de fax e modem.</span><span class="sxs-lookup"><span data-stu-id="fb494-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb494-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb494-131">Remarks</span></span>

<span data-ttu-id="fb494-132">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb494-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="fb494-133">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="fb494-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="fb494-134">Observe que o modo de portador e o tipo de mídia são noções diferentes.</span><span class="sxs-lookup"><span data-stu-id="fb494-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="fb494-135">O modo de portador de uma chamada é uma indicação da qualidade da conexão telefônica, conforme fornecido principalmente pela rede.</span><span class="sxs-lookup"><span data-stu-id="fb494-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="fb494-136">O tipo de mídia de uma chamada é uma indicação do tipo de fluxo de informações que é trocado nessa chamada.</span><span class="sxs-lookup"><span data-stu-id="fb494-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="fb494-137">O fax do grupo 3 ou o modem de dados são tipos de mídia que usam uma chamada com um modo de portador de voz de 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="fb494-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb494-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb494-138">Requirements</span></span>



| <span data-ttu-id="fb494-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb494-139">Requirement</span></span> | <span data-ttu-id="fb494-140">Valor</span><span class="sxs-lookup"><span data-stu-id="fb494-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fb494-141">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fb494-141">TAPI version</span></span><br/> | <span data-ttu-id="fb494-142">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fb494-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fb494-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb494-143">Header</span></span><br/>       | <dl> <span data-ttu-id="fb494-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb494-144"><dt>Tapi.h</dt></span></span> </dl> |



 

