---
title: Código de notificação STN_CLICKED (WinUser. h)
description: O \_ código de notificação clicado em STN é enviado quando o usuário clica em um controle estático que tem o \_ estilo de notificação SS. A janela pai do controle recebe esse código de notificação por meio da \_ mensagem de comando do WM.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824190"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="cb6de-105">\_Código de notificação clicado em STN</span><span class="sxs-lookup"><span data-stu-id="cb6de-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="cb6de-106">O \_ código de notificação clicado em STN é enviado quando o usuário clica em um controle estático que tem o estilo de [**\_ notificação SS**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="cb6de-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="cb6de-107">A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="cb6de-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cb6de-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb6de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb6de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb6de-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle estático.</span><span class="sxs-lookup"><span data-stu-id="cb6de-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="cb6de-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="cb6de-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cb6de-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb6de-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb6de-113">Identificador para o controle estático.</span><span class="sxs-lookup"><span data-stu-id="cb6de-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb6de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb6de-114">Requirements</span></span>



| <span data-ttu-id="cb6de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6de-115">Requirement</span></span> | <span data-ttu-id="cb6de-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cb6de-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6de-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6de-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb6de-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb6de-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6de-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb6de-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb6de-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb6de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6de-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb6de-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb6de-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb6de-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb6de-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cb6de-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb6de-125">STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="cb6de-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="cb6de-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cb6de-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb6de-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="cb6de-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="cb6de-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="cb6de-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="cb6de-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb6de-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cb6de-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb6de-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cb6de-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cb6de-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

