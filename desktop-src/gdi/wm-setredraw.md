---
description: Um aplicativo envia a \_ mensagem de redesenho do WM para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensagem de WM_SETREDRAW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170527"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="d64d9-103">Mensagem de reemissão do WM \_</span><span class="sxs-lookup"><span data-stu-id="d64d9-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="d64d9-104">Um aplicativo envia a mensagem de **\_ redesenho do WM** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.</span><span class="sxs-lookup"><span data-stu-id="d64d9-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="d64d9-105">Para enviar essa mensagem, chame a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d64d9-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="d64d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d64d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d64d9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d64d9-108">O estado de redesenho.</span><span class="sxs-lookup"><span data-stu-id="d64d9-108">The redraw state.</span></span> <span data-ttu-id="d64d9-109">Se esse parâmetro for **true**, o conteúdo poderá ser redesenhado após uma alteração.</span><span class="sxs-lookup"><span data-stu-id="d64d9-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="d64d9-110">Se esse parâmetro for **false**, o conteúdo não poderá ser redesenhado após uma alteração.</span><span class="sxs-lookup"><span data-stu-id="d64d9-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="d64d9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d64d9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d64d9-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d64d9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64d9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d64d9-113">Return value</span></span>

<span data-ttu-id="d64d9-114">Um aplicativo retornará zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="d64d9-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d64d9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d64d9-115">Remarks</span></span>

<span data-ttu-id="d64d9-116">Essa mensagem poderá ser útil se um aplicativo precisar adicionar vários itens a uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d64d9-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="d64d9-117">O aplicativo pode chamar essa mensagem com *wParam* definido como **false**, adicionar os itens e, em seguida, chamar a mensagem novamente com *wParam* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="d64d9-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="d64d9-118">Por fim, o aplicativo pode chamar [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **NULL**, **NULL**, RDW \_ apagar \| RDW \_ quadro \| RDW \_ invalidar \| RDW \_ filhos) para fazer com que a caixa de listagem seja repintada.</span><span class="sxs-lookup"><span data-stu-id="d64d9-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="d64d9-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com os sinalizadores especificados é usado em vez de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) porque o primeiro é necessário para alguns controles que têm uma área não cliente por conta própria ou que têm estilos de janela que fazem com que eles recebam uma área que não seja de cliente (como **WS \_ THICKFRAME**, **WS \_ Border** ou **WS \_ ex \_ CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="d64d9-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="d64d9-120">Se o controle não tiver uma área que não seja cliente, **RedrawWindow** com esses sinalizadores fará apenas a invalidação que o **InvalidateRect** faria.</span><span class="sxs-lookup"><span data-stu-id="d64d9-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="d64d9-121">Se o aplicativo enviar a mensagem de **\_ reemissão do WM** para uma janela oculta, a janela ficará visível (ou seja, o sistema operacional adicionará o estilo **WS \_ visível** à janela).</span><span class="sxs-lookup"><span data-stu-id="d64d9-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="d64d9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64d9-122">Requirements</span></span>



| <span data-ttu-id="d64d9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64d9-123">Requirement</span></span> | <span data-ttu-id="d64d9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d64d9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64d9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d64d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d64d9-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d64d9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d64d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d64d9-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d64d9-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d64d9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d64d9-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d64d9-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64d9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d64d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64d9-132">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="d64d9-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="d64d9-133">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="d64d9-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="d64d9-134">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="d64d9-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
