---
title: Sinalizadores de ponteiro
description: Os valores que podem aparecer no campo pointerFlags da estrutura de POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644857"
---
# <a name="pointer-flags"></a><span data-ttu-id="fdd5a-103">Sinalizadores de ponteiro</span><span class="sxs-lookup"><span data-stu-id="fdd5a-103">Pointer Flags</span></span>

<span data-ttu-id="fdd5a-104">Os valores que podem aparecer no campo **pointerFlags** da estrutura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fdd5a-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="fdd5a-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-107">Padrão</span><span class="sxs-lookup"><span data-stu-id="fdd5a-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fdd5a-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-110">Indica a chegada de um novo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fdd5a-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-113">Indica que esse ponteiro continua a existir.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="fdd5a-114">Quando esse sinalizador não é definido, ele indica que o ponteiro tem um intervalo de detecção à esquerda.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="fdd5a-115">Esse sinalizador normalmente não é definido somente quando um ponteiro em foco deixa o intervalo de detecção (**POINTER_FLAG_UPDATE** é definido) ou quando um ponteiro em contato com uma superfície de janela sai do intervalo de detecção (**POINTER_FLAG_UP** é definido).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="fdd5a-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-118">Indica que esse ponteiro está em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="fdd5a-119">Quando esse sinalizador não é definido, ele indica um ponteiro em foco.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdd5a-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-122">Indica uma ação primária, análoga a um botão esquerdo do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="fdd5a-123">Um ponteiro de toque tem esse sinalizador definido quando ele está em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="fdd5a-124">Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora sem botões pressionados.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="fdd5a-125">Um ponteiro do mouse tem esse sinalizador definido quando o botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="fdd5a-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-128">Indica uma ação secundária, análoga a um botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="fdd5a-129">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-130">Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora com o botão de rosca de caneta pressionado.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="fdd5a-131">Um ponteiro do mouse tem esse sinalizador definido quando o botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="fdd5a-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-134">Análogo a um botão de roda do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="fdd5a-135">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-136">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-137">Um ponteiro do mouse tem esse sinalizador definido quando o botão da roda do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="fdd5a-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-140">Análogo a um botão do primeiro mouse estendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="fdd5a-141">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-142">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-143">Um ponteiro do mouse tem esse sinalizador definido quando o botão do primeiro mouse estendido (XBUTTON1) está inoperante.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="fdd5a-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-146">Análogo a um segundo botão do mouse estendido (XButton2).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="fdd5a-147">Um ponteiro de toque não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-148">Um ponteiro de caneta não usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="fdd5a-149">Um ponteiro do mouse tem esse sinalizador definido quando o segundo botão do mouse estendido (XBUTTON2) está inoperante.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-152">Indica que esse ponteiro foi designado como o ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="fdd5a-153">Um ponteiro principal é um único ponteiro que pode executar ações além daquelas disponíveis para ponteiros não primários.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="fdd5a-154">Por exemplo, quando um ponteiro principal faz contato com uma superfície da janela, ele pode fornecer à janela uma oportunidade de ativação, enviando a ele uma mensagem [**WM_POINTERACTIVATE**](wm-pointeractivate.md) .</span><span class="sxs-lookup"><span data-stu-id="fdd5a-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="fdd5a-155">O ponteiro principal é identificado de todas as interações atuais do usuário no sistema (mouse, toque, caneta e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="fdd5a-156">Como tal, o ponteiro principal pode não estar associado ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="fdd5a-157">O primeiro contato em uma interação multitoque é definido como o ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="fdd5a-158">Depois que um ponteiro principal é identificado, todos os contatos devem ser levantados antes que um novo contato possa ser identificado como um ponteiro principal.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="fdd5a-159">Para aplicativos que não processam a entrada do ponteiro, somente os eventos do ponteiro principal são promovidos para eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-162">Confiança é uma sugestão do dispositivo de origem sobre se o ponteiro representa uma interação pretendida ou acidental, que é especialmente relevante para ponteiros de PT_TOUCH em que uma interação acidental (como com a palma da mão) pode disparar a entrada.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="fdd5a-163">A presença desse sinalizador indica que o dispositivo de origem tem alta confiança de que essa entrada faz parte de uma interação pretendida.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-166">Indica que o ponteiro está se deparando de forma anormal, por exemplo, quando o sistema recebe uma entrada inválida para o ponteiro ou quando um dispositivo com ponteiros ativos faz parte abruptamente.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="fdd5a-167">Se o aplicativo que está recebendo a entrada estiver em uma posição para fazer isso, ele deverá tratar a interação como não concluída e inverter os efeitos do ponteiro preocupado.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-170">Indica que esse ponteiro fez a transição para um estado inativo; ou seja, ele fez contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-173">Indica que se trata de uma atualização simples que não inclui alterações de estado de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-176">Indica que esse ponteiro fez a transição para um estado ativo; ou seja, o contato com a superfície do digitalizador terminou.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-179">Indica a entrada associada a uma roda de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="fdd5a-180">Para ponteiros do mouse, isso é equivalente à ação da roda de rolagem do mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-183">Indica a entrada associada a um ponteiro h-Wheel.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="fdd5a-184">Para ponteiros do mouse, isso é equivalente à ação da roda de rolagem horizontal do mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-187">Indica que esse ponteiro foi capturado por (associado a) outro elemento e o elemento original perdeu a captura (consulte [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="fdd5a-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdd5a-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdd5a-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="fdd5a-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="fdd5a-190">Indica que esse ponteiro tem uma transformação associada.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdd5a-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd5a-191">Remarks</span></span>

<span data-ttu-id="fdd5a-192">XBUTTON1 e XBUTTON2 são botões adicionais usados em vários dispositivos de mouse.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="fdd5a-193">Eles retornam os mesmos dados que os botões padrão do mouse.</span><span class="sxs-lookup"><span data-stu-id="fdd5a-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd5a-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd5a-194">Requirements</span></span>



| <span data-ttu-id="fdd5a-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd5a-195">Requirement</span></span> | <span data-ttu-id="fdd5a-196">Valor</span><span class="sxs-lookup"><span data-stu-id="fdd5a-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd5a-197">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd5a-197">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd5a-198">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fdd5a-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fdd5a-199">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd5a-199">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd5a-200">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fdd5a-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fdd5a-201">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdd5a-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd5a-202"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd5a-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd5a-203">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fdd5a-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd5a-204">Constantes</span><span class="sxs-lookup"><span data-stu-id="fdd5a-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="fdd5a-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fdd5a-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="fdd5a-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

