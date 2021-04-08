---
title: ACN_STOP código de notificação (commctrl. h)
description: Notifica a janela pai de um controle de animação que o clipe AVI associado parou de ser reproduzido. Esse código de notificação é enviado na forma de uma mensagem de comando do WM \_ .
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009075"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="36016-105">\_Código de notificação de parada ACN</span><span class="sxs-lookup"><span data-stu-id="36016-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="36016-106">Notifica a janela pai de um controle de animação que o clipe AVI associado parou de ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="36016-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="36016-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="36016-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="36016-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36016-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36016-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36016-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de animação.</span><span class="sxs-lookup"><span data-stu-id="36016-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="36016-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="36016-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="36016-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36016-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36016-113">Um **HWND** que especifica o identificador para o controle de animação.</span><span class="sxs-lookup"><span data-stu-id="36016-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36016-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36016-114">Requirements</span></span>



| <span data-ttu-id="36016-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36016-115">Requirement</span></span> | <span data-ttu-id="36016-116">Valor</span><span class="sxs-lookup"><span data-stu-id="36016-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36016-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36016-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36016-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36016-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36016-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36016-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36016-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36016-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36016-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36016-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="36016-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36016-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

