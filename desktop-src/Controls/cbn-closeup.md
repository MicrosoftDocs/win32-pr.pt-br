---
title: Código de notificação CBN_CLOSEUP (WinUser. h)
description: Enviado quando a caixa de listagem de uma caixa de combinação foi fechada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086477"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="ce56d-105">Código de notificação do CBN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="ce56d-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="ce56d-106">Enviado quando a caixa de listagem de uma caixa de combinação foi fechada.</span><span class="sxs-lookup"><span data-stu-id="ce56d-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="ce56d-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ce56d-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ce56d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce56d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce56d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce56d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce56d-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="ce56d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="ce56d-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="ce56d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ce56d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce56d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce56d-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="ce56d-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce56d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce56d-114">Remarks</span></span>

<span data-ttu-id="ce56d-115">Se o usuário alterou a seleção atual, a caixa de combinação também envia o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) quando a lista suspensa é fechada.</span><span class="sxs-lookup"><span data-stu-id="ce56d-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="ce56d-116">Em geral, não é possível prever a ordem na qual os códigos de notificação serão enviados.</span><span class="sxs-lookup"><span data-stu-id="ce56d-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="ce56d-117">Em particular, um \_ código de notificação CBN SELCHANGE pode ocorrer antes ou depois de um \_ código de notificação do CBN closeup.</span><span class="sxs-lookup"><span data-stu-id="ce56d-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="ce56d-118">Para executar um processo específico cada vez que o usuário seleciona um item de lista, você pode manipular o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) ou CBN \_ closeup.</span><span class="sxs-lookup"><span data-stu-id="ce56d-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="ce56d-119">Normalmente, você esperaria pelo código de \_ notificação CBN closeup antes de processar uma alteração na seleção atual.</span><span class="sxs-lookup"><span data-stu-id="ce56d-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="ce56d-120">Isso pode ser particularmente importante se uma quantidade significativa de processamento for necessária.</span><span class="sxs-lookup"><span data-stu-id="ce56d-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="ce56d-121">Esse código de notificação não é enviado para uma caixa de combinação que tem o estilo [**\_ simples do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ce56d-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce56d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce56d-122">Requirements</span></span>



| <span data-ttu-id="ce56d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce56d-123">Requirement</span></span> | <span data-ttu-id="ce56d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ce56d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce56d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce56d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ce56d-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce56d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ce56d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce56d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ce56d-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce56d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce56d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce56d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce56d-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce56d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce56d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce56d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce56d-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ce56d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce56d-133">\_lista suspensa CBN</span><span class="sxs-lookup"><span data-stu-id="ce56d-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="ce56d-134">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="ce56d-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="ce56d-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ce56d-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ce56d-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce56d-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ce56d-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce56d-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ce56d-138">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ce56d-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

