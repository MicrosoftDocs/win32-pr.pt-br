---
title: Mensagem de WM_SETCURSOR (WinUser. h)
description: Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009456"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="c25f4-104">\_Mensagem de SETcursor do WM</span><span class="sxs-lookup"><span data-stu-id="c25f4-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="c25f4-105">Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada.</span><span class="sxs-lookup"><span data-stu-id="c25f4-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="c25f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c25f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c25f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c25f4-108">Um identificador para a janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="c25f4-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="c25f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c25f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c25f4-110">A palavra de ordem inferior de *lParam* especifica o resultado do teste de clique para a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="c25f4-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="c25f4-111">Consulte os valores de retorno para [WM_NCHITTEST](../inputdev/wm-nchittest.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c25f4-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="c25f4-112">A palavra de ordem superior do *lParam* especifica a mensagem de janela do mouse que disparou esse evento, como [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="c25f4-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="c25f4-113">Quando a janela entra no modo de menu, esse valor é zero.</span><span class="sxs-lookup"><span data-stu-id="c25f4-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c25f4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c25f4-114">Return value</span></span>

<span data-ttu-id="c25f4-115">Se um aplicativo processar essa mensagem, ele deverá retornar **true** para interromper o processamento adicional ou **false** para continuar.</span><span class="sxs-lookup"><span data-stu-id="c25f4-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25f4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c25f4-116">Remarks</span></span>

<span data-ttu-id="c25f4-117">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) passa a **mensagem \_ SetCursor do WM** para uma janela pai antes do processamento.</span><span class="sxs-lookup"><span data-stu-id="c25f4-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="c25f4-118">Se a janela pai retornar **true**, o processamento adicional será interrompido.</span><span class="sxs-lookup"><span data-stu-id="c25f4-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="c25f4-119">Passar a mensagem para a janela pai de uma janela fornece o controle de janela pai sobre a configuração do cursor em uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="c25f4-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="c25f4-120">A função **DefWindowProc** também usa essa mensagem para definir o cursor para uma seta se ela não estiver na área do cliente ou para o cursor de classe registrado, se estiver na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="c25f4-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="c25f4-121">Se a palavra de ordem inferior do parâmetro *lParam* for **HTERROR** e a palavra de ordem superior de *lParam* especificar que um dos botões do mouse será pressionado, **DefWindowProc** chamará a função [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .</span><span class="sxs-lookup"><span data-stu-id="c25f4-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c25f4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c25f4-122">Requirements</span></span>



| <span data-ttu-id="c25f4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c25f4-123">Requirement</span></span> | <span data-ttu-id="c25f4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c25f4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25f4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c25f4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c25f4-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c25f4-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c25f4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c25f4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c25f4-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c25f4-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c25f4-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c25f4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c25f4-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c25f4-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c25f4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c25f4-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c25f4-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c25f4-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c25f4-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c25f4-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="c25f4-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c25f4-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c25f4-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c25f4-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c25f4-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c25f4-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c25f4-137">Cursores</span><span class="sxs-lookup"><span data-stu-id="c25f4-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 

