---
title: Código de notificação CBN_ERRSPACE (WinUser. h)
description: Enviado quando uma caixa de combinação não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- CBN_ERRSPACE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086423"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="67e39-105">Código de notificação do CBN \_ ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="67e39-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="67e39-106">Enviado quando uma caixa de combinação não pode alocar memória suficiente para atender a uma solicitação específica.</span><span class="sxs-lookup"><span data-stu-id="67e39-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="67e39-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="67e39-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="67e39-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67e39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67e39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e39-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="67e39-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="67e39-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="67e39-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="67e39-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67e39-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e39-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="67e39-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67e39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67e39-114">Requirements</span></span>



| <span data-ttu-id="67e39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="67e39-115">Requirement</span></span> | <span data-ttu-id="67e39-116">Valor</span><span class="sxs-lookup"><span data-stu-id="67e39-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e39-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67e39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="67e39-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67e39-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67e39-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67e39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="67e39-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67e39-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67e39-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67e39-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e39-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67e39-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e39-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="67e39-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="67e39-124">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="67e39-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="67e39-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67e39-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="67e39-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="67e39-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="67e39-127">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="67e39-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

