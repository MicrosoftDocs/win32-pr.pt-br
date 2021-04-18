---
description: As \_ constantes de sinalizador de bit LINEFORWARDMODE descrevem as condições sob as quais as chamadas para um endereço podem ser encaminhadas.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes de LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779899"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="1d61a-103">\_Constantes LINEFORWARDMODE</span><span class="sxs-lookup"><span data-stu-id="1d61a-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="1d61a-104">As constantes de sinalizador de bit **LINEFORWARDMODE \_** descrevem as condições sob as quais as chamadas para um endereço podem ser encaminhadas.</span><span class="sxs-lookup"><span data-stu-id="1d61a-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="1d61a-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="1d61a-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-106">Encaminhe todas as chamadas em ocupado, independentemente de sua origem.</span><span class="sxs-lookup"><span data-stu-id="1d61a-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="1d61a-107">Use esse valor ao encaminhar para chamadas internas e externas em ocupado e sem resposta não podem ser controladas separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-109">Encaminhar todas as chamadas externas em ocupado.</span><span class="sxs-lookup"><span data-stu-id="1d61a-109">Forward all external calls on busy.</span></span> <span data-ttu-id="1d61a-110">Use esse valor quando o encaminhamento para chamadas internas e externas em ocupado e sem resposta puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-112">Encaminhar todas as chamadas internas em ocupado.</span><span class="sxs-lookup"><span data-stu-id="1d61a-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="1d61a-113">Use esse valor quando o encaminhamento para chamadas internas e externas em ocupado e sem resposta puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**</span><span class="sxs-lookup"><span data-stu-id="1d61a-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-115">Encaminhe todas as chamadas para ocupado/sem resposta, independentemente de sua origem.</span><span class="sxs-lookup"><span data-stu-id="1d61a-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="1d61a-116">Use esse valor ao encaminhar para chamadas internas e externas em ocupado e sem resposta não podem ser controladas separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-118">Encaminhe todas as chamadas externas para ocupado/sem resposta.</span><span class="sxs-lookup"><span data-stu-id="1d61a-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="1d61a-119">Use este valor quando o encaminhamento de chamadas em ocupado e sem resposta não puder ser controlado separadamente para chamadas internas.</span><span class="sxs-lookup"><span data-stu-id="1d61a-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-121">Encaminhe todas as chamadas internas em resposta/não.</span><span class="sxs-lookup"><span data-stu-id="1d61a-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="1d61a-122">Use este valor quando o encaminhamento de chamadas em ocupado e sem resposta não puder ser controlado separadamente para chamadas internas.</span><span class="sxs-lookup"><span data-stu-id="1d61a-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="1d61a-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-124">Encaminhar em ocupado/não responder a todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).</span><span class="sxs-lookup"><span data-stu-id="1d61a-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="1d61a-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-126">Encaminhar em ocupado todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).</span><span class="sxs-lookup"><span data-stu-id="1d61a-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**</span><span class="sxs-lookup"><span data-stu-id="1d61a-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-128">Encaminhe todas as chamadas sem resposta, independentemente de sua origem.</span><span class="sxs-lookup"><span data-stu-id="1d61a-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="1d61a-129">Use esse valor quando o encaminhamento de chamada para chamadas internas e externas sem resposta não puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-131">Encaminhe todas as chamadas externas sem resposta.</span><span class="sxs-lookup"><span data-stu-id="1d61a-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="1d61a-132">Usar esse valor ao encaminhar para chamadas internas e externas sem resposta pode ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-134">Encaminhe todas as chamadas internas sem resposta.</span><span class="sxs-lookup"><span data-stu-id="1d61a-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="1d61a-135">Usar esse valor ao encaminhar para chamadas internas e externas sem resposta pode ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="1d61a-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-137">Encaminhar sem responder a todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).</span><span class="sxs-lookup"><span data-stu-id="1d61a-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="1d61a-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-139">As chamadas são encaminhadas, mas as condições sob as quais o encaminhamento ocorrerão não são conhecidas e nunca serão conhecidas pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1d61a-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="1d61a-140">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="1d61a-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNCOND**</span><span class="sxs-lookup"><span data-stu-id="1d61a-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-142">Encaminhe todas as chamadas incondicionalmente, independentemente de sua origem.</span><span class="sxs-lookup"><span data-stu-id="1d61a-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="1d61a-143">Use esse valor quando o encaminhamento incondicional para chamadas internas e externas não puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="1d61a-144">O encaminhamento incondicional de substituições em direção ao ocupado e/ou nenhuma condição de resposta.</span><span class="sxs-lookup"><span data-stu-id="1d61a-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-146">Encaminhe todas as chamadas externas incondicionalmente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="1d61a-147">Use esse valor quando o encaminhamento incondicional para chamadas internas e externas puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="1d61a-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-149">Encaminhe todas as chamadas internas incondicionalmente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="1d61a-150">Use esse valor quando o encaminhamento incondicional para chamadas internas e externas puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="1d61a-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-152">Encaminhe incondicionalmente todas as chamadas originadas em um endereço especificado (encaminhamento de chamada seletiva).</span><span class="sxs-lookup"><span data-stu-id="1d61a-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1d61a-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="1d61a-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1d61a-154">As chamadas são encaminhadas, mas as condições sob as quais o encaminhamento ocorrerão não são conhecidas neste momento.</span><span class="sxs-lookup"><span data-stu-id="1d61a-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="1d61a-155">É possível que as condições sejam conhecidas em um momento futuro.</span><span class="sxs-lookup"><span data-stu-id="1d61a-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="1d61a-156">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="1d61a-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d61a-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d61a-157">Remarks</span></span>

<span data-ttu-id="1d61a-158">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="1d61a-158">No extensibility.</span></span> <span data-ttu-id="1d61a-159">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="1d61a-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="1d61a-160">Os sinalizadores de bits definidos por LINEFORWARDMODE \_ não são ortogonal.</span><span class="sxs-lookup"><span data-stu-id="1d61a-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="1d61a-161">O encaminhamento incondicional ignora qualquer condição específica, como ocupado ou sem resposta.</span><span class="sxs-lookup"><span data-stu-id="1d61a-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="1d61a-162">Se o encaminhamento incondicional não estiver em vigor, o encaminhamento em ocupado e sem resposta poderá ser controlado separadamente ou não separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="1d61a-163">Se controlado separadamente, os \_ sinalizadores LINEFORWARDMODE Busy e LINEFORWARDMODE \_ NOANSW podem ser usados separadamente.</span><span class="sxs-lookup"><span data-stu-id="1d61a-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="1d61a-164">Se não for controlado separadamente, o sinalizador LINEFORWARDMODE \_ BUSYNA deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="1d61a-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="1d61a-165">Da mesma forma, se o encaminhamento de chamadas internas e externas puder ser controlado separadamente, \_ os sinalizadores externos LINEFORWARDMODE internos e LINEFORWARDMODE \_ poderão ser usados separadamente; caso contrário, a combinação será usada.</span><span class="sxs-lookup"><span data-stu-id="1d61a-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="1d61a-166">Os recursos de endereço indicam quais modos de encaminhamento estão disponíveis para cada endereço atribuído a uma linha.</span><span class="sxs-lookup"><span data-stu-id="1d61a-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="1d61a-167">Um aplicativo pode usar [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) para definir as condições de encaminhamento no comutador.</span><span class="sxs-lookup"><span data-stu-id="1d61a-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="1d61a-168">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINEFORWARDMODE \_ se a versão negociada não oferecer suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="1d61a-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d61a-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d61a-169">Requirements</span></span>



| <span data-ttu-id="1d61a-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d61a-170">Requirement</span></span> | <span data-ttu-id="1d61a-171">Valor</span><span class="sxs-lookup"><span data-stu-id="1d61a-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1d61a-172">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1d61a-172">TAPI version</span></span><br/> | <span data-ttu-id="1d61a-173">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1d61a-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1d61a-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d61a-174">Header</span></span><br/>       | <dl> <span data-ttu-id="1d61a-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d61a-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




