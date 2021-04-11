---
title: Código de notificação CBN_SELCHANGE (WinUser. h)
description: Enviado quando o usuário altera a seleção atual na caixa de listagem de uma caixa de combinação.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919171"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="14061-104">Código de notificação do CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="14061-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="14061-105">Enviado quando o usuário altera a seleção atual na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="14061-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="14061-106">O usuário pode alterar a seleção clicando na caixa de listagem ou usando as teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="14061-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="14061-107">A janela pai da caixa de combinação recebe esse código de notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="14061-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="14061-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14061-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14061-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14061-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14061-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="14061-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="14061-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="14061-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="14061-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14061-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14061-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="14061-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14061-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="14061-114">Remarks</span></span>

<span data-ttu-id="14061-115">Para obter o índice da seleção atual, envie a mensagem [**de \_ iscurse CB**](cb-getcursel.md) para o controle.</span><span class="sxs-lookup"><span data-stu-id="14061-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="14061-116">O \_ código de notificação CBN SELCHANGE não é enviado quando a seleção atual é definida usando a mensagem do [**CB \_ setcurse**](cb-setcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="14061-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14061-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14061-117">Requirements</span></span>



| <span data-ttu-id="14061-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14061-118">Requirement</span></span> | <span data-ttu-id="14061-119">Valor</span><span class="sxs-lookup"><span data-stu-id="14061-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14061-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14061-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14061-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14061-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14061-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14061-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14061-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14061-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14061-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14061-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14061-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14061-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14061-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="14061-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="14061-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="14061-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14061-128">CBN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="14061-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="14061-129">CBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="14061-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="14061-130">**iscursel de CB \_**</span><span class="sxs-lookup"><span data-stu-id="14061-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="14061-131">**CB \_ SETcurseal**</span><span class="sxs-lookup"><span data-stu-id="14061-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="14061-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="14061-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="14061-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14061-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="14061-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14061-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14061-135">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="14061-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

