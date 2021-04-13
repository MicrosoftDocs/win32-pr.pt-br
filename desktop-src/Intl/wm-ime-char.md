---
description: Enviado a um aplicativo quando o IME Obtém um caractere do resultado da conversão. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Mensagem de WM_IME_CHAR (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370779"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="c81c6-104">Mensagem de caracteres do \_ IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="c81c6-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="c81c6-105">Enviado a um aplicativo quando o IME Obtém um caractere do resultado da conversão.</span><span class="sxs-lookup"><span data-stu-id="c81c6-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="c81c6-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c81c6-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="c81c6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c81c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81c6-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c81c6-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c81c6-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="c81c6-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="c81c6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c81c6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c81c6-111">**DBCS:** Um valor de caractere de byte único ou de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="c81c6-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="c81c6-112">Para um caractere de byte duplo, (BYTE) (wParam >> 8) contém o byte de Lead.</span><span class="sxs-lookup"><span data-stu-id="c81c6-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="c81c6-113">Observe que os parênteses são necessários porque o operador cast tem precedência mais alta do que o operador shift.</span><span class="sxs-lookup"><span data-stu-id="c81c6-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="c81c6-114">**Unicode:** Um valor de caractere Unicode.</span><span class="sxs-lookup"><span data-stu-id="c81c6-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="c81c6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c81c6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c81c6-116">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, com valores definidos abaixo.</span><span class="sxs-lookup"><span data-stu-id="c81c6-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="c81c6-117">bit</span><span class="sxs-lookup"><span data-stu-id="c81c6-117">Bit</span></span>   | <span data-ttu-id="c81c6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c81c6-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c81c6-119">0-15</span><span class="sxs-lookup"><span data-stu-id="c81c6-119">0-15</span></span>  | <span data-ttu-id="c81c6-120">Contagem de repetições.</span><span class="sxs-lookup"><span data-stu-id="c81c6-120">Repeat count.</span></span> <span data-ttu-id="c81c6-121">Como o primeiro byte e o segundo byte são contínuos, isso é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="c81c6-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="c81c6-122">16-23</span><span class="sxs-lookup"><span data-stu-id="c81c6-122">16-23</span></span> | <span data-ttu-id="c81c6-123">Código de verificação de um caractere asiático completo.</span><span class="sxs-lookup"><span data-stu-id="c81c6-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="c81c6-124">24</span><span class="sxs-lookup"><span data-stu-id="c81c6-124">24</span></span>    | <span data-ttu-id="c81c6-125">Chave estendida.</span><span class="sxs-lookup"><span data-stu-id="c81c6-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="c81c6-126">25-28</span><span class="sxs-lookup"><span data-stu-id="c81c6-126">25-28</span></span> | <span data-ttu-id="c81c6-127">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c81c6-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="c81c6-128">29</span><span class="sxs-lookup"><span data-stu-id="c81c6-128">29</span></span>    | <span data-ttu-id="c81c6-129">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="c81c6-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="c81c6-130">30</span><span class="sxs-lookup"><span data-stu-id="c81c6-130">30</span></span>    | <span data-ttu-id="c81c6-131">Estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="c81c6-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="c81c6-132">31</span><span class="sxs-lookup"><span data-stu-id="c81c6-132">31</span></span>    | <span data-ttu-id="c81c6-133">Estado de transição.</span><span class="sxs-lookup"><span data-stu-id="c81c6-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c81c6-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="c81c6-134">Remarks</span></span>

<span data-ttu-id="c81c6-135">Ao contrário da mensagem do [**WM \_ Char**](../inputdev/wm-char.md) para uma janela não-Unicode, essa mensagem pode incluir valores de caractere de byte duplo e de byte único.</span><span class="sxs-lookup"><span data-stu-id="c81c6-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="c81c6-136">Para uma janela Unicode, essa mensagem é igual ao WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="c81c6-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="c81c6-137">Para uma janela não-Unicode, se a \_ mensagem de caractere IME do WM \_ incluir um caractere de byte duplo e o aplicativo passar essa mensagem para [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o IME converterá essa mensagem em duas \_ mensagens do WM Char, cada uma contendo um byte do caractere de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="c81c6-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81c6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c81c6-138">Requirements</span></span>



| <span data-ttu-id="c81c6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81c6-139">Requirement</span></span> | <span data-ttu-id="c81c6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c81c6-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c81c6-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c81c6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c81c6-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c81c6-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c81c6-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c81c6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c81c6-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c81c6-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c81c6-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c81c6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c81c6-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c81c6-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81c6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c81c6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81c6-148">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c81c6-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c81c6-149">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c81c6-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
