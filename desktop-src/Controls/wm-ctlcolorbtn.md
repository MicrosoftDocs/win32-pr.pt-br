---
title: Mensagem de WM_CTLCOLORBTN (WinUser. h)
description: A mensagem do WM \_ CTLCOLORBTN é enviada para a janela pai de um botão antes de desenhar o botão. A janela pai pode alterar o texto do botão e as cores do plano de fundo. No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa essa mensagem.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Controles de WM_CTLCOLORBTN de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917978"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="8f537-106">Mensagem do WM \_ CTLCOLORBTN</span><span class="sxs-lookup"><span data-stu-id="8f537-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="8f537-107">A mensagem do **WM \_ CTLCOLORBTN** é enviada para a janela pai de um botão antes de desenhar o botão.</span><span class="sxs-lookup"><span data-stu-id="8f537-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="8f537-108">A janela pai pode alterar o texto do botão e as cores do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="8f537-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="8f537-109">No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f537-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8f537-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f537-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f537-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f537-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f537-112">Um **HDC** que especifica o identificador para o contexto de exibição do botão.</span><span class="sxs-lookup"><span data-stu-id="8f537-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="8f537-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f537-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f537-114">Um **HWND** que especifica o identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="8f537-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f537-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f537-115">Return value</span></span>

<span data-ttu-id="8f537-116">Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel.</span><span class="sxs-lookup"><span data-stu-id="8f537-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="8f537-117">O sistema usa o pincel para pintar o plano de fundo do botão.</span><span class="sxs-lookup"><span data-stu-id="8f537-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f537-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f537-118">Remarks</span></span>

<span data-ttu-id="8f537-119">Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="8f537-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="8f537-120">Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.</span><span class="sxs-lookup"><span data-stu-id="8f537-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="8f537-121">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o botão.</span><span class="sxs-lookup"><span data-stu-id="8f537-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="8f537-122">Os botões com os estilos de botão de [**\_ pressão BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)ou [**BS \_ PUSHLIKE**](button-styles.md) não usam o pincel retornado.</span><span class="sxs-lookup"><span data-stu-id="8f537-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="8f537-123">Os botões com esses estilos são sempre desenhados com as cores padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="8f537-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="8f537-124">O desenho de botões de push requer vários pincéis diferentes: face, realce e sombra, mas a mensagem do **WM \_ CTLCOLORBTN** permite que apenas um pincel seja retornado.</span><span class="sxs-lookup"><span data-stu-id="8f537-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="8f537-125">Para fornecer uma aparência personalizada para botões de push, use um botão de desenho proprietário.</span><span class="sxs-lookup"><span data-stu-id="8f537-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="8f537-126">Para obter mais informações, consulte [criando controles de Owner-Drawn](user-controls-intro.md).</span><span class="sxs-lookup"><span data-stu-id="8f537-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="8f537-127">A mensagem do **WM \_ CTLCOLORBTN** nunca é enviada entre threads.</span><span class="sxs-lookup"><span data-stu-id="8f537-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="8f537-128">Ele é enviado somente dentro de um thread.</span><span class="sxs-lookup"><span data-stu-id="8f537-128">It is sent only within one thread.</span></span>

<span data-ttu-id="8f537-129">A cor do texto de uma caixa de seleção ou botão de opção se aplica à caixa ou ao botão, à marca de seleção e ao texto.</span><span class="sxs-lookup"><span data-stu-id="8f537-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="8f537-130">O retângulo de foco para esses botões permanece a cor padrão do sistema (normalmente preto).</span><span class="sxs-lookup"><span data-stu-id="8f537-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="8f537-131">A cor do texto de uma caixa de grupo se aplica ao texto, mas não à linha que define a caixa.</span><span class="sxs-lookup"><span data-stu-id="8f537-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="8f537-132">A cor do texto de um botão de ação é aplicável somente ao seu retângulo de foco; Ele não afeta a cor do texto.</span><span class="sxs-lookup"><span data-stu-id="8f537-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="8f537-133">Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="8f537-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="8f537-134">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="8f537-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="8f537-135">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8f537-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f537-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f537-136">Requirements</span></span>



| <span data-ttu-id="8f537-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f537-137">Requirement</span></span> | <span data-ttu-id="8f537-138">Valor</span><span class="sxs-lookup"><span data-stu-id="8f537-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f537-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f537-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8f537-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f537-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f537-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f537-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8f537-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f537-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f537-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f537-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f537-144"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f537-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f537-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f537-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f537-146">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8f537-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8f537-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="8f537-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="8f537-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="8f537-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

