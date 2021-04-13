---
title: Mensagem de WM_SYSCHAR (WinUser. h)
description: Postado na janela com o foco do teclado quando uma \_ mensagem do WM SYSKEYDOWN é convertida pela função TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499835"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="57225-104">Mensagem do WM \_ SYSCHAR</span><span class="sxs-lookup"><span data-stu-id="57225-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="57225-105">Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="57225-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="57225-106">Especifica o código de caractere de uma chave de caractere do sistema que é uma tecla de caractere que é pressionada enquanto a tecla ALT está inativa.</span><span class="sxs-lookup"><span data-stu-id="57225-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="57225-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57225-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57225-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57225-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57225-109">O código de caractere da tecla de menu da janela.</span><span class="sxs-lookup"><span data-stu-id="57225-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="57225-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57225-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57225-111">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57225-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="57225-112">Bits</span><span class="sxs-lookup"><span data-stu-id="57225-112">Bits</span></span>                                                                             | <span data-ttu-id="57225-113">Significado</span><span class="sxs-lookup"><span data-stu-id="57225-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57225-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="57225-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="57225-115">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="57225-115">The repeat count for the current message.</span></span> <span data-ttu-id="57225-116">O valor é o número de vezes que o pressionamento de tecla foi repetido automaticamente como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="57225-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="57225-117">Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="57225-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="57225-118">No entanto, a contagem de repetição não é cumulativa.</span><span class="sxs-lookup"><span data-stu-id="57225-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="57225-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="57225-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="57225-120">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="57225-120">The scan code.</span></span> <span data-ttu-id="57225-121">O valor depende do OEM (fabricante original do equipamento).</span><span class="sxs-lookup"><span data-stu-id="57225-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="57225-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="57225-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="57225-123">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="57225-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="57225-124">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="57225-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="57225-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="57225-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="57225-126">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="57225-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="57225-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="57225-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="57225-128">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="57225-128">The context code.</span></span> <span data-ttu-id="57225-129">O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla for pressionada; caso contrário, o valor será 0.</span><span class="sxs-lookup"><span data-stu-id="57225-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="57225-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="57225-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="57225-131">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="57225-131">The previous key state.</span></span> <span data-ttu-id="57225-132">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="57225-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="57225-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="57225-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="57225-134">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="57225-134">The transition state.</span></span> <span data-ttu-id="57225-135">O valor será 1 se a chave estiver sendo liberada ou for 0 se a chave estiver sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="57225-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="57225-136">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="57225-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57225-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57225-137">Return value</span></span>

<span data-ttu-id="57225-138">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="57225-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="57225-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="57225-139">Remarks</span></span>

<span data-ttu-id="57225-140">Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave padrão em vez de uma mensagem de chave de caractere do sistema.</span><span class="sxs-lookup"><span data-stu-id="57225-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="57225-141">Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="57225-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="57225-142">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; a chave de SCRN de impressão; a chave de interrupção; a tecla NUMLOCK; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="57225-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="57225-143">Outros teclados podem dar suporte ao bit de chave estendida no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="57225-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="57225-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57225-144">Requirements</span></span>



| <span data-ttu-id="57225-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="57225-145">Requirement</span></span> | <span data-ttu-id="57225-146">Valor</span><span class="sxs-lookup"><span data-stu-id="57225-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57225-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57225-147">Minimum supported client</span></span><br/> | <span data-ttu-id="57225-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57225-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57225-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57225-149">Minimum supported server</span></span><br/> | <span data-ttu-id="57225-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57225-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57225-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="57225-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="57225-152"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57225-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57225-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="57225-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="57225-154">**Referência**</span><span class="sxs-lookup"><span data-stu-id="57225-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57225-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="57225-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="57225-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="57225-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="57225-157">**SYSKEYDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="57225-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="57225-158">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="57225-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57225-159">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="57225-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

