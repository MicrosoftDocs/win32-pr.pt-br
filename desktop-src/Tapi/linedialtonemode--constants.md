---
description: As \_ constantes de sinalizador de bit LINEDIALTONEMODE descrevem tipos diferentes de tons de discagem. Um tom de discagem especial normalmente apresenta um significado especial (assim como acontece com a mensagem em espera).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes de LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792615"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="4bc29-104">\_Constantes LINEDIALTONEMODE</span><span class="sxs-lookup"><span data-stu-id="4bc29-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="4bc29-105">As constantes de sinalizador de bit **LINEDIALTONEMODE \_** descrevem tipos diferentes de tons de discagem.</span><span class="sxs-lookup"><span data-stu-id="4bc29-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="4bc29-106">Um tom de discagem especial normalmente apresenta um significado especial (assim como acontece com a mensagem em espera).</span><span class="sxs-lookup"><span data-stu-id="4bc29-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="4bc29-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externo**</span><span class="sxs-lookup"><span data-stu-id="4bc29-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-108">Este é um tom de discagem externo (rede pública).</span><span class="sxs-lookup"><span data-stu-id="4bc29-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc29-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**</span><span class="sxs-lookup"><span data-stu-id="4bc29-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-110">Esse é um tom de discagem interna, como em um PBX.</span><span class="sxs-lookup"><span data-stu-id="4bc29-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc29-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="4bc29-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-112">Esse é um tom de discagem normal, que normalmente é um tom contínuo.</span><span class="sxs-lookup"><span data-stu-id="4bc29-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc29-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ especial**</span><span class="sxs-lookup"><span data-stu-id="4bc29-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-114">Esse é um tom de discagem especial que indica que uma determinada condição (conhecida pelo comutador ou pela rede) está em vigor no momento.</span><span class="sxs-lookup"><span data-stu-id="4bc29-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="4bc29-115">Os tons de discagem especiais normalmente usam um tom interrompido.</span><span class="sxs-lookup"><span data-stu-id="4bc29-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="4bc29-116">Assim como com um tom de discagem normal, isso indica que a opção está pronta para receber o número a ser discado.</span><span class="sxs-lookup"><span data-stu-id="4bc29-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc29-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="4bc29-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-118">O modo de Tom de discagem não está disponível e não se tornará conhecido.</span><span class="sxs-lookup"><span data-stu-id="4bc29-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc29-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="4bc29-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4bc29-120">O modo de Tom de discagem não é conhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4bc29-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bc29-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4bc29-121">Remarks</span></span>

<span data-ttu-id="4bc29-122">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bc29-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="4bc29-123">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="4bc29-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="4bc29-124">As **\_ constantes LINEDIALTONEMODE** são usadas na estrutura de dados [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para uma chamada no estado de disinalização.</span><span class="sxs-lookup"><span data-stu-id="4bc29-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc29-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bc29-125">Requirements</span></span>



| <span data-ttu-id="4bc29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bc29-126">Requirement</span></span> | <span data-ttu-id="4bc29-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4bc29-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4bc29-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4bc29-128">TAPI version</span></span><br/> | <span data-ttu-id="4bc29-129">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4bc29-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4bc29-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bc29-130">Header</span></span><br/>       | <dl> <span data-ttu-id="4bc29-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bc29-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




