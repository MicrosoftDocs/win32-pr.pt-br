---
title: Código de notificação CBN_KILLFOCUS (WinUser. h)
description: Enviado quando uma caixa de combinação perde o foco do teclado. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 0118a2ff-9811-4bf1-b3f6-1d00ca5c8dbe
keywords:
- CBN_KILLFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e266824bf8bcdac1fb901d40ca2b15406fc79660
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753793"
---
# <a name="cbn_killfocus-notification-code"></a><span data-ttu-id="d2c22-105">Código de notificação do CBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="d2c22-105">CBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="d2c22-106">Enviado quando uma caixa de combinação perde o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="d2c22-106">Sent when a combo box loses the keyboard focus.</span></span> <span data-ttu-id="d2c22-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d2c22-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d2c22-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2c22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2c22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c22-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d2c22-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d2c22-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d2c22-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d2c22-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2c22-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c22-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d2c22-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2c22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c22-114">Requirements</span></span>



| <span data-ttu-id="d2c22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c22-115">Requirement</span></span> | <span data-ttu-id="d2c22-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d2c22-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c22-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2c22-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c22-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2c22-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2c22-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2c22-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c22-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2c22-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2c22-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2c22-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c22-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2c22-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2c22-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2c22-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2c22-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d2c22-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2c22-125">CBN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="d2c22-125">CBN\_SETFOCUS</span></span>](cbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="d2c22-126">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="d2c22-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d2c22-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2c22-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d2c22-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2c22-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2c22-129">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d2c22-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

