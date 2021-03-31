---
title: Mensagem de WM_KEYUP (WinUser. h)
description: Postado na janela com o foco do teclado quando uma tecla que não é do sistema é liberada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada ou uma tecla do teclado pressionada quando uma janela tem o foco do teclado.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Entrada de mouse e teclado de mensagem WM_KEYUP
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369496"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="cd53c-105">Mensagem do WM \_ KEYUP</span><span class="sxs-lookup"><span data-stu-id="cd53c-105">WM\_KEYUP message</span></span>

<span data-ttu-id="cd53c-106">Postado na janela com o foco do teclado quando uma tecla que não é do sistema é liberada.</span><span class="sxs-lookup"><span data-stu-id="cd53c-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="cd53c-107">Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT *não* é pressionada ou uma tecla do teclado pressionada quando uma janela tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="cd53c-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="cd53c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd53c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd53c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd53c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd53c-110">O código de chave virtual da chave que não é do sistema.</span><span class="sxs-lookup"><span data-stu-id="cd53c-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="cd53c-111">Consulte [códigos de chave virtual](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cd53c-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd53c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd53c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd53c-113">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd53c-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="cd53c-114">Bits</span><span class="sxs-lookup"><span data-stu-id="cd53c-114">Bits</span></span>  | <span data-ttu-id="cd53c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="cd53c-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd53c-116">0-15</span><span class="sxs-lookup"><span data-stu-id="cd53c-116">0-15</span></span>  | <span data-ttu-id="cd53c-117">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="cd53c-117">The repeat count for the current message.</span></span> <span data-ttu-id="cd53c-118">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="cd53c-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="cd53c-119">A contagem de repetição é sempre 1 para uma mensagem do **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="cd53c-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="cd53c-120">16-23</span><span class="sxs-lookup"><span data-stu-id="cd53c-120">16-23</span></span> | <span data-ttu-id="cd53c-121">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="cd53c-121">The scan code.</span></span> <span data-ttu-id="cd53c-122">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="cd53c-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="cd53c-123">24</span><span class="sxs-lookup"><span data-stu-id="cd53c-123">24</span></span>    | <span data-ttu-id="cd53c-124">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="cd53c-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="cd53c-125">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="cd53c-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="cd53c-126">25-28</span><span class="sxs-lookup"><span data-stu-id="cd53c-126">25-28</span></span> | <span data-ttu-id="cd53c-127">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="cd53c-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="cd53c-128">29</span><span class="sxs-lookup"><span data-stu-id="cd53c-128">29</span></span>    | <span data-ttu-id="cd53c-129">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="cd53c-129">The context code.</span></span> <span data-ttu-id="cd53c-130">O valor é sempre 0 para uma mensagem do **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="cd53c-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="cd53c-131">30</span><span class="sxs-lookup"><span data-stu-id="cd53c-131">30</span></span>    | <span data-ttu-id="cd53c-132">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="cd53c-132">The previous key state.</span></span> <span data-ttu-id="cd53c-133">O valor é sempre 1 para uma mensagem do **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="cd53c-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="cd53c-134">31</span><span class="sxs-lookup"><span data-stu-id="cd53c-134">31</span></span>    | <span data-ttu-id="cd53c-135">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="cd53c-135">The transition state.</span></span> <span data-ttu-id="cd53c-136">O valor é sempre 1 para uma mensagem do **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="cd53c-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="cd53c-137">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="cd53c-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd53c-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd53c-138">Return value</span></span>

<span data-ttu-id="cd53c-139">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd53c-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd53c-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd53c-140">Remarks</span></span>

<span data-ttu-id="cd53c-141">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior se a tecla F10 ou a tecla Alt foi liberada.</span><span class="sxs-lookup"><span data-stu-id="cd53c-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="cd53c-142">O parâmetro *wParam* da mensagem é definido como SC \_ keymenu.</span><span class="sxs-lookup"><span data-stu-id="cd53c-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="cd53c-143">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="cd53c-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="cd53c-144">Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cd53c-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="cd53c-145">Os aplicativos devem passar *wParam* para [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sem alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="cd53c-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd53c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd53c-146">Requirements</span></span>



| <span data-ttu-id="cd53c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd53c-147">Requirement</span></span> | <span data-ttu-id="cd53c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="cd53c-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd53c-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd53c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="cd53c-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd53c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cd53c-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd53c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="cd53c-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd53c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd53c-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cd53c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd53c-154"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd53c-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd53c-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cd53c-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd53c-156">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cd53c-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd53c-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cd53c-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cd53c-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="cd53c-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="cd53c-159">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="cd53c-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="cd53c-160">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd53c-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="cd53c-161">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cd53c-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cd53c-162">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="cd53c-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

