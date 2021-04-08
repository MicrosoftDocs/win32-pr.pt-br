---
title: Código de notificação STN_DBLCLK (WinUser. h)
description: O \_ código de notificação STN DBLCLK é enviado quando o usuário clica duas vezes em um controle estático com o \_ estilo de notificação SS. A janela pai do controle recebe esse código de notificação por meio da \_ mensagem de comando do WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009069"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="def54-105">Código de notificação do STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="def54-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="def54-106">O \_ código de notificação STN DBLCLK é enviado quando o usuário clica duas vezes em um controle estático com o estilo de [**\_ notificação SS**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="def54-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="def54-107">A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="def54-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="def54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="def54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def54-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle estático.</span><span class="sxs-lookup"><span data-stu-id="def54-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="def54-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="def54-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="def54-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="def54-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def54-113">Identificador para o controle estático.</span><span class="sxs-lookup"><span data-stu-id="def54-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="def54-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def54-114">Requirements</span></span>



| <span data-ttu-id="def54-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="def54-115">Requirement</span></span> | <span data-ttu-id="def54-116">Valor</span><span class="sxs-lookup"><span data-stu-id="def54-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def54-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def54-117">Minimum supported client</span></span><br/> | <span data-ttu-id="def54-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="def54-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="def54-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def54-119">Minimum supported server</span></span><br/> | <span data-ttu-id="def54-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="def54-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="def54-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="def54-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="def54-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="def54-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def54-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="def54-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="def54-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="def54-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="def54-125">STN \_ clicou</span><span class="sxs-lookup"><span data-stu-id="def54-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="def54-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="def54-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="def54-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="def54-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="def54-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="def54-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="def54-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="def54-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="def54-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="def54-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="def54-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="def54-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

