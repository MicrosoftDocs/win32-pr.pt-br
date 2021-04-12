---
description: A \_ Propriedade PKEY AudioEndpoint \_ FormFactor especifica o fator forma do dispositivo de ponto de extremidade de áudio. O fator forma indica os atributos físicos do dispositivo de ponto de extremidade de áudio que o usuário manipula.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457115"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="f280e-104">PKEY \_ AudioEndpoint \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="f280e-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="f280e-105">A propriedade **PKEY \_ AudioEndpoint \_ FormFactor** especifica o fator forma do dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="f280e-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="f280e-106">O fator forma indica os atributos físicos do dispositivo de ponto de extremidade de áudio que o usuário manipula.</span><span class="sxs-lookup"><span data-stu-id="f280e-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="f280e-107">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="f280e-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="f280e-108">O membro **uintVal** da estrutura **PROPVARIANT** contém um valor de enumeração que é convertido para o tipo uint.</span><span class="sxs-lookup"><span data-stu-id="f280e-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="f280e-109">Ele é definido como um dos seguintes valores de enumeração [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :</span><span class="sxs-lookup"><span data-stu-id="f280e-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="f280e-110">RemoteNetworkDevice</span><span class="sxs-lookup"><span data-stu-id="f280e-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="f280e-111">Speakers</span><span class="sxs-lookup"><span data-stu-id="f280e-111">Speakers</span></span>
-   <span data-ttu-id="f280e-112">LineLevel</span><span class="sxs-lookup"><span data-stu-id="f280e-112">LineLevel</span></span>
-   <span data-ttu-id="f280e-113">Fone</span><span class="sxs-lookup"><span data-stu-id="f280e-113">Headphones</span></span>
-   <span data-ttu-id="f280e-114">Microfone</span><span class="sxs-lookup"><span data-stu-id="f280e-114">Microphone</span></span>
-   <span data-ttu-id="f280e-115">Headset</span><span class="sxs-lookup"><span data-stu-id="f280e-115">Headset</span></span>
-   <span data-ttu-id="f280e-116">Aparelho</span><span class="sxs-lookup"><span data-stu-id="f280e-116">Handset</span></span>
-   <span data-ttu-id="f280e-117">UnknownDigitalPassthrough</span><span class="sxs-lookup"><span data-stu-id="f280e-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="f280e-118">SPDIF</span><span class="sxs-lookup"><span data-stu-id="f280e-118">SPDIF</span></span>
-   <span data-ttu-id="f280e-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="f280e-119">HDMI</span></span>
-   <span data-ttu-id="f280e-120">UnknownFormFactor</span><span class="sxs-lookup"><span data-stu-id="f280e-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="f280e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f280e-121">Requirements</span></span>



| <span data-ttu-id="f280e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f280e-122">Requirement</span></span> | <span data-ttu-id="f280e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f280e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f280e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f280e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f280e-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f280e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f280e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f280e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f280e-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f280e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f280e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f280e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f280e-129"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f280e-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f280e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f280e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f280e-131">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="f280e-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="f280e-132">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="f280e-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




