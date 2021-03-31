---
title: Código de notificação CBN_SELENDCANCEL (WinUser. h)
description: Enviado quando o usuário seleciona um item, mas seleciona outro controle ou fecha a caixa de diálogo. Indica que a seleção inicial do usuário deve ser ignorada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645036"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="2eb7e-106">Código de notificação do CBN \_ SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="2eb7e-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="2eb7e-107">Enviado quando o usuário seleciona um item, mas seleciona outro controle ou fecha a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="2eb7e-108">Indica que a seleção inicial do usuário deve ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="2eb7e-109">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2eb7e-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2eb7e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eb7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb7e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2eb7e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eb7e-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="2eb7e-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2eb7e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eb7e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eb7e-115">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eb7e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eb7e-116">Remarks</span></span>

<span data-ttu-id="2eb7e-117">Em uma caixa de combinação com o estilo [**\_ simples do CBS**](combo-box-styles.md) , o \_ código de notificação CBN SELENDCANCEL não é enviado.</span><span class="sxs-lookup"><span data-stu-id="2eb7e-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="2eb7e-118">O código de notificação [CBN \_ SELENDOK](cbn-selendok.md) é enviado imediatamente antes de cada código de notificação do [CBN \_ SELCHANGE](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb7e-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb7e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb7e-119">Requirements</span></span>



| <span data-ttu-id="2eb7e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb7e-120">Requirement</span></span> | <span data-ttu-id="2eb7e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2eb7e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb7e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb7e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2eb7e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2eb7e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb7e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2eb7e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2eb7e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2eb7e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb7e-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb7e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb7e-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2eb7e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2eb7e-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2eb7e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2eb7e-130">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="2eb7e-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="2eb7e-131">CBN \_ SELENDOK</span><span class="sxs-lookup"><span data-stu-id="2eb7e-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="2eb7e-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2eb7e-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2eb7e-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2eb7e-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2eb7e-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2eb7e-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2eb7e-135">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2eb7e-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

