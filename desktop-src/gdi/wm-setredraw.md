---
description: Você envia a mensagem de **WM_SETREDRAW** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensagem de WM_SETREDRAW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593452"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="e1819-103">WM_SETREDRAW mensagem</span><span class="sxs-lookup"><span data-stu-id="e1819-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="e1819-104">Você envia a mensagem de **\_ redesenho do WM** para uma janela para permitir que as alterações nessa janela sejam redesenhadas ou para impedir que as alterações nessa janela sejam redesenhadas.</span><span class="sxs-lookup"><span data-stu-id="e1819-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="e1819-105">Para enviar essa mensagem, chame a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1819-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="e1819-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1819-106">Parameters</span></span>

`wParam`

<span data-ttu-id="e1819-107">O estado de redesenho.</span><span class="sxs-lookup"><span data-stu-id="e1819-107">The redraw state.</span></span> <span data-ttu-id="e1819-108">Se esse parâmetro for **true**, o conteúdo poderá ser redesenhado após uma alteração.</span><span class="sxs-lookup"><span data-stu-id="e1819-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="e1819-109">Se esse parâmetro for **false**, o conteúdo não poderá ser redesenhado após uma alteração.</span><span class="sxs-lookup"><span data-stu-id="e1819-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="e1819-110">Esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e1819-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1819-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1819-111">Return value</span></span>

<span data-ttu-id="e1819-112">Seu aplicativo deverá retornar 0 se processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1819-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1819-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1819-113">Remarks</span></span>

<span data-ttu-id="e1819-114">Essa mensagem poderá ser útil se o aplicativo precisar adicionar vários itens a uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e1819-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="e1819-115">Seu aplicativo pode chamar essa mensagem com *wParam* definido como **false**, adicionar os itens e, em seguida, chamar a mensagem novamente com *wParam* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="e1819-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="e1819-116">Por fim, seu aplicativo pode chamar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **NULL**, **NULL**, RDW \_ apagar \| RDW \_ quadro \| RDW \_ invalidar \| RDW \_ filhos) para fazer com que a caixa de listagem seja repintada.</span><span class="sxs-lookup"><span data-stu-id="e1819-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="e1819-117">Você deve usar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) com os sinalizadores especificados, em vez de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), porque o primeiro é necessário para alguns controles que têm uma área não cliente própria ou que têm estilos de janela que fazem com que eles recebam uma área que não seja de cliente (como **WS_THICKFRAME**, **WS_BORDER** ou **WS_EX_CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="e1819-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="e1819-118">Se o controle não tiver uma área não cliente, **RedrawWindow** com esses sinalizadores fará apenas a invalidação que o **InvalidateRect** faria.</span><span class="sxs-lookup"><span data-stu-id="e1819-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="e1819-119">Passar uma mensagem de **WM_SETREDRAW** para a função **DefWindowProc** remove o estilo de **WS_VISIBLE** da janela quando *wParam* é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="e1819-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="e1819-120">Embora o conteúdo da janela permaneça visível na tela, a função [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) retorna **false** quando chamado em uma janela nesse estado.</span><span class="sxs-lookup"><span data-stu-id="e1819-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="e1819-121">Passar uma mensagem de **WM_SETREDRAW** para a função **DefWindowProc** adiciona o estilo de **WS_VISIBLE** à janela, se não estiver definido, quando *wParam* estiver definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="e1819-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="e1819-122">Se seu aplicativo enviar a mensagem de **WM_SETREDRAW** com *wParam* definido como **true** para uma janela oculta, a janela ficará visível.</span><span class="sxs-lookup"><span data-stu-id="e1819-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="e1819-123">**Windows 10 e posterior; Windows Server 2016 e posterior**.</span><span class="sxs-lookup"><span data-stu-id="e1819-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="e1819-124">O sistema define uma propriedade chamada *SysSetRedraw* em uma janela cujo procedimento de janela passa **WM_SETREDRAW** mensagens para **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="e1819-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="e1819-125">Você pode usar a função [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) para obter o valor da propriedade quando ela estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="e1819-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="e1819-126">**GetProp** retorna um valor diferente de zero quando redesenhar está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e1819-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="e1819-127">**GetProp** retornará zero quando redesenhar estiver habilitado ou quando a Propriedade Window não existir.</span><span class="sxs-lookup"><span data-stu-id="e1819-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="e1819-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1819-128">Requirements</span></span>

| <span data-ttu-id="e1819-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1819-129">Requirement</span></span> | <span data-ttu-id="e1819-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e1819-130">Value</span></span> |
|-|-|
| <span data-ttu-id="e1819-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1819-131">Minimum supported client</span></span> | <span data-ttu-id="e1819-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1819-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="e1819-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1819-133">Minimum supported server</span></span> | <span data-ttu-id="e1819-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1819-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="e1819-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1819-135">Header</span></span> | <dl><span data-ttu-id="e1819-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1819-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="e1819-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1819-137">See also</span></span>

* [<span data-ttu-id="e1819-138">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="e1819-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="e1819-139">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="e1819-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="e1819-140">RedrawWindow</span><span class="sxs-lookup"><span data-stu-id="e1819-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
