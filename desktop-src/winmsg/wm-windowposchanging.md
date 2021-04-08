---
description: Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z está prestes a ser alterado como resultado de uma chamada para a função SetWindowPos ou outra função de gerenciamento de janela.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Mensagem de WM_WINDOWPOSCHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662809"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="6b0fd-103">Mensagem do WM \_ WINDOWPOSCHANGING</span><span class="sxs-lookup"><span data-stu-id="6b0fd-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="6b0fd-104">Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z está prestes a ser alterado como resultado de uma chamada para a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou outra função de gerenciamento de janela.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="6b0fd-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b0fd-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="6b0fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b0fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b0fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0fd-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b0fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b0fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0fd-110">Um ponteiro para uma estrutura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que contém informações sobre o novo tamanho e a posição da janela.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0fd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b0fd-111">Return value</span></span>

<span data-ttu-id="6b0fd-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-112">Type: **LRESULT**</span></span>

<span data-ttu-id="6b0fd-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0fd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b0fd-114">Remarks</span></span>

<span data-ttu-id="6b0fd-115">Para uma janela com o [**estilo \_ WS Overlapped**](window-styles.md) ou **WS \_ THICKFRAME** , a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia a mensagem [**\_ GETMINMAXINFO do WM**](wm-getminmaxinfo.md) para a janela.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="6b0fd-116">Isso é feito para validar o novo tamanho e a posição da janela e para impor os estilos de cliente [cs \_ BYTEALIGNCLIENT](about-window-classes.md) e cs \_ BYTEALIGNWINDOW.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="6b0fd-117">Ao não passar a mensagem do **WM \_ WINDOWPOSCHANGING** para a função **DefWindowProc** , um aplicativo pode substituir esses padrões.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="6b0fd-118">Enquanto essa mensagem está sendo processada, modificar qualquer um dos valores em [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) afeta o novo tamanho, a posição ou o local da janela na ordem Z.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="6b0fd-119">Um aplicativo pode impedir alterações na janela definindo ou limpando os bits apropriados no membro **flags** de **WINDOWPOS**.</span><span class="sxs-lookup"><span data-stu-id="6b0fd-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0fd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b0fd-120">Requirements</span></span>



| <span data-ttu-id="6b0fd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0fd-121">Requirement</span></span> | <span data-ttu-id="6b0fd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6b0fd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0fd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b0fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0fd-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b0fd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6b0fd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b0fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0fd-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b0fd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b0fd-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6b0fd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b0fd-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fd-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0fd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b0fd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b0fd-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b0fd-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6b0fd-132">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="6b0fd-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="6b0fd-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="6b0fd-135">**GETMINMAXINFO do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="6b0fd-136">**movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="6b0fd-137">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="6b0fd-138">**WINDOWPOSCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="6b0fd-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6b0fd-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b0fd-140">Windows</span><span class="sxs-lookup"><span data-stu-id="6b0fd-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
