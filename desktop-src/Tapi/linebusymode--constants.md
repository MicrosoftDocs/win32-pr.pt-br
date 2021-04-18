---
description: As \_ constantes de sinalizador de bit LINEBUSYMODE descrevem sinais ocupados diferentes que o comutador ou a rede pode gerar. Esses sinais ocupados normalmente indicam que um recurso diferente necessário para fazer uma chamada está em uso no momento.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes de LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810129"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="5f664-104">\_Constantes LINEBUSYMODE</span><span class="sxs-lookup"><span data-stu-id="5f664-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="5f664-105">As constantes de sinalizador de bit **LINEBUSYMODE \_** descrevem sinais ocupados diferentes que o comutador ou a rede pode gerar.</span><span class="sxs-lookup"><span data-stu-id="5f664-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="5f664-106">Esses sinais ocupados normalmente indicam que um recurso diferente necessário para fazer uma chamada está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="5f664-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="5f664-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_estação LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="5f664-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f664-108">O sinal de ocupado indica que a estação da parte chamada está ocupada.</span><span class="sxs-lookup"><span data-stu-id="5f664-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="5f664-109">Isso geralmente é sinalizado com um tom ocupado *normal* .</span><span class="sxs-lookup"><span data-stu-id="5f664-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f664-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_tronco LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="5f664-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f664-111">O sinal Busy indica que um tronco ou circuito está ocupado.</span><span class="sxs-lookup"><span data-stu-id="5f664-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="5f664-112">Em geral, isso é sinalizado com um tom de ocupado *rápido* .</span><span class="sxs-lookup"><span data-stu-id="5f664-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f664-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="5f664-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f664-114">O modo específico do sinal Busy é desconhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="5f664-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f664-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="5f664-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f664-116">O modo específico do sinal de ocupado não está disponível e não se tornará conhecido.</span><span class="sxs-lookup"><span data-stu-id="5f664-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f664-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f664-117">Remarks</span></span>

<span data-ttu-id="5f664-118">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f664-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="5f664-119">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="5f664-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="5f664-120">Sinais ocupados podem ser enviados como tons de inband ou mensagens fora de banda.</span><span class="sxs-lookup"><span data-stu-id="5f664-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="5f664-121">A TAPI não faz suposições sobre o mecanismo de sinalização específico.</span><span class="sxs-lookup"><span data-stu-id="5f664-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f664-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f664-122">Requirements</span></span>



| <span data-ttu-id="5f664-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f664-123">Requirement</span></span> | <span data-ttu-id="5f664-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5f664-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5f664-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5f664-125">TAPI version</span></span><br/> | <span data-ttu-id="5f664-126">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5f664-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5f664-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f664-127">Header</span></span><br/>       | <dl> <span data-ttu-id="5f664-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f664-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




