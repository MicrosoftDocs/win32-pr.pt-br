---
title: Mensagem de WM_CTLCOLORSTATIC (WinUser. h)
description: Um controle estático, ou um controle de edição que é somente leitura ou desabilitado, envia a \_ mensagem do WM CTLCOLORSTATIC para sua janela pai quando o controle está prestes a ser desenhado.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Controles de WM_CTLCOLORSTATIC de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644616"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="f4040-104">Mensagem do WM \_ CTLCOLORSTATIC</span><span class="sxs-lookup"><span data-stu-id="f4040-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="f4040-105">Um controle estático, ou um controle de edição que é somente leitura ou desabilitado, envia a mensagem do **WM \_ CTLCOLORSTATIC** para sua janela pai quando o controle está prestes a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="f4040-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="f4040-106">Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto do dispositivo especificado para definir as cores de primeiro plano do texto e do plano de fundo do controle estático.</span><span class="sxs-lookup"><span data-stu-id="f4040-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="f4040-107">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f4040-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f4040-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4040-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4040-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4040-110">Identificador para o contexto do dispositivo para a janela de controle estático.</span><span class="sxs-lookup"><span data-stu-id="f4040-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="f4040-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4040-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4040-112">Identificador para o controle estático.</span><span class="sxs-lookup"><span data-stu-id="f4040-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4040-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4040-113">Return value</span></span>

<span data-ttu-id="f4040-114">Se um aplicativo processar essa mensagem, o valor de retorno será um identificador para um pincel que o sistema usa para pintar o plano de fundo do controle estático.</span><span class="sxs-lookup"><span data-stu-id="f4040-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4040-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4040-115">Remarks</span></span>

<span data-ttu-id="f4040-116">Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="f4040-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="f4040-117">Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="f4040-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="f4040-118">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle estático.</span><span class="sxs-lookup"><span data-stu-id="f4040-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="f4040-119">Você pode definir a cor do plano de fundo do texto de um controle de edição desabilitado, mas não pode definir a cor do primeiro plano do texto.</span><span class="sxs-lookup"><span data-stu-id="f4040-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="f4040-120">O sistema sempre usa a cor \_ GRAYTEXT.</span><span class="sxs-lookup"><span data-stu-id="f4040-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="f4040-121">Os controles de edição que não são somente leitura ou desabilitados não enviam a mensagem do **WM \_ CTLCOLORSTATIC** ; em vez disso, eles enviam a mensagem do [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="f4040-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="f4040-122">A mensagem do **WM \_ CTLCOLORSTATIC** nunca é enviada entre threads; ela é enviada somente dentro do mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="f4040-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="f4040-123">Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="f4040-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="f4040-124">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="f4040-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="f4040-125">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f4040-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="f4040-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4040-126">Examples</span></span>

<span data-ttu-id="f4040-127">O exemplo de C++ a seguir mostra como definir as cores de primeiro e segundo plano do texto de um controle estático em resposta à mensagem **\_ CTLCOLORSTATIC do WM** .</span><span class="sxs-lookup"><span data-stu-id="f4040-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="f4040-128">A `hbrBkgnd` variável é uma variável **HBRUSH** estática que é inicializada como NULL e armazena o pincel de plano de fundo entre chamadas para o **WM \_ CTLCOLORSTATIC**.</span><span class="sxs-lookup"><span data-stu-id="f4040-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="f4040-129">O pincel deve ser destruído por uma chamada para a função [**ExcluirObjeto**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) quando não for mais necessário, normalmente quando a caixa de diálogo associada for destruída.</span><span class="sxs-lookup"><span data-stu-id="f4040-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="f4040-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4040-130">Requirements</span></span>



| <span data-ttu-id="f4040-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4040-131">Requirement</span></span> | <span data-ttu-id="f4040-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f4040-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4040-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4040-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f4040-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4040-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4040-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4040-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f4040-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4040-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4040-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4040-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4040-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4040-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4040-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f4040-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4040-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f4040-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4040-141">**CTLCOLORBTN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f4040-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="f4040-142">**CTLCOLOREDIT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f4040-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="f4040-143">**CTLCOLORLISTBOX do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f4040-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="f4040-144">**CTLCOLORSCROLLBAR do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f4040-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="f4040-145">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="f4040-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f4040-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f4040-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f4040-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="f4040-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="f4040-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="f4040-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="f4040-149">**CTLCOLORDLG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f4040-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

