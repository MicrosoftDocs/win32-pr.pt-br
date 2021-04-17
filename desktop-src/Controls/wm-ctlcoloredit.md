---
title: Mensagem de WM_CTLCOLOREDIT (WinUser. h)
description: Um controle de edição que não é somente leitura ou desabilitado envia a \_ mensagem do WM CTLCOLOREDIT para sua janela pai quando o controle está prestes a ser desenhado.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Controles de WM_CTLCOLOREDIT de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454611"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="75529-104">Mensagem do WM \_ CTLCOLOREDIT</span><span class="sxs-lookup"><span data-stu-id="75529-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="75529-105">Um controle de edição que não é somente leitura ou desabilitado envia a mensagem do **WM \_ CTLCOLOREDIT** para sua janela pai quando o controle está prestes a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="75529-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="75529-106">Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de dispositivo especificado para definir o texto e as cores de plano de fundo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75529-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="75529-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75529-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75529-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75529-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75529-109">Um identificador para o contexto do dispositivo para a janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75529-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="75529-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75529-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75529-111">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75529-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75529-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75529-112">Return value</span></span>

<span data-ttu-id="75529-113">Se um aplicativo processar essa mensagem, ele deverá retornar o identificador de um pincel.</span><span class="sxs-lookup"><span data-stu-id="75529-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="75529-114">O sistema usa o pincel para pintar o plano de fundo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75529-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="75529-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="75529-115">Remarks</span></span>

<span data-ttu-id="75529-116">Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="75529-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="75529-117">Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="75529-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="75529-118">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="75529-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="75529-119">Os controles de edição somente leitura ou desabilitados não enviam a mensagem do **WM \_ CTLCOLOREDIT** ; em vez disso, eles enviam a mensagem do [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .</span><span class="sxs-lookup"><span data-stu-id="75529-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="75529-120">A mensagem do **WM \_ CTLCOLOREDIT** nunca é enviada entre threads, ela é enviada somente dentro do mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="75529-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="75529-121">Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="75529-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="75529-122">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="75529-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="75529-123">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="75529-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="75529-124">**Edição avançada:** Não há suporte para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="75529-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="75529-125">Para definir a cor do plano de fundo para um controle de edição rico, use a mensagem em [**\_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="75529-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="75529-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75529-126">Requirements</span></span>



| <span data-ttu-id="75529-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="75529-127">Requirement</span></span> | <span data-ttu-id="75529-128">Valor</span><span class="sxs-lookup"><span data-stu-id="75529-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75529-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75529-129">Minimum supported client</span></span><br/> | <span data-ttu-id="75529-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75529-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="75529-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75529-131">Minimum supported server</span></span><br/> | <span data-ttu-id="75529-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75529-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75529-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75529-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="75529-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75529-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75529-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="75529-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="75529-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="75529-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75529-137">**em \_ SETBKGNDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="75529-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="75529-138">**CTLCOLORSTATIC do WM \_**</span><span class="sxs-lookup"><span data-stu-id="75529-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="75529-139">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="75529-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="75529-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="75529-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="75529-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="75529-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="75529-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="75529-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

