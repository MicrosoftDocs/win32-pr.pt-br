---
title: Código de notificação CBN_DROPDOWN (WinUser. h)
description: Enviado quando a caixa de listagem de uma caixa de combinação está prestes a se tornar visível. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762754"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="6ccfc-105">\_Código de notificação da lista suspensa CBN</span><span class="sxs-lookup"><span data-stu-id="6ccfc-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="6ccfc-106">Enviado quando a caixa de listagem de uma caixa de combinação está prestes a se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="6ccfc-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6ccfc-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6ccfc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ccfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccfc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ccfc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccfc-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="6ccfc-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6ccfc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ccfc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccfc-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ccfc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ccfc-114">Remarks</span></span>

<span data-ttu-id="6ccfc-115">Esse código de notificação só será enviado se a caixa de combinação tiver o estilo [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6ccfc-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccfc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccfc-116">Requirements</span></span>



| <span data-ttu-id="6ccfc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccfc-117">Requirement</span></span> | <span data-ttu-id="6ccfc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ccfc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccfc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ccfc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccfc-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ccfc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6ccfc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ccfc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccfc-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ccfc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ccfc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ccfc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccfc-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccfc-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ccfc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ccfc-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ccfc-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6ccfc-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6ccfc-127">CBN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="6ccfc-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="6ccfc-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6ccfc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6ccfc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ccfc-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6ccfc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ccfc-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6ccfc-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6ccfc-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

