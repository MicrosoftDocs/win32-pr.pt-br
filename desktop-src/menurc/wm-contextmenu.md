---
title: Mensagem de WM_CONTEXTMENU (WinUser. h)
description: Notifica uma janela de que o usuário clicou com o botão direito do mouse (clicado com o botão direito) na janela.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761671"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="203be-104">Mensagem de CONTEXTMENU do WM \_</span><span class="sxs-lookup"><span data-stu-id="203be-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="203be-105">Notifica uma janela que o usuário deseja que um menu de contexto apareça.</span><span class="sxs-lookup"><span data-stu-id="203be-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="203be-106">O usuário pode ter clicado com o botão direito do mouse (clicado com o botão direito) na janela, pressionado Shift + F10 ou pressionou a chave de aplicativos (chave de menu de contexto) disponível em alguns teclados.</span><span class="sxs-lookup"><span data-stu-id="203be-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="203be-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="203be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="203be-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="203be-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="203be-109">Um identificador para a janela na qual o usuário clicou com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="203be-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="203be-110">Essa pode ser uma janela filho da janela que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="203be-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="203be-111">Para obter mais informações sobre como processar essa mensagem, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="203be-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="203be-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="203be-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="203be-113">A palavra de ordem inferior Especifica a posição horizontal do cursor, em coordenadas de tela, no momento do clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="203be-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="203be-114">A palavra de ordem superior especifica a posição vertical do cursor, em coordenadas da tela, no momento do clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="203be-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="203be-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="203be-115">Return value</span></span>

<span data-ttu-id="203be-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="203be-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="203be-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="203be-117">Remarks</span></span>

<span data-ttu-id="203be-118">Uma janela pode processar essa mensagem exibindo um menu de atalho usando as funções [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) ou [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="203be-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="203be-119">Para obter as posições horizontal e vertical, use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="203be-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="203be-120">Se uma janela não exibir um menu de atalho, ela deverá passar essa mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="203be-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="203be-121">Se uma janela for uma janela filho, o **DefWindowProc** enviará a mensagem para o pai.</span><span class="sxs-lookup"><span data-stu-id="203be-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="203be-122">Caso contrário, o **DefWindowProc** exibirá um menu de atalho padrão se a posição especificada estiver na legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="203be-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="203be-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gera a mensagem de **\_ CONTEXTMENU do WM** quando processa a mensagem do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) ou quando o usuário digita Shift + F10.</span><span class="sxs-lookup"><span data-stu-id="203be-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="203be-124">A mensagem de **\_ CONTEXTMENU do WM** também é gerada quando o usuário pressiona e libera a chave de [**\_ aplicativos VK**](/windows/desktop/inputdev/virtual-key-codes) .</span><span class="sxs-lookup"><span data-stu-id="203be-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="203be-125">Se o menu de contexto for gerado do teclado, por exemplo, se o usuário digitar SHIFT + F10, as coordenadas x e y serão-1 e o aplicativo deverá exibir o menu de contexto no local da seleção atual em vez de em (xPos, yPos).</span><span class="sxs-lookup"><span data-stu-id="203be-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="203be-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="203be-126">Requirements</span></span>



| <span data-ttu-id="203be-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="203be-127">Requirement</span></span> | <span data-ttu-id="203be-128">Valor</span><span class="sxs-lookup"><span data-stu-id="203be-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203be-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203be-129">Minimum supported client</span></span><br/> | <span data-ttu-id="203be-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="203be-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="203be-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="203be-131">Minimum supported server</span></span><br/> | <span data-ttu-id="203be-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="203be-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="203be-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="203be-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="203be-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="203be-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203be-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="203be-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="203be-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="203be-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="203be-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="203be-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="203be-138">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="203be-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="203be-139">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="203be-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="203be-140">**TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="203be-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="203be-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="203be-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="203be-142">**NCRBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="203be-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="203be-143">**RBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="203be-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="203be-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="203be-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="203be-145">Menus</span><span class="sxs-lookup"><span data-stu-id="203be-145">Menus</span></span>](menus.md)
</dt> </dl>

 

