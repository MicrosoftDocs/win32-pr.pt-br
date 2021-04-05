---
title: Mensagem de WM_CTLCOLORSCROLLBAR (WinUser. h)
description: A mensagem do WM \_ CTLCOLORSCROLLBAR é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Controles de WM_CTLCOLORSCROLLBAR de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918385"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="2dfd0-104">Mensagem do WM \_ CTLCOLORSCROLLBAR</span><span class="sxs-lookup"><span data-stu-id="2dfd0-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="2dfd0-105">A mensagem do **WM \_ CTLCOLORSCROLLBAR** é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="2dfd0-106">Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de exibição para definir a cor da tela de fundo do controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="2dfd0-107">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2dfd0-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2dfd0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dfd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dfd0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2dfd0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfd0-110">Identificador para o contexto do dispositivo para o controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="2dfd0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2dfd0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfd0-112">Identificador para a barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dfd0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2dfd0-113">Return value</span></span>

<span data-ttu-id="2dfd0-114">Se um aplicativo processar essa mensagem, ele deverá retornar o identificador para um pincel.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="2dfd0-115">O sistema usa o pincel para pintar o plano de fundo do controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dfd0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dfd0-116">Remarks</span></span>

<span data-ttu-id="2dfd0-117">Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="2dfd0-118">Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="2dfd0-119">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="2dfd0-120">A mensagem do **WM \_ CTLCOLORSCROLLBAR** nunca é enviada entre threads; ela é enviada somente dentro do mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="2dfd0-121">Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="2dfd0-122">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="2dfd0-123">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="2dfd0-124">A mensagem do **WM \_ CTLCOLORSCROLLBAR** é usada somente por controles da barra de rolagem filho.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="2dfd0-125">Barras de rolagem anexadas a uma janela (WS \_ Scroll e WS \_ VSCROLL) não geram essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="2dfd0-126">Para personalizar a aparência das barras de rolagem anexadas a uma janela, use as funções da barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="2dfd0-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dfd0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dfd0-127">Requirements</span></span>



| <span data-ttu-id="2dfd0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dfd0-128">Requirement</span></span> | <span data-ttu-id="2dfd0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2dfd0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfd0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dfd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2dfd0-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dfd0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2dfd0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dfd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2dfd0-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2dfd0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2dfd0-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dfd0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dfd0-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dfd0-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dfd0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dfd0-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="2dfd0-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2dfd0-138">**CTLCOLORBTN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="2dfd0-139">**CTLCOLOREDIT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="2dfd0-140">**CTLCOLORLISTBOX do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="2dfd0-141">**CTLCOLORSTATIC do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="2dfd0-142">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2dfd0-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2dfd0-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="2dfd0-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="2dfd0-146">**CTLCOLORDLG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfd0-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

