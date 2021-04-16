---
description: As \_ constantes de sinalizador de bit PHONEHOOKSWITCHDEV descrevem vários dispositivos de e/s de áudio cada um com seu próprio Hookswitch controlável do computador.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Constantes de PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754184"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="2e95e-103">\_Constantes PHONEHOOKSWITCHDEV</span><span class="sxs-lookup"><span data-stu-id="2e95e-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="2e95e-104">As constantes de sinalizador de bit **PHONEHOOKSWITCHDEV \_** descrevem vários dispositivos de e/s de áudio cada um com seu próprio Hookswitch controlável do computador.</span><span class="sxs-lookup"><span data-stu-id="2e95e-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="2e95e-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**fone de PHONEHOOKSWITCHDEV \_**</span><span class="sxs-lookup"><span data-stu-id="2e95e-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e95e-106">Esse é um telefone Ear e mouthpiece padrão.</span><span class="sxs-lookup"><span data-stu-id="2e95e-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e95e-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**Headset de PHONEHOOKSWITCHDEV \_**</span><span class="sxs-lookup"><span data-stu-id="2e95e-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e95e-108">Este é um headset conectado ao conjunto de telefone.</span><span class="sxs-lookup"><span data-stu-id="2e95e-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e95e-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ palestrante**</span><span class="sxs-lookup"><span data-stu-id="2e95e-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e95e-110">Este é um loudspeaker e um microfone internos.</span><span class="sxs-lookup"><span data-stu-id="2e95e-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="2e95e-111">Isso também pode ser um palestrante de suplemento conectado externamente ao conjunto de telefone.</span><span class="sxs-lookup"><span data-stu-id="2e95e-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e95e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e95e-112">Remarks</span></span>

<span data-ttu-id="2e95e-113">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="2e95e-113">No extensibility.</span></span> <span data-ttu-id="2e95e-114">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="2e95e-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="2e95e-115">Essas constantes são usadas na estrutura de dados [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para indicar os recursos do Dispositivo Hookswitch de um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="2e95e-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="2e95e-116">A estrutura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) relata o estado dos dispositivos Hookswitch do telefone.</span><span class="sxs-lookup"><span data-stu-id="2e95e-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="2e95e-117">A função [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) e [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) o usam como um parâmetro para selecionar o dispositivo de e/s do telefone.</span><span class="sxs-lookup"><span data-stu-id="2e95e-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e95e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e95e-118">Requirements</span></span>



| <span data-ttu-id="2e95e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e95e-119">Requirement</span></span> | <span data-ttu-id="2e95e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2e95e-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2e95e-121">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="2e95e-121">TAPI version</span></span><br/> | <span data-ttu-id="2e95e-122">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2e95e-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2e95e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e95e-123">Header</span></span><br/>       | <dl> <span data-ttu-id="2e95e-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e95e-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




