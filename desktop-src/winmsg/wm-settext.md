---
description: Define o texto de uma janela.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Mensagem de WM_SETTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663153"
---
# <a name="wm_settext-message"></a><span data-ttu-id="435bc-103">\_Mensagem de SETtext do WM</span><span class="sxs-lookup"><span data-stu-id="435bc-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="435bc-104">Define o texto de uma janela.</span><span class="sxs-lookup"><span data-stu-id="435bc-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="435bc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="435bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435bc-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="435bc-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="435bc-107">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="435bc-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="435bc-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="435bc-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="435bc-109">Um ponteiro para uma cadeia de caracteres terminada em nulo que é o texto da janela.</span><span class="sxs-lookup"><span data-stu-id="435bc-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435bc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="435bc-110">Return value</span></span>

<span data-ttu-id="435bc-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="435bc-111">Type: **LRESULT**</span></span>

<span data-ttu-id="435bc-112">O valor de retorno será **true** se o texto estiver definido.</span><span class="sxs-lookup"><span data-stu-id="435bc-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="435bc-113">É **false** (para um controle de edição), **lb \_ ERRSPACE** (para uma caixa de listagem) ou **CB \_ ERRSPACE** (para uma caixa de combinação) se houver espaço insuficiente disponível para definir o texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="435bc-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="435bc-114">Será **CB \_ Err** se essa mensagem for enviada para uma caixa de combinação sem um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="435bc-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="435bc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="435bc-115">Remarks</span></span>

<span data-ttu-id="435bc-116">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) define e exibe o texto da janela.</span><span class="sxs-lookup"><span data-stu-id="435bc-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="435bc-117">Para um controle de edição, o texto é o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="435bc-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="435bc-118">Para uma caixa de combinação, o texto é o conteúdo da parte de controle de edição da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="435bc-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="435bc-119">Para um botão, o texto é o nome do botão.</span><span class="sxs-lookup"><span data-stu-id="435bc-119">For a button, the text is the button name.</span></span> <span data-ttu-id="435bc-120">Para outras janelas, o texto é o título da janela.</span><span class="sxs-lookup"><span data-stu-id="435bc-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="435bc-121">Esta mensagem não altera a seleção atual na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="435bc-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="435bc-122">Um aplicativo deve usar a [**mensagem \_ SelectString do CB**](../controls/cb-selectstring.md) para selecionar o item em uma caixa de listagem que corresponda ao texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="435bc-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="435bc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="435bc-123">Requirements</span></span>



| <span data-ttu-id="435bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="435bc-124">Requirement</span></span> | <span data-ttu-id="435bc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="435bc-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="435bc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="435bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="435bc-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="435bc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="435bc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="435bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="435bc-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="435bc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="435bc-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="435bc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="435bc-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="435bc-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435bc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="435bc-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="435bc-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="435bc-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="435bc-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="435bc-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="435bc-135">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="435bc-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="435bc-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="435bc-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="435bc-137">Windows</span><span class="sxs-lookup"><span data-stu-id="435bc-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="435bc-138">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="435bc-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="435bc-139">**seleção do CB \_**</span><span class="sxs-lookup"><span data-stu-id="435bc-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
