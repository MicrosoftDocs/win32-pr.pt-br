---
title: Código de notificação BN_CLICKED (WinUser. h)
description: Enviado quando o usuário clica em um botão. A janela pai do botão recebe esse código de notificação por meio da \_ mensagem de comando do WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- BN_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085340"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="24b5a-105">\_Código de notificação clicado em bilhão</span><span class="sxs-lookup"><span data-stu-id="24b5a-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="24b5a-106">Enviado quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="24b5a-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="24b5a-107">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="24b5a-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="24b5a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24b5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b5a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24b5a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24b5a-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="24b5a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="24b5a-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="24b5a-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="24b5a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24b5a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24b5a-113">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="24b5a-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24b5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="24b5a-114">Remarks</span></span>

<span data-ttu-id="24b5a-115">Um botão desabilitado não envia um \_ código de notificação clicado bilhão para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="24b5a-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b5a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b5a-116">Requirements</span></span>



| <span data-ttu-id="24b5a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b5a-117">Requirement</span></span> | <span data-ttu-id="24b5a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="24b5a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b5a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24b5a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24b5a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24b5a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24b5a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24b5a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24b5a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b5a-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24b5a-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b5a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b5a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="24b5a-126">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="24b5a-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="24b5a-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24b5a-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="24b5a-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24b5a-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24b5a-129">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="24b5a-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

