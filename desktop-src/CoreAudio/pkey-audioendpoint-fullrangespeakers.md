---
description: A \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089517"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="fb154-103">PKEY \_ AudioEndpoint \_ FullRangeSpeakers</span><span class="sxs-lookup"><span data-stu-id="fb154-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="fb154-104">A propriedade **PKEY \_ AudioEndpoint \_ FullRangeSpeakers** especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="fb154-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="fb154-105">A máscara indica a configuração física dos alto-falantes do intervalo completo e especifica a atribuição de canais a esses alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="fb154-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="fb154-106">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="fb154-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="fb154-107">O membro **uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é convertida para o tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="fb154-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="fb154-108">Um palestrante de intervalo completo é capaz de reproduzir sons em todo o intervalo de baixo a agudos.</span><span class="sxs-lookup"><span data-stu-id="fb154-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="fb154-109">Normalmente, os alto-falantes maiores são um intervalo completo, mas os altifalantes menores são significativamente menos capazes de reproduzir sons graves.</span><span class="sxs-lookup"><span data-stu-id="fb154-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="fb154-110">No Windows Vista, o mecanismo de áudio usa essa propriedade para gerenciar os níveis de baixo desempenho no fluxo de saída de áudio que é reproduzido pelo dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="fb154-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="fb154-111">A máscara de configuração de canal para essa propriedade está no mesmo formato que a máscara de configuração de canal para a propriedade [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) .</span><span class="sxs-lookup"><span data-stu-id="fb154-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="fb154-112">Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fb154-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="fb154-113">A descrição da propriedade de \_ configuração do canal de áudio KSPROPERTY \_ \_ na documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="fb154-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="fb154-114">A white paper intitulada "suporte de driver de áudio para configurações de alto-falante de Home Theater" no site de [tecnologias de dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="fb154-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="fb154-115">O sistema Obtém a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb154-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="fb154-116">O usuário insere essas informações por meio do painel de controle multimídia do Windows Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="fb154-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="fb154-117">Para obter mais informações sobre Mmsys.cpl, consulte a documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="fb154-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="fb154-118">A máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers de um dispositivo de ponto de extremidade de áudio é um subconjunto da máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ PhysicalSpeakers do mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb154-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="fb154-119">Por exemplo, se um dispositivo de ponto de extremidade de áudio direcionar um conjunto de alto-falantes de 5,1 surround, a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ PHYSICALSPEAKERS será KSAUDIO de \_ alto-falante \_ 5POINT1.</span><span class="sxs-lookup"><span data-stu-id="fb154-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="fb154-120">Essa máscara indica a presença de alto-falantes da esquerda, frontal direita, Front-Center, lateral esquerda e lateral direita — além de um subwoofer.</span><span class="sxs-lookup"><span data-stu-id="fb154-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="fb154-121">Se os alto-falantes front-Left e front-Right forem grandes o suficiente para produzir sons graves, mas o front-Center e os alto-falantes laterais menores não forem, a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FULLRANGESPEAKERS será KSAUDIO \_ \_ , que indica apenas os alto-falantes front-Left e front-Right.</span><span class="sxs-lookup"><span data-stu-id="fb154-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="fb154-122">As máscaras de configuração de canal KSAUDIO \_ \_ 5POINT1 de orador e KSAUDIO \_ \_ estéreo são definidas no arquivo de cabeçalho Ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="fb154-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb154-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb154-123">Requirements</span></span>



| <span data-ttu-id="fb154-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb154-124">Requirement</span></span> | <span data-ttu-id="fb154-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fb154-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb154-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb154-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb154-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb154-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fb154-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb154-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb154-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb154-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fb154-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb154-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb154-131"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb154-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb154-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb154-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb154-133">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="fb154-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="fb154-134">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="fb154-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="fb154-135">**\_Propriedade PKEY AudioEndpoint \_ PhysicalSpeakers**</span><span class="sxs-lookup"><span data-stu-id="fb154-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




