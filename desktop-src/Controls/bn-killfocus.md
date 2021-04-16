---
title: Código de notificação BN_KILLFOCUS (WinUser. h)
description: Enviado quando um botão perde o foco do teclado. O botão deve ter o estilo de notificação de BS \_ para enviar esse código. A janela pai do botão recebe esse código de notificação por meio da \_ mensagem de comando do WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454825"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="5daf1-106">Código de notificação do bilhão \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="5daf1-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="5daf1-107">Enviado quando um botão perde o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="5daf1-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="5daf1-108">O botão deve ter o estilo de notificação de [**BS \_**](button-styles.md) para enviar esse código.</span><span class="sxs-lookup"><span data-stu-id="5daf1-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="5daf1-109">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5daf1-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5daf1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5daf1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5daf1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5daf1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5daf1-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="5daf1-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5daf1-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="5daf1-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5daf1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5daf1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5daf1-115">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="5daf1-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5daf1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5daf1-116">Requirements</span></span>



| <span data-ttu-id="5daf1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5daf1-117">Requirement</span></span> | <span data-ttu-id="5daf1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5daf1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5daf1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5daf1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5daf1-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5daf1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5daf1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5daf1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5daf1-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5daf1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5daf1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5daf1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5daf1-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5daf1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5daf1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5daf1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5daf1-126">BILHÃO \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="5daf1-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 

