---
title: Código de notificação EN_ERRSPACE (WinUser. h)
description: Enviado quando um controle de edição não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ .
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824201"
---
# <a name="en_errspace-notification-code"></a><span data-ttu-id="44a5a-105">\_Código de notificação en ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="44a5a-105">EN\_ERRSPACE notification code</span></span>

<span data-ttu-id="44a5a-106">Enviado quando um controle de edição não pode alocar memória suficiente para atender a uma solicitação específica.</span><span class="sxs-lookup"><span data-stu-id="44a5a-106">Sent when an edit control cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="44a5a-107">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="44a5a-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="44a5a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44a5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a5a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44a5a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a5a-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="44a5a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="44a5a-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="44a5a-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="44a5a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44a5a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a5a-113">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="44a5a-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44a5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="44a5a-114">Remarks</span></span>

<span data-ttu-id="44a5a-115">A janela pai sempre receberá uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para esse evento; ela não requer uma máscara de notificação enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="44a5a-115">The parent window will always get a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event; it does not require a notification mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="44a5a-116">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="44a5a-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="44a5a-117">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="44a5a-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44a5a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a5a-118">Requirements</span></span>



| <span data-ttu-id="44a5a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a5a-119">Requirement</span></span> | <span data-ttu-id="44a5a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="44a5a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a5a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44a5a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44a5a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44a5a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44a5a-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44a5a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44a5a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44a5a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a5a-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44a5a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a5a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="44a5a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a5a-128">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="44a5a-128">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

