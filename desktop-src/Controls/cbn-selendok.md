---
title: Código de notificação CBN_SELENDOK (WinUser. h)
description: Enviado quando o usuário seleciona um item de lista ou seleciona um item e fecha a lista. Indica que a seleção do usuário deve ser processada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771697"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="8fb13-106">Código de notificação do CBN \_ SELENDOK</span><span class="sxs-lookup"><span data-stu-id="8fb13-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="8fb13-107">Enviado quando o usuário seleciona um item de lista ou seleciona um item e fecha a lista.</span><span class="sxs-lookup"><span data-stu-id="8fb13-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="8fb13-108">Indica que a seleção do usuário deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="8fb13-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="8fb13-109">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8fb13-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8fb13-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fb13-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb13-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fb13-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb13-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="8fb13-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="8fb13-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="8fb13-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8fb13-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fb13-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb13-115">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="8fb13-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fb13-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fb13-116">Remarks</span></span>

<span data-ttu-id="8fb13-117">Em uma caixa de combinação com o estilo [**\_ simples do CBS**](combo-box-styles.md) , o \_ código de notificação CBN SELENDOK é enviado imediatamente antes de cada código de notificação do [CBN \_ SELCHANGE](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb13-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb13-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb13-118">Requirements</span></span>



| <span data-ttu-id="8fb13-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb13-119">Requirement</span></span> | <span data-ttu-id="8fb13-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8fb13-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb13-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fb13-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb13-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fb13-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fb13-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fb13-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb13-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fb13-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fb13-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fb13-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb13-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fb13-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb13-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fb13-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8fb13-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8fb13-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8fb13-129">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="8fb13-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="8fb13-130">CBN \_ SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="8fb13-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="8fb13-131">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8fb13-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="8fb13-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8fb13-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8fb13-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8fb13-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8fb13-134">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8fb13-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

