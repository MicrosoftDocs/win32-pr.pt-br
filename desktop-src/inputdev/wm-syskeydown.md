---
title: Mensagem de WM_SYSKEYDOWN (WinUser. h)
description: Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e, em seguida, pressiona outra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Entrada de mouse e teclado de mensagem WM_SYSKEYDOWN
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794567"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="c7d5f-104">Mensagem do WM \_ SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="c7d5f-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="c7d5f-105">Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e, em seguida, pressiona outra tecla.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="c7d5f-106">Ele também ocorre quando nenhuma janela tem o foco do teclado no momento; Nesse caso, a mensagem do **WM \_ SYSKEYDOWN** é enviada para a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="c7d5f-107">A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c7d5f-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="c7d5f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7d5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7d5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d5f-110">O código de chave virtual da chave que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="c7d5f-111">Consulte [**códigos de chave virtual**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c7d5f-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7d5f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7d5f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d5f-113">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="c7d5f-114">Bits</span><span class="sxs-lookup"><span data-stu-id="c7d5f-114">Bits</span></span>  | <span data-ttu-id="c7d5f-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c7d5f-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d5f-116">0-15</span><span class="sxs-lookup"><span data-stu-id="c7d5f-116">0-15</span></span>  | <span data-ttu-id="c7d5f-117">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-117">The repeat count for the current message.</span></span> <span data-ttu-id="c7d5f-118">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="c7d5f-119">Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="c7d5f-120">No entanto, a contagem de repetição não é cumulativa.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="c7d5f-121">16-23</span><span class="sxs-lookup"><span data-stu-id="c7d5f-121">16-23</span></span> | <span data-ttu-id="c7d5f-122">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-122">The scan code.</span></span> <span data-ttu-id="c7d5f-123">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c7d5f-124">24</span><span class="sxs-lookup"><span data-stu-id="c7d5f-124">24</span></span>    | <span data-ttu-id="c7d5f-125">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="c7d5f-126">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="c7d5f-127">25-28</span><span class="sxs-lookup"><span data-stu-id="c7d5f-127">25-28</span></span> | <span data-ttu-id="c7d5f-128">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c7d5f-129">29</span><span class="sxs-lookup"><span data-stu-id="c7d5f-129">29</span></span>    | <span data-ttu-id="c7d5f-130">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-130">The context code.</span></span> <span data-ttu-id="c7d5f-131">O valor será 1 se a tecla ALT estiver inoperante enquanto a tecla for pressionada; será 0 se a mensagem do **WM \_ SYSKEYDOWN** for postada na janela ativa porque nenhuma janela tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="c7d5f-132">30</span><span class="sxs-lookup"><span data-stu-id="c7d5f-132">30</span></span>    | <span data-ttu-id="c7d5f-133">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-133">The previous key state.</span></span> <span data-ttu-id="c7d5f-134">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c7d5f-135">31</span><span class="sxs-lookup"><span data-stu-id="c7d5f-135">31</span></span>    | <span data-ttu-id="c7d5f-136">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-136">The transition state.</span></span> <span data-ttu-id="c7d5f-137">O valor é sempre 0 para uma mensagem do **WM \_ SYSKEYDOWN** .</span><span class="sxs-lookup"><span data-stu-id="c7d5f-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="c7d5f-138">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="c7d5f-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d5f-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7d5f-139">Return value</span></span>

<span data-ttu-id="c7d5f-140">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d5f-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7d5f-141">Remarks</span></span>

<span data-ttu-id="c7d5f-142">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina a chave especificada e gera uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) se a chave for Tab ou Enter.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="c7d5f-143">Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="c7d5f-144">Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="c7d5f-145">Devido à repetição automática, mais de uma mensagem do **WM \_ SYSKEYDOWN** pode ocorrer antes de uma mensagem do [**WM \_ SYSKEYUP**](wm-syskeyup.md) ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="c7d5f-146">O estado de chave anterior (bit 30) pode ser usado para determinar se a mensagem do **WM \_ SYSKEYDOWN** indica a primeira transição para baixo ou uma transição repetida.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="c7d5f-147">Para teclados avançados de 101 e 102 teclas, as chaves avançadas são as teclas ALT e CTRL na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="c7d5f-148">Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c7d5f-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="c7d5f-149">Essa mensagem também é enviada sempre que o usuário pressiona a tecla F10 sem a tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="c7d5f-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d5f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7d5f-150">Requirements</span></span>



| <span data-ttu-id="c7d5f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7d5f-151">Requirement</span></span> | <span data-ttu-id="c7d5f-152">Valor</span><span class="sxs-lookup"><span data-stu-id="c7d5f-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d5f-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d5f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d5f-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7d5f-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7d5f-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d5f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d5f-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7d5f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7d5f-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7d5f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d5f-158"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7d5f-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d5f-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7d5f-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7d5f-160">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7d5f-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c7d5f-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="c7d5f-163">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="c7d5f-164">**SYSKEYUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="c7d5f-165">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c7d5f-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7d5f-166">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="c7d5f-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

