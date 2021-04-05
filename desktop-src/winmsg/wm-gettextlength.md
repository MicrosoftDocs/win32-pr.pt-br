---
description: Determina o comprimento, em caracteres, do texto associado a uma janela.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Mensagem de WM_GETTEXTLENGTH (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922152"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="913c6-103">Mensagem do WM \_ GETTEXTLENGTH</span><span class="sxs-lookup"><span data-stu-id="913c6-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="913c6-104">Determina o comprimento, em caracteres, do texto associado a uma janela.</span><span class="sxs-lookup"><span data-stu-id="913c6-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="913c6-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="913c6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913c6-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="913c6-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="913c6-107">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="913c6-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="913c6-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="913c6-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="913c6-109">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="913c6-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913c6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="913c6-110">Return value</span></span>

<span data-ttu-id="913c6-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="913c6-111">Type: **LRESULT**</span></span>

<span data-ttu-id="913c6-112">O valor de retorno é o comprimento do texto em caracteres, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="913c6-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="913c6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="913c6-113">Remarks</span></span>

<span data-ttu-id="913c6-114">Para um controle de edição, o texto a ser copiado é o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="913c6-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="913c6-115">Para uma caixa de combinação, o texto é o conteúdo da parte do controle de edição (ou texto estático) da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="913c6-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="913c6-116">Para um botão, o texto é o nome do botão.</span><span class="sxs-lookup"><span data-stu-id="913c6-116">For a button, the text is the button name.</span></span> <span data-ttu-id="913c6-117">Para outras janelas, o texto é o título da janela.</span><span class="sxs-lookup"><span data-stu-id="913c6-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="913c6-118">Para determinar o comprimento de um item em uma caixa de listagem, um aplicativo pode usar a mensagem [**\_ GETTEXTLEN de lb**](../controls/lb-gettextlen.md) .</span><span class="sxs-lookup"><span data-stu-id="913c6-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="913c6-119">Quando a **mensagem \_ GETTEXTLENGTH do WM** é enviada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna o comprimento, em caracteres, do texto.</span><span class="sxs-lookup"><span data-stu-id="913c6-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="913c6-120">Em determinadas condições, a função **DefWindowProc** retorna um valor maior que o comprimento real do texto.</span><span class="sxs-lookup"><span data-stu-id="913c6-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="913c6-121">Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto.</span><span class="sxs-lookup"><span data-stu-id="913c6-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="913c6-122">O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você pode usá-lo sempre para orientar a alocação do buffer.</span><span class="sxs-lookup"><span data-stu-id="913c6-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="913c6-123">Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.</span><span class="sxs-lookup"><span data-stu-id="913c6-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="913c6-124">Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)ou [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) ou a função [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="913c6-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="913c6-125">Enviar uma mensagem do **WM \_ GETTEXTLENGTH** para um controle estático de não texto, como um bitmap estático ou um ícone estático ControlC, não retorna um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="913c6-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="913c6-126">Em vez disso, retorna zero.</span><span class="sxs-lookup"><span data-stu-id="913c6-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="913c6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913c6-127">Requirements</span></span>



| <span data-ttu-id="913c6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="913c6-128">Requirement</span></span> | <span data-ttu-id="913c6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="913c6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913c6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="913c6-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="913c6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="913c6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="913c6-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="913c6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="913c6-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="913c6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="913c6-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="913c6-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913c6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="913c6-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="913c6-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="913c6-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="913c6-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="913c6-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="913c6-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="913c6-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="913c6-140">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="913c6-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="913c6-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="913c6-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="913c6-142">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="913c6-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="913c6-143">Windows</span><span class="sxs-lookup"><span data-stu-id="913c6-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="913c6-144">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="913c6-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="913c6-145">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="913c6-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="913c6-146">**LB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="913c6-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="913c6-147">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="913c6-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
