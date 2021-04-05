---
title: Código de notificação LBN_SELCHANGE (WinUser. h)
description: Notifica o aplicativo que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644667"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="565e6-105">Código de notificação do LBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="565e6-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="565e6-106">Notifica o aplicativo que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="565e6-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="565e6-107">A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="565e6-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="565e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="565e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="565e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="565e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="565e6-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="565e6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="565e6-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="565e6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="565e6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="565e6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="565e6-113">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="565e6-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="565e6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="565e6-114">Remarks</span></span>

<span data-ttu-id="565e6-115">Esse código de notificação é enviado somente por uma caixa de listagem que tem o estilo de [**\_ notificação lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="565e6-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="565e6-116">Esse código de notificação não será enviado se [**o \_ lb SETSEL**](lb-setsel.md), [**lb \_ setcurseal**](lb-setcursel.md), lb [**\_ SelectString**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) ou [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) Message alterar a seleção.</span><span class="sxs-lookup"><span data-stu-id="565e6-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="565e6-117">Para uma caixa de listagem de seleção múltipla, o \_ código de notificação lbn SELCHANGE é enviado sempre que o usuário pressiona uma tecla de seta, mesmo que a seleção não seja alterada.</span><span class="sxs-lookup"><span data-stu-id="565e6-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="565e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="565e6-118">Requirements</span></span>



| <span data-ttu-id="565e6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="565e6-119">Requirement</span></span> | <span data-ttu-id="565e6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="565e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="565e6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="565e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="565e6-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="565e6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="565e6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="565e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="565e6-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="565e6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="565e6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="565e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="565e6-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="565e6-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="565e6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="565e6-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="565e6-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="565e6-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="565e6-129">**LB- \_ REcursel**</span><span class="sxs-lookup"><span data-stu-id="565e6-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="565e6-130">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="565e6-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="565e6-131">LBN \_ SELCANCEL</span><span class="sxs-lookup"><span data-stu-id="565e6-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="565e6-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="565e6-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="565e6-133">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="565e6-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

