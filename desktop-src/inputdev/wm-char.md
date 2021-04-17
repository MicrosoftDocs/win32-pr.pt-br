---
title: Mensagem de WM_CHAR (WinUser. h)
description: Postado na janela com o foco do teclado quando uma \_ mensagem do WM KEYDOWN é convertida pela função TranslateMessage. A mensagem do WM \_ Char contém o código de caractere da chave que foi pressionada.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Entrada de mouse e teclado de mensagem WM_CHAR
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785298"
---
# <a name="wm_char-message"></a><span data-ttu-id="5b31b-105">Mensagem do WM \_ Char</span><span class="sxs-lookup"><span data-stu-id="5b31b-105">WM\_CHAR message</span></span>

<span data-ttu-id="5b31b-106">Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="5b31b-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="5b31b-107">A mensagem do **WM \_ Char** contém o código de caractere da chave que foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="5b31b-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="5b31b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b31b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b31b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b31b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b31b-110">O código de caractere da chave.</span><span class="sxs-lookup"><span data-stu-id="5b31b-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="5b31b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b31b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b31b-112">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b31b-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="5b31b-113">Bits</span><span class="sxs-lookup"><span data-stu-id="5b31b-113">Bits</span></span>  | <span data-ttu-id="5b31b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5b31b-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b31b-115">0-15</span><span class="sxs-lookup"><span data-stu-id="5b31b-115">0-15</span></span>  | <span data-ttu-id="5b31b-116">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="5b31b-116">The repeat count for the current message.</span></span> <span data-ttu-id="5b31b-117">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="5b31b-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="5b31b-118">Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="5b31b-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="5b31b-119">No entanto, a contagem de repetição não é cumulativa.</span><span class="sxs-lookup"><span data-stu-id="5b31b-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="5b31b-120">16-23</span><span class="sxs-lookup"><span data-stu-id="5b31b-120">16-23</span></span> | <span data-ttu-id="5b31b-121">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="5b31b-121">The scan code.</span></span> <span data-ttu-id="5b31b-122">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="5b31b-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="5b31b-123">24</span><span class="sxs-lookup"><span data-stu-id="5b31b-123">24</span></span>    | <span data-ttu-id="5b31b-124">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="5b31b-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="5b31b-125">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="5b31b-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="5b31b-126">25-28</span><span class="sxs-lookup"><span data-stu-id="5b31b-126">25-28</span></span> | <span data-ttu-id="5b31b-127">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="5b31b-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5b31b-128">29</span><span class="sxs-lookup"><span data-stu-id="5b31b-128">29</span></span>    | <span data-ttu-id="5b31b-129">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="5b31b-129">The context code.</span></span> <span data-ttu-id="5b31b-130">O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla for pressionada; caso contrário, o valor será 0.</span><span class="sxs-lookup"><span data-stu-id="5b31b-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="5b31b-131">30</span><span class="sxs-lookup"><span data-stu-id="5b31b-131">30</span></span>    | <span data-ttu-id="5b31b-132">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="5b31b-132">The previous key state.</span></span> <span data-ttu-id="5b31b-133">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="5b31b-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="5b31b-134">31</span><span class="sxs-lookup"><span data-stu-id="5b31b-134">31</span></span>    | <span data-ttu-id="5b31b-135">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="5b31b-135">The transition state.</span></span> <span data-ttu-id="5b31b-136">O valor será 1 se a chave estiver sendo liberada ou for 0 se a chave estiver sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="5b31b-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="5b31b-137">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="5b31b-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b31b-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b31b-138">Return value</span></span>

<span data-ttu-id="5b31b-139">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b31b-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="5b31b-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5b31b-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="5b31b-141">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="5b31b-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b31b-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b31b-142">Remarks</span></span>

<span data-ttu-id="5b31b-143">A mensagem do **WM \_ Char** usa o formato UTF (Unicode Transformation Format)-16.</span><span class="sxs-lookup"><span data-stu-id="5b31b-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="5b31b-144">Não há necessariamente uma correspondência de um para um entre as chaves pressionadas e as mensagens de caracteres geradas e, portanto, as informações na palavra de ordem superior do parâmetro *lParam* geralmente não são úteis para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5b31b-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="5b31b-145">As informações na palavra de ordem superior aplicam-se apenas à mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede o lançamento da mensagem do **WM \_ Char** .</span><span class="sxs-lookup"><span data-stu-id="5b31b-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="5b31b-146">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT direita e direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="5b31b-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="5b31b-147">Alguns teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5b31b-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="5b31b-148">A mensagem do [**WM \_ UNICHAR**](wm-unichar.md) é igual à do **WM \_ Char**, exceto pelo uso de UTF-32.</span><span class="sxs-lookup"><span data-stu-id="5b31b-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="5b31b-149">Ele foi projetado para enviar ou postar caracteres Unicode para janelas ANSI e pode manipular caracteres de plano suplementar Unicode.</span><span class="sxs-lookup"><span data-stu-id="5b31b-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b31b-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b31b-150">Requirements</span></span>



| <span data-ttu-id="5b31b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b31b-151">Requirement</span></span> | <span data-ttu-id="5b31b-152">Valor</span><span class="sxs-lookup"><span data-stu-id="5b31b-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b31b-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b31b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5b31b-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b31b-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b31b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5b31b-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b31b-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b31b-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b31b-158"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b31b-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b31b-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b31b-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b31b-160">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5b31b-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b31b-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="5b31b-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="5b31b-162">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="5b31b-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="5b31b-163">**UNICHAR do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5b31b-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="5b31b-164">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5b31b-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b31b-165">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="5b31b-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

