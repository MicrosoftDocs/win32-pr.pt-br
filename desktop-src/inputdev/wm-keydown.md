---
title: Mensagem de WM_KEYDOWN (WinUser. h)
description: Postado na janela com o foco do teclado quando uma tecla que não é do sistema é pressionada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Entrada de mouse e teclado de mensagem WM_KEYDOWN
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797605"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="dc423-105">Mensagem de KEYDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="dc423-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="dc423-106">Postado na janela com o foco do teclado quando uma tecla que não é do sistema é pressionada.</span><span class="sxs-lookup"><span data-stu-id="dc423-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="dc423-107">Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada.</span><span class="sxs-lookup"><span data-stu-id="dc423-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="dc423-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc423-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc423-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc423-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc423-110">O código de chave virtual da chave que não é do sistema.</span><span class="sxs-lookup"><span data-stu-id="dc423-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="dc423-111">Consulte [códigos de chave virtual](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dc423-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc423-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc423-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc423-113">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc423-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="dc423-114">Bits</span><span class="sxs-lookup"><span data-stu-id="dc423-114">Bits</span></span>  | <span data-ttu-id="dc423-115">Significado</span><span class="sxs-lookup"><span data-stu-id="dc423-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc423-116">0-15</span><span class="sxs-lookup"><span data-stu-id="dc423-116">0-15</span></span>  | <span data-ttu-id="dc423-117">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="dc423-117">The repeat count for the current message.</span></span> <span data-ttu-id="dc423-118">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="dc423-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="dc423-119">Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="dc423-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="dc423-120">No entanto, a contagem de repetição não é cumulativa.</span><span class="sxs-lookup"><span data-stu-id="dc423-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="dc423-121">16-23</span><span class="sxs-lookup"><span data-stu-id="dc423-121">16-23</span></span> | <span data-ttu-id="dc423-122">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="dc423-122">The scan code.</span></span> <span data-ttu-id="dc423-123">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="dc423-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="dc423-124">24</span><span class="sxs-lookup"><span data-stu-id="dc423-124">24</span></span>    | <span data-ttu-id="dc423-125">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="dc423-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="dc423-126">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="dc423-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="dc423-127">25-28</span><span class="sxs-lookup"><span data-stu-id="dc423-127">25-28</span></span> | <span data-ttu-id="dc423-128">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="dc423-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="dc423-129">29</span><span class="sxs-lookup"><span data-stu-id="dc423-129">29</span></span>    | <span data-ttu-id="dc423-130">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="dc423-130">The context code.</span></span> <span data-ttu-id="dc423-131">O valor é sempre 0 para uma mensagem do **WM \_ KEYDOWN** .</span><span class="sxs-lookup"><span data-stu-id="dc423-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="dc423-132">30</span><span class="sxs-lookup"><span data-stu-id="dc423-132">30</span></span>    | <span data-ttu-id="dc423-133">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="dc423-133">The previous key state.</span></span> <span data-ttu-id="dc423-134">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for zero se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="dc423-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="dc423-135">31</span><span class="sxs-lookup"><span data-stu-id="dc423-135">31</span></span>    | <span data-ttu-id="dc423-136">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="dc423-136">The transition state.</span></span> <span data-ttu-id="dc423-137">O valor é sempre 0 para uma mensagem do **WM \_ KEYDOWN** .</span><span class="sxs-lookup"><span data-stu-id="dc423-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="dc423-138">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="dc423-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc423-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc423-139">Return value</span></span>

<span data-ttu-id="dc423-140">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="dc423-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="dc423-141">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dc423-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="dc423-142">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="dc423-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="dc423-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc423-143">Remarks</span></span>

<span data-ttu-id="dc423-144">Se a tecla F10 for pressionada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) definirá um sinalizador interno.</span><span class="sxs-lookup"><span data-stu-id="dc423-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="dc423-145">Quando **DefWindowProc** recebe a mensagem do [**WM \_ KEYUP**](wm-keyup.md) , a função verifica se o sinalizador interno está definido e, nesse caso, envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="dc423-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="dc423-146">O parâmetro **WM \_ SYSCOMMAND** da mensagem é definido como SC \_ keymenu.</span><span class="sxs-lookup"><span data-stu-id="dc423-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="dc423-147">Devido ao recurso AutoRepetir, mais de uma mensagem do **WM \_ KEYDOWN** pode ser postada antes que uma mensagem do [**WM \_ KEYUP**](wm-keyup.md) seja postada.</span><span class="sxs-lookup"><span data-stu-id="dc423-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="dc423-148">O estado de chave anterior (bit 30) pode ser usado para determinar se a mensagem do **WM \_ KEYDOWN** indica a primeira transição para baixo ou uma transição repetida.</span><span class="sxs-lookup"><span data-stu-id="dc423-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="dc423-149">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="dc423-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="dc423-150">Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="dc423-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="dc423-151">Os aplicativos devem passar *wParam* para [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sem alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="dc423-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc423-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc423-152">Requirements</span></span>



| <span data-ttu-id="dc423-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc423-153">Requirement</span></span> | <span data-ttu-id="dc423-154">Valor</span><span class="sxs-lookup"><span data-stu-id="dc423-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc423-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc423-155">Minimum supported client</span></span><br/> | <span data-ttu-id="dc423-156">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc423-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc423-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc423-157">Minimum supported server</span></span><br/> | <span data-ttu-id="dc423-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc423-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc423-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc423-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc423-160"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc423-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc423-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc423-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc423-162">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dc423-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc423-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dc423-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dc423-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="dc423-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="dc423-165">**caractere do WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc423-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="dc423-166">**o WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="dc423-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="dc423-167">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc423-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="dc423-168">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="dc423-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc423-169">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="dc423-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

