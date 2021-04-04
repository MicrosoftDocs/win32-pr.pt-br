---
title: Código de notificação STN_DISABLE (WinUser. h)
description: O \_ código de notificação de desabilitação de STN é enviado quando um controle estático é desabilitado.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085252"
---
# <a name="stn_disable-notification-code"></a><span data-ttu-id="8d9c4-104">STN \_ desabilitar código de notificação</span><span class="sxs-lookup"><span data-stu-id="8d9c4-104">STN\_DISABLE notification code</span></span>

<span data-ttu-id="8d9c4-105">O \_ código de notificação de desabilitação de STN é enviado quando um controle estático é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8d9c4-105">The STN\_DISABLE notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="8d9c4-106">O controle estático deve ter o [**estilo \_ de notificação SS**](static-control-styles.md) para receber esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="8d9c4-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="8d9c4-107">A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8d9c4-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8d9c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d9c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d9c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d9c4-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle estático.</span><span class="sxs-lookup"><span data-stu-id="8d9c4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="8d9c4-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="8d9c4-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8d9c4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d9c4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d9c4-113">Identificador para o controle estático.</span><span class="sxs-lookup"><span data-stu-id="8d9c4-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d9c4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9c4-114">Requirements</span></span>



| <span data-ttu-id="8d9c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9c4-115">Requirement</span></span> | <span data-ttu-id="8d9c4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8d9c4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9c4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d9c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9c4-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d9c4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d9c4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d9c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9c4-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d9c4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d9c4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d9c4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9c4-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d9c4-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9c4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d9c4-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d9c4-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8d9c4-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d9c4-125">STN \_ habilitar</span><span class="sxs-lookup"><span data-stu-id="8d9c4-125">STN\_ENABLE</span></span>](stn-enable.md)
</dt> <dt>

<span data-ttu-id="8d9c4-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8d9c4-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d9c4-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="8d9c4-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="8d9c4-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8d9c4-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="8d9c4-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d9c4-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8d9c4-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d9c4-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8d9c4-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8d9c4-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

