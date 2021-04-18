---
title: Sinalizadores de mensagem do ponteiro
description: Valores que são usados em várias macros de ponteiro (consulte as macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780741"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="32d4c-103">Sinalizadores de mensagem do ponteiro</span><span class="sxs-lookup"><span data-stu-id="32d4c-103">Pointer Message Flags</span></span>

<span data-ttu-id="32d4c-104">Valores que são usados em várias macros de ponteiro (consulte [as macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="32d4c-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="32d4c-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="32d4c-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="32d4c-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-107">Indica a chegada de um novo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="32d4c-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="32d4c-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="32d4c-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-110">Indica que esse ponteiro continua a existir.</span><span class="sxs-lookup"><span data-stu-id="32d4c-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="32d4c-111">Quando esse sinalizador não é definido, ele indica que o ponteiro tem um intervalo de detecção à esquerda.</span><span class="sxs-lookup"><span data-stu-id="32d4c-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="32d4c-112">Esse sinalizador normalmente não é definido somente quando um ponteiro em foco deixa o intervalo de detecção (**POINTER_FLAG_UPDATE** é definido) ou quando um ponteiro em contato com uma superfície de janela sai do intervalo de detecção (**POINTER_FLAG_UP** é definido).</span><span class="sxs-lookup"><span data-stu-id="32d4c-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="32d4c-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="32d4c-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-115">Indica que esse ponteiro está em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="32d4c-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="32d4c-116">Quando esse sinalizador não é definido, ele indica um ponteiro em foco.</span><span class="sxs-lookup"><span data-stu-id="32d4c-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="32d4c-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32d4c-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-119">Indica uma ação primária, análoga a um botão esquerdo do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="32d4c-120">Um ponteiro de toque tem esse sinalizador definido quando ele está em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="32d4c-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="32d4c-121">Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora sem botões pressionados.</span><span class="sxs-lookup"><span data-stu-id="32d4c-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="32d4c-122">Um ponteiro do mouse tem esse sinalizador definido quando o botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="32d4c-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="32d4c-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-125">Indica uma ação secundária, análoga a um botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="32d4c-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="32d4c-126">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-127">Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora com o botão de rosca de caneta pressionado.</span><span class="sxs-lookup"><span data-stu-id="32d4c-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="32d4c-128">Um ponteiro do mouse tem esse sinalizador definido quando o botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="32d4c-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="32d4c-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-131">Análogo a um botão de roda do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="32d4c-132">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-133">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-134">Um ponteiro do mouse tem esse sinalizador definido quando o botão da roda do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="32d4c-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="32d4c-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-137">Análogo a um botão do primeiro mouse estendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="32d4c-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="32d4c-138">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-139">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-140">Um ponteiro do mouse tem esse sinalizador definido quando o botão do primeiro mouse estendido (XBUTTON1) está inoperante.</span><span class="sxs-lookup"><span data-stu-id="32d4c-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="32d4c-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="32d4c-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-143">Análogo a um segundo botão do mouse estendido (XButton2).</span><span class="sxs-lookup"><span data-stu-id="32d4c-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="32d4c-144">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-145">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="32d4c-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="32d4c-146">Um ponteiro do mouse tem esse sinalizador definido quando o segundo botão do mouse estendido (XBUTTON2) está inoperante.</span><span class="sxs-lookup"><span data-stu-id="32d4c-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="32d4c-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="32d4c-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-149">Indica que esse ponteiro foi designado como o ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="32d4c-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="32d4c-150">Um ponteiro principal é um único ponteiro que pode executar ações além daquelas disponíveis para ponteiros não primários.</span><span class="sxs-lookup"><span data-stu-id="32d4c-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="32d4c-151">Por exemplo, quando um ponteiro principal faz contato com uma superfície da janela, ele pode fornecer à janela uma oportunidade de ativação, enviando a ele uma mensagem WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="32d4c-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="32d4c-152">O ponteiro principal é identificado de todas as interações atuais do usuário no sistema (mouse, toque, caneta e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="32d4c-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="32d4c-153">Como tal, o ponteiro principal pode não estar associado ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="32d4c-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="32d4c-154">O primeiro contato em uma interação multitoque é definido como o ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="32d4c-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="32d4c-155">Depois que um ponteiro principal é identificado, todos os contatos devem ser levantados antes que um novo contato possa ser identificado como um ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="32d4c-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="32d4c-156">Para aplicativos que não processam a entrada do ponteiro, somente os eventos do ponteiro principal são promovidos para eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="32d4c-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="32d4c-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="32d4c-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-159">Confiança é uma sugestão do dispositivo de origem sobre se o ponteiro representa uma interação pretendida ou acidental, que é especialmente relevante para ponteiros de PT_TOUCH em que uma interação acidental (como com a palma da mão) pode disparar a entrada.</span><span class="sxs-lookup"><span data-stu-id="32d4c-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="32d4c-160">A presença desse sinalizador indica que o dispositivo de origem tem alta confiança de que essa entrada faz parte de uma interação pretendida.</span><span class="sxs-lookup"><span data-stu-id="32d4c-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="32d4c-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="32d4c-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32d4c-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="32d4c-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="32d4c-163">Indica que o ponteiro está se deparando de forma anormal, por exemplo, quando o sistema recebe uma entrada inválida para o ponteiro ou quando um dispositivo com ponteiros ativos faz parte abruptamente.</span><span class="sxs-lookup"><span data-stu-id="32d4c-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="32d4c-164">Se o aplicativo que está recebendo a entrada estiver em uma posição para fazer isso, ele deverá tratar a interação como não concluída e inverter os efeitos do ponteiro preocupado.</span><span class="sxs-lookup"><span data-stu-id="32d4c-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32d4c-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="32d4c-165">Remarks</span></span>

<span data-ttu-id="32d4c-166">XBUTTON1 e XBUTTON2 são botões adicionais usados em vários dispositivos de mouse.</span><span class="sxs-lookup"><span data-stu-id="32d4c-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="32d4c-167">Eles retornam os mesmos dados que os botões padrão do mouse.</span><span class="sxs-lookup"><span data-stu-id="32d4c-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="32d4c-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32d4c-168">Requirements</span></span>



| <span data-ttu-id="32d4c-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d4c-169">Requirement</span></span> | <span data-ttu-id="32d4c-170">Valor</span><span class="sxs-lookup"><span data-stu-id="32d4c-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32d4c-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32d4c-171">Minimum supported client</span></span><br/> | <span data-ttu-id="32d4c-172">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="32d4c-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="32d4c-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32d4c-173">Minimum supported server</span></span><br/> | <span data-ttu-id="32d4c-174">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="32d4c-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32d4c-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32d4c-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="32d4c-176"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d4c-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32d4c-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="32d4c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d4c-178">Constantes</span><span class="sxs-lookup"><span data-stu-id="32d4c-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="32d4c-179">Macros</span><span class="sxs-lookup"><span data-stu-id="32d4c-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





