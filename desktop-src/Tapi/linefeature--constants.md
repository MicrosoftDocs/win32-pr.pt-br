---
description: As \_ constantes LINEFEATURE listam as operações que podem ser invocadas em uma linha usando essa API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes de LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754733"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="b64fb-103">\_Constantes LINEFEATURE</span><span class="sxs-lookup"><span data-stu-id="b64fb-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="b64fb-104">As **\_ constantes LINEFEATURE** listam as operações que podem ser invocadas em uma linha usando essa API.</span><span class="sxs-lookup"><span data-stu-id="b64fb-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="b64fb-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="b64fb-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-106">Operações específicas do dispositivo podem ser usadas na linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**</span><span class="sxs-lookup"><span data-stu-id="b64fb-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-108">Recursos específicos do dispositivo podem ser usados na linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**encaminhar LINEFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="b64fb-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-110">O encaminhamento de todos os endereços pode ser usado na linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="b64fb-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-112">A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (com um endereço de destino vazio) pode ser usada para ativar o recurso não incomodar em todos os endereços na linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="b64fb-113">O LINEFEATURE \_ Forward também será definido.</span><span class="sxs-lookup"><span data-stu-id="b64fb-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="b64fb-114">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b64fb-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="b64fb-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-116">A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pode ser usada para encaminhar chamadas em todos os endereços na linha para outros números.</span><span class="sxs-lookup"><span data-stu-id="b64fb-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="b64fb-117">O LINEFEATURE \_ Forward também será definido.</span><span class="sxs-lookup"><span data-stu-id="b64fb-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="b64fb-118">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b64fb-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="b64fb-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-120">Uma chamada de saída pode ser colocada nessa linha usando um endereço não especificado.</span><span class="sxs-lookup"><span data-stu-id="b64fb-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="b64fb-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-122">A função [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) pode ser invocada no dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="b64fb-123">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b64fb-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="b64fb-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-125">O controle de mídia pode ser definido nessa linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b64fb-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETterminal**</span><span class="sxs-lookup"><span data-stu-id="b64fb-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b64fb-127">Os modos de terminal para essa linha podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="b64fb-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="b64fb-128">Se nenhum dos novos bits "encaminhar" modificados estiver definido no membro **dwLineFeatures** em [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , mas o \_ bit de encaminhamento LINEFEATURE for definido, qualquer um dos modos de encaminhamento poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.</span><span class="sxs-lookup"><span data-stu-id="b64fb-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b64fb-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b64fb-129">Remarks</span></span>

<span data-ttu-id="b64fb-130">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="b64fb-130">No extensibility.</span></span> <span data-ttu-id="b64fb-131">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="b64fb-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="b64fb-132">As \_ constantes LINEFEATURE são usadas em [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (retornado por [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span><span class="sxs-lookup"><span data-stu-id="b64fb-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="b64fb-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) relatórios, para uma determinada linha, quais recursos de linha podem ser realmente invocados enquanto a linha está no estado atual.</span><span class="sxs-lookup"><span data-stu-id="b64fb-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="b64fb-134">Um aplicativo tornaria essa determinação dinâmica após as alterações de estado de linha, geralmente causada por endereço ou atividades relacionadas à chamada na linha.</span><span class="sxs-lookup"><span data-stu-id="b64fb-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64fb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64fb-135">Requirements</span></span>



| <span data-ttu-id="b64fb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64fb-136">Requirement</span></span> | <span data-ttu-id="b64fb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b64fb-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b64fb-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b64fb-138">TAPI version</span></span><br/> | <span data-ttu-id="b64fb-139">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b64fb-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b64fb-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b64fb-140">Header</span></span><br/>       | <dl> <span data-ttu-id="b64fb-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64fb-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64fb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b64fb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64fb-143">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="b64fb-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="b64fb-144">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="b64fb-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="b64fb-145">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="b64fb-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="b64fb-146">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="b64fb-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




