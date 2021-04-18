---
title: Códigos de erro de animação do Windows (Winerror. h)
description: Se ocorrer um erro, a animação do Windows retornará um código como um valor HRESULT. Esta seção fornece uma lista de códigos de erro específicos da animação do Windows. Para obter uma lista de códigos de erro COM gerais, consulte códigos de erro COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788856"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="6bc0a-105">Códigos de erro de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="6bc0a-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="6bc0a-106">Se ocorrer um erro, a animação do Windows retornará um código como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bc0a-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="6bc0a-107">Esta seção fornece uma lista de códigos de erro específicos da animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="6bc0a-108">Para obter uma lista de códigos de erro COM gerais, consulte [códigos de erro com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6bc0a-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6bc0a-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ falha na criação da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="6bc0a-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-111">Não foi possível criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**interface de usuário \_ E \_ desligamento \_ chamada**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="6bc0a-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-114">O método de [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) foi chamado no Gerenciador de animação, fazendo com que o Gerenciador de animação seja desligado e todas as variáveis de animação e Storyboards criados para serem liberados.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="6bc0a-115">Nenhum método pode ser chamado em qualquer objeto de animação após o [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span><span class="sxs-lookup"><span data-stu-id="6bc0a-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**IU \_ E \_ \_ reentrância ilegal**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="6bc0a-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-118">Este método não pode ser chamado durante esse tipo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI \_ E \_ objeto \_ lacrado**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="6bc0a-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-121">Este objeto foi lacrado, portanto, essa alteração não é mais permitida.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**valor de IU \_ E \_ \_ não \_ definido**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="6bc0a-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-124">O valor solicitado nunca foi definido e, portanto, não pode ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**valor de IU \_ E \_ \_ não \_ determinado**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="6bc0a-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-127">O valor solicitado não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**saída de interface de usuário \_ E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="6bc0a-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-130">Um retorno de chamada retornou um parâmetro de saída inválido.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**interface do usuário \_ E \_ booliano \_ esperado**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="6bc0a-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-133">Um retorno de chamada retornou um código de êxito diferente de S \_ OK ou s \_ false.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**IU \_ E \_ \_ proprietário diferente**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="6bc0a-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-136">Um parâmetro que deve pertencer a esse objeto pertence a um objeto diferente.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ correspondência ambígua E de interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="6bc0a-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-139">Mais de um item correspondeu aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**estouro de IU \_ E \_ FP \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="6bc0a-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-142">Ocorreu um estouro de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**interface de usuário \_ E \_ thread incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="6bc0a-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-145">Esse método só pode ser chamado a partir do thread que criou o objeto.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**interface do usuário \_ E \_ storyboard \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="6bc0a-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-148">O storyboard está atualmente na agenda.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**a interface do usuário \_ E o \_ Storyboard não estão em \_ \_ execução**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="6bc0a-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-151">O storyboard não está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**IU \_ E \_ \_ quadro-chave inicial após o \_ \_ final**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="6bc0a-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-154">O quadro-chave inicial pode ocorrer após o quadro-chave final.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**quadro-chave de término da interface do usuário \_ \_ \_ \_ não \_ determinado**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="6bc0a-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-157">Pode não ser possível determinar a hora do quadro-chave final quando o quadro chave inicial é atingido.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**sobreposição de \_ \_ loops E de interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="6bc0a-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-160">Duas partes repetidas de um storyboard podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**interface do usuário \_ E \_ transição \_ já \_ usada**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="6bc0a-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-163">A transição já foi adicionada a um storyboard diferente ou foi adicionada a um Storyboard que terminou de ser reproduzido e liberada.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**a \_ transição de interface do usuário E \_ não está \_ \_ no \_ storyboard**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="6bc0a-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-166">A transição não foi adicionada a nenhum Storyboard.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transição de interface do usuário \_ E \_ \_ Eclipse**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="6bc0a-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-169">A transição pode ocultar o início de outra transição no storyboard.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_tempo E \_ hora da IU antes da \_ \_ última \_ atualização**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="6bc0a-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-172">A hora especificada é anterior à hora passada para a última atualização.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bc0a-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_cliente do temporizador E de interface do usuário \_ \_ \_ já \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="6bc0a-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bc0a-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="6bc0a-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="6bc0a-175">Este cliente já está conectado a um temporizador.</span><span class="sxs-lookup"><span data-stu-id="6bc0a-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bc0a-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc0a-176">Requirements</span></span>



| <span data-ttu-id="6bc0a-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc0a-177">Requirement</span></span> | <span data-ttu-id="6bc0a-178">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc0a-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc0a-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc0a-179">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc0a-180">Windows 7, Windows Vista e atualização de plataforma para aplicativos de área de trabalho do Windows Vista \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="6bc0a-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6bc0a-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc0a-181">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc0a-182">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6bc0a-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="6bc0a-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bc0a-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bc0a-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc0a-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="6bc0a-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bc0a-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc0a-186">Referência de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="6bc0a-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

