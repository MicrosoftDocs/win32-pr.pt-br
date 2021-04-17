---
description: As \_ constantes de sinalizador de bit PHONEHOOKSWITCHMODE descrevem os componentes de microfone e de alto-falante de um dispositivo Hookswitch.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Constantes de PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769399"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="77e0a-103">\_Constantes PHONEHOOKSWITCHMODE</span><span class="sxs-lookup"><span data-stu-id="77e0a-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="77e0a-104">As constantes de sinalizador de bit **PHONEHOOKSWITCHMODE \_** descrevem os componentes de microfone e de alto-falante de um dispositivo Hookswitch.</span><span class="sxs-lookup"><span data-stu-id="77e0a-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="77e0a-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**\_MIC PHONEHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="77e0a-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="77e0a-106">O microfone do dispositivo está ativo, o viva-voz está mudo.</span><span class="sxs-lookup"><span data-stu-id="77e0a-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="77e0a-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**</span><span class="sxs-lookup"><span data-stu-id="77e0a-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="77e0a-108">O microfone e o palestrante do dispositivo estão ativos.</span><span class="sxs-lookup"><span data-stu-id="77e0a-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="77e0a-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE \_ ONhook**</span><span class="sxs-lookup"><span data-stu-id="77e0a-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="77e0a-110">O microfone e o alto-falante do dispositivo estão conectados.</span><span class="sxs-lookup"><span data-stu-id="77e0a-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="77e0a-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ palestrante**</span><span class="sxs-lookup"><span data-stu-id="77e0a-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="77e0a-112">O alto-falante do dispositivo está ativo, o microfone está mudo.</span><span class="sxs-lookup"><span data-stu-id="77e0a-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="77e0a-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="77e0a-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="77e0a-114">O modo Hookswitch do dispositivo é desconhecido no momento.</span><span class="sxs-lookup"><span data-stu-id="77e0a-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77e0a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="77e0a-115">Remarks</span></span>

<span data-ttu-id="77e0a-116">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="77e0a-116">No extensibility.</span></span> <span data-ttu-id="77e0a-117">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="77e0a-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="77e0a-118">Essas constantes são usadas para fornecer um nível individual de controle sobre os componentes de microfone e de alto-falante de um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="77e0a-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e0a-119">Requirements</span></span>



| <span data-ttu-id="77e0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e0a-120">Requirement</span></span> | <span data-ttu-id="77e0a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="77e0a-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="77e0a-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="77e0a-122">TAPI version</span></span><br/> | <span data-ttu-id="77e0a-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="77e0a-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="77e0a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77e0a-124">Header</span></span><br/>       | <dl> <span data-ttu-id="77e0a-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e0a-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




