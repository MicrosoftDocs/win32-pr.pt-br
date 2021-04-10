---
description: Enviado quando o plano de fundo da janela deve ser apagado (por exemplo, quando uma janela é redimensionada). A mensagem é enviada para preparar uma parte invalidada de uma janela para pintura.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Mensagem de WM_ERASEBKGND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170447"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="328f6-104">Mensagem do WM \_ ERASEBKGND</span><span class="sxs-lookup"><span data-stu-id="328f6-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="328f6-105">Enviado quando o plano de fundo da janela deve ser apagado (por exemplo, quando uma janela é redimensionada).</span><span class="sxs-lookup"><span data-stu-id="328f6-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="328f6-106">A mensagem é enviada para preparar uma parte invalidada de uma janela para pintura.</span><span class="sxs-lookup"><span data-stu-id="328f6-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="328f6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="328f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328f6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="328f6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="328f6-109">Um identificador para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="328f6-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="328f6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="328f6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="328f6-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="328f6-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="328f6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="328f6-112">Return value</span></span>

<span data-ttu-id="328f6-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="328f6-113">Type: **LRESULT**</span></span>

<span data-ttu-id="328f6-114">Um aplicativo deve retornar diferente de zero se apagar o plano de fundo; caso contrário, ele deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="328f6-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="328f6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="328f6-115">Remarks</span></span>

<span data-ttu-id="328f6-116">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) apaga o plano de fundo usando o pincel de plano de fundo de classe especificado pelo membro **HbrBackground** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) .</span><span class="sxs-lookup"><span data-stu-id="328f6-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="328f6-117">Se **hbrBackground** for **nulo**, o aplicativo deverá processar a mensagem do **WM \_ ERASEBKGND** e apagar o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="328f6-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="328f6-118">Um aplicativo deve retornar diferente de zero em resposta ao **WM \_ ERASEBKGND** se ele processar a mensagem e apagar o plano de fundo; isso indica que não é necessário apagar mais.</span><span class="sxs-lookup"><span data-stu-id="328f6-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="328f6-119">Se o aplicativo retornar zero, a janela permanecerá marcada para apagamento.</span><span class="sxs-lookup"><span data-stu-id="328f6-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="328f6-120">(Normalmente, isso indica que o membro **fErase** da estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) será **true**.)</span><span class="sxs-lookup"><span data-stu-id="328f6-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="328f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="328f6-121">Requirements</span></span>



| <span data-ttu-id="328f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="328f6-122">Requirement</span></span> | <span data-ttu-id="328f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="328f6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="328f6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="328f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="328f6-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="328f6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="328f6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="328f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="328f6-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="328f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="328f6-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="328f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="328f6-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="328f6-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328f6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="328f6-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="328f6-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="328f6-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="328f6-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="328f6-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="328f6-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="328f6-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="328f6-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="328f6-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="328f6-135">Ícones</span><span class="sxs-lookup"><span data-stu-id="328f6-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="328f6-136">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="328f6-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="328f6-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="328f6-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="328f6-138">**PAINTSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="328f6-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
