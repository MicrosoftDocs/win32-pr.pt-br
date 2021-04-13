---
title: Mensagem de WM_SYSKEYUP (WinUser. h)
description: Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era mantida pressionada.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Entrada de mouse e teclado de mensagem WM_SYSKEYUP
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298060"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="99199-104">Mensagem do WM \_ SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="99199-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="99199-105">Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era mantida pressionada.</span><span class="sxs-lookup"><span data-stu-id="99199-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="99199-106">Ele também ocorre quando nenhuma janela tem o foco do teclado no momento; Nesse caso, a mensagem do **WM \_ SYSKEYUP** é enviada para a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="99199-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="99199-107">A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="99199-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="99199-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99199-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="99199-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99199-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99199-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99199-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99199-111">O código de chave virtual da chave que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="99199-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="99199-112">Consulte [**códigos de chave virtual**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="99199-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="99199-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99199-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99199-114">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="99199-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="99199-115">Bits</span><span class="sxs-lookup"><span data-stu-id="99199-115">Bits</span></span>  | <span data-ttu-id="99199-116">Significado</span><span class="sxs-lookup"><span data-stu-id="99199-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99199-117">0-15</span><span class="sxs-lookup"><span data-stu-id="99199-117">0-15</span></span>  | <span data-ttu-id="99199-118">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="99199-118">The repeat count for the current message.</span></span> <span data-ttu-id="99199-119">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="99199-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="99199-120">A contagem de repetição é sempre uma para uma mensagem do **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="99199-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="99199-121">16-23</span><span class="sxs-lookup"><span data-stu-id="99199-121">16-23</span></span> | <span data-ttu-id="99199-122">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="99199-122">The scan code.</span></span> <span data-ttu-id="99199-123">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="99199-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="99199-124">24</span><span class="sxs-lookup"><span data-stu-id="99199-124">24</span></span>    | <span data-ttu-id="99199-125">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="99199-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="99199-126">O valor será 1 se for uma chave estendida; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="99199-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="99199-127">25-28</span><span class="sxs-lookup"><span data-stu-id="99199-127">25-28</span></span> | <span data-ttu-id="99199-128">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="99199-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="99199-129">29</span><span class="sxs-lookup"><span data-stu-id="99199-129">29</span></span>    | <span data-ttu-id="99199-130">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="99199-130">The context code.</span></span> <span data-ttu-id="99199-131">O valor será 1 se a tecla ALT estiver inoperante enquanto a chave for liberada; será zero se a mensagem do **WM \_ SYSKEYUP** for postada na janela ativa porque nenhuma janela tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="99199-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="99199-132">30</span><span class="sxs-lookup"><span data-stu-id="99199-132">30</span></span>    | <span data-ttu-id="99199-133">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="99199-133">The previous key state.</span></span> <span data-ttu-id="99199-134">O valor é sempre 1 para uma mensagem do **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="99199-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="99199-135">31</span><span class="sxs-lookup"><span data-stu-id="99199-135">31</span></span>    | <span data-ttu-id="99199-136">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="99199-136">The transition state.</span></span> <span data-ttu-id="99199-137">O valor é sempre 1 para uma mensagem do **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="99199-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="99199-138">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="99199-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99199-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99199-139">Return value</span></span>

<span data-ttu-id="99199-140">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="99199-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="99199-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="99199-141">Remarks</span></span>

<span data-ttu-id="99199-142">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior se a tecla F10 ou a tecla Alt foi liberada.</span><span class="sxs-lookup"><span data-stu-id="99199-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="99199-143">O parâmetro *wParam* da mensagem é definido como **sc \_ keymenu**.</span><span class="sxs-lookup"><span data-stu-id="99199-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="99199-144">Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caracteres.</span><span class="sxs-lookup"><span data-stu-id="99199-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="99199-145">Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="99199-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="99199-146">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="99199-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="99199-147">Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="99199-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="99199-148">Para não-U. S. teclados avançados de 102 teclas, a tecla ALT direita é tratada como uma tecla CTRL + ALT.</span><span class="sxs-lookup"><span data-stu-id="99199-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="99199-149">A tabela a seguir mostra a sequência de mensagens que resultam quando o usuário pressiona e libera essa chave.</span><span class="sxs-lookup"><span data-stu-id="99199-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="99199-150">Mensagem</span><span class="sxs-lookup"><span data-stu-id="99199-150">Message</span></span>                           | <span data-ttu-id="99199-151">Código de chave virtual</span><span class="sxs-lookup"><span data-stu-id="99199-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="99199-152">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="99199-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="99199-153">**\_controle VK**</span><span class="sxs-lookup"><span data-stu-id="99199-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="99199-154">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="99199-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="99199-155">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="99199-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="99199-156">**o WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="99199-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="99199-157">**\_controle VK**</span><span class="sxs-lookup"><span data-stu-id="99199-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="99199-158">**SYSKEYUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="99199-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="99199-159">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="99199-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="99199-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99199-160">Requirements</span></span>



| <span data-ttu-id="99199-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="99199-161">Requirement</span></span> | <span data-ttu-id="99199-162">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99199-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99199-163">Minimum supported client</span></span><br/> | <span data-ttu-id="99199-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99199-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99199-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99199-165">Minimum supported server</span></span><br/> | <span data-ttu-id="99199-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99199-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99199-167">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99199-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="99199-168"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99199-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99199-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="99199-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="99199-170">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99199-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99199-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="99199-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="99199-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="99199-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="99199-173">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="99199-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="99199-174">**SYSKEYDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="99199-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="99199-175">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="99199-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99199-176">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="99199-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

