---
title: Mensagem de WM_UNICHAR (WinUser. h)
description: A mensagem do WM \_ UNICHAR pode ser usada por um aplicativo para postar a entrada para outras janelas.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Entrada de mouse e teclado de mensagem WM_UNICHAR
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770552"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="34c55-104">Mensagem do WM \_ UNICHAR</span><span class="sxs-lookup"><span data-stu-id="34c55-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="34c55-105">A mensagem do **WM \_ UNICHAR** pode ser usada por um aplicativo para postar a entrada para outras janelas.</span><span class="sxs-lookup"><span data-stu-id="34c55-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="34c55-106">Essa mensagem contém o código de caractere da chave que foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="34c55-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="34c55-107">(Teste se um aplicativo de destino pode processar mensagens do **WM \_ UNICHAR** enviando a mensagem com *wParam* definido como **Unicode \_ nochar**.)</span><span class="sxs-lookup"><span data-stu-id="34c55-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="34c55-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34c55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c55-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34c55-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34c55-110">O código de caractere da chave.</span><span class="sxs-lookup"><span data-stu-id="34c55-110">The character code of the key.</span></span>

<span data-ttu-id="34c55-111">Se *wParam* for **Unicode \_ nochar** e o aplicativo processar essa mensagem, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="34c55-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="34c55-112">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará **false** (o padrão).</span><span class="sxs-lookup"><span data-stu-id="34c55-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="34c55-113">Se *wParam* não for **Unicode \_ nochar**, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="34c55-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="34c55-114">O Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posta uma mensagem do [**WM \_ Char**](wm-char.md) com os mesmos parâmetros e a função ANSI **DefWindowProc** posta uma ou duas mensagens do **WM \_ Char** com os caracteres ANSI correspondentes.</span><span class="sxs-lookup"><span data-stu-id="34c55-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="34c55-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34c55-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34c55-116">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34c55-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="34c55-117">Bits</span><span class="sxs-lookup"><span data-stu-id="34c55-117">Bits</span></span>  | <span data-ttu-id="34c55-118">Significado</span><span class="sxs-lookup"><span data-stu-id="34c55-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c55-119">0-15</span><span class="sxs-lookup"><span data-stu-id="34c55-119">0-15</span></span>  | <span data-ttu-id="34c55-120">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="34c55-120">The repeat count for the current message.</span></span> <span data-ttu-id="34c55-121">O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave.</span><span class="sxs-lookup"><span data-stu-id="34c55-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="34c55-122">Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="34c55-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="34c55-123">No entanto, a contagem de repetição não é cumulativa.</span><span class="sxs-lookup"><span data-stu-id="34c55-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="34c55-124">16-23</span><span class="sxs-lookup"><span data-stu-id="34c55-124">16-23</span></span> | <span data-ttu-id="34c55-125">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="34c55-125">The scan code.</span></span> <span data-ttu-id="34c55-126">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="34c55-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="34c55-127">24</span><span class="sxs-lookup"><span data-stu-id="34c55-127">24</span></span>    | <span data-ttu-id="34c55-128">Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas.</span><span class="sxs-lookup"><span data-stu-id="34c55-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="34c55-129">O valor será 1 se for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="34c55-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="34c55-130">25-28</span><span class="sxs-lookup"><span data-stu-id="34c55-130">25-28</span></span> | <span data-ttu-id="34c55-131">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="34c55-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="34c55-132">29</span><span class="sxs-lookup"><span data-stu-id="34c55-132">29</span></span>    | <span data-ttu-id="34c55-133">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="34c55-133">The context code.</span></span> <span data-ttu-id="34c55-134">O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla for pressionada; caso contrário, o valor será 0.</span><span class="sxs-lookup"><span data-stu-id="34c55-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="34c55-135">30</span><span class="sxs-lookup"><span data-stu-id="34c55-135">30</span></span>    | <span data-ttu-id="34c55-136">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="34c55-136">The previous key state.</span></span> <span data-ttu-id="34c55-137">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="34c55-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="34c55-138">31</span><span class="sxs-lookup"><span data-stu-id="34c55-138">31</span></span>    | <span data-ttu-id="34c55-139">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="34c55-139">The transition state.</span></span> <span data-ttu-id="34c55-140">O valor será 1 se a chave estiver sendo liberada ou for 0 se a chave estiver sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="34c55-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="34c55-141">Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="34c55-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34c55-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34c55-142">Return value</span></span>

<span data-ttu-id="34c55-143">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="34c55-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="34c55-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="34c55-144">Remarks</span></span>

<span data-ttu-id="34c55-145">A mensagem do **WM \_ UNICHAR** é semelhante ao [**WM \_ Char**](wm-char.md), mas usa o formato UTF (Unicode transformation Format)-32, enquanto o **WM \_ Char** usa UTF-16.</span><span class="sxs-lookup"><span data-stu-id="34c55-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="34c55-146">Essa mensagem foi criada para enviar ou postar caracteres Unicode para janelas ANSI e pode manipular caracteres de plano suplementar Unicode.</span><span class="sxs-lookup"><span data-stu-id="34c55-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="34c55-147">Como não há necessariamente uma correspondência de um para um entre as chaves pressionadas e as mensagens de caracteres geradas, as informações na palavra de ordem superior do parâmetro *lParam* geralmente não são úteis para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="34c55-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="34c55-148">As informações na palavra de ordem superior aplicam-se apenas à mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede o lançamento da mensagem do **WM \_ UNICHAR** .</span><span class="sxs-lookup"><span data-stu-id="34c55-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="34c55-149">Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT direita e direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="34c55-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="34c55-150">Alguns teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="34c55-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="34c55-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34c55-151">Requirements</span></span>



| <span data-ttu-id="34c55-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="34c55-152">Requirement</span></span> | <span data-ttu-id="34c55-153">Valor</span><span class="sxs-lookup"><span data-stu-id="34c55-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c55-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34c55-154">Minimum supported client</span></span><br/> | <span data-ttu-id="34c55-155">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34c55-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34c55-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34c55-156">Minimum supported server</span></span><br/> | <span data-ttu-id="34c55-157">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34c55-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34c55-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34c55-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="34c55-159"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34c55-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c55-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="34c55-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="34c55-161">**Referência**</span><span class="sxs-lookup"><span data-stu-id="34c55-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34c55-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="34c55-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="34c55-163">**caractere do WM \_**</span><span class="sxs-lookup"><span data-stu-id="34c55-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="34c55-164">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="34c55-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="34c55-165">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="34c55-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="34c55-166">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="34c55-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

