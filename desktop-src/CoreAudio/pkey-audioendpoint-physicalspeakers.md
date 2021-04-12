---
description: 'Saiba mais sobre: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501057"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="d40ad-103">PKEY \_ AudioEndpoint \_ PhysicalSpeakers</span><span class="sxs-lookup"><span data-stu-id="d40ad-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="d40ad-104">A propriedade **PKEY \_ AudioEndpoint \_ PhysicalSpeakers** especifica a máscara de configuração de canal para o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="d40ad-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="d40ad-105">A máscara indica a configuração física de um conjunto de alto-falantes e especifica a atribuição de canais aos alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="d40ad-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="d40ad-106">Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d40ad-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="d40ad-107">A descrição da propriedade de \_ configuração do canal de áudio KSPROPERTY \_ \_ na documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="d40ad-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="d40ad-108">A white paper intitulada "suporte de driver de áudio para configurações de alto-falante de Home Theater" no site de [tecnologias de dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="d40ad-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="d40ad-109">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="d40ad-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="d40ad-110">O membro **uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é convertida para o tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="d40ad-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d40ad-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d40ad-111">Requirements</span></span>



| <span data-ttu-id="d40ad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d40ad-112">Requirement</span></span> | <span data-ttu-id="d40ad-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d40ad-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d40ad-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d40ad-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d40ad-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d40ad-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d40ad-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d40ad-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d40ad-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d40ad-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d40ad-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d40ad-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d40ad-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d40ad-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d40ad-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d40ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d40ad-121">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="d40ad-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="d40ad-122">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="d40ad-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




