---
title: Código de notificação LBN_SETFOCUS (WinUser. h)
description: Notifica o aplicativo que a caixa de listagem recebeu o foco do teclado. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- LBN_SETFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824427"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="2b76f-105">\_Código de notificação lbn SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="2b76f-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="2b76f-106">Notifica o aplicativo que a caixa de listagem recebeu o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="2b76f-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="2b76f-107">A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2b76f-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2b76f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b76f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b76f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b76f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b76f-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2b76f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="2b76f-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="2b76f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2b76f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b76f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b76f-113">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2b76f-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b76f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b76f-114">Requirements</span></span>



| <span data-ttu-id="2b76f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b76f-115">Requirement</span></span> | <span data-ttu-id="2b76f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2b76f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b76f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b76f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b76f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b76f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b76f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b76f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b76f-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b76f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b76f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b76f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b76f-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b76f-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b76f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b76f-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b76f-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2b76f-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b76f-125">LBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="2b76f-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="2b76f-126">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2b76f-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2b76f-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b76f-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2b76f-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b76f-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2b76f-129">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2b76f-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

