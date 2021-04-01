---
title: ACN_START código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de animação que o clipe AVI associado começou a ser reproduzido. Esse código de notificação é enviado na forma de uma mensagem de comando do WM \_ .
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644404"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="93dbe-105">ACN \_ Iniciar código de notificação</span><span class="sxs-lookup"><span data-stu-id="93dbe-105">ACN\_START notification code</span></span>

<span data-ttu-id="93dbe-106">Notifica uma janela pai do controle de animação que o clipe AVI associado começou a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="93dbe-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="93dbe-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="93dbe-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="93dbe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93dbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93dbe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93dbe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93dbe-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de animação.</span><span class="sxs-lookup"><span data-stu-id="93dbe-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="93dbe-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="93dbe-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="93dbe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93dbe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93dbe-113">Um **HWND** que especifica o identificador para o controle de animação.</span><span class="sxs-lookup"><span data-stu-id="93dbe-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93dbe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93dbe-114">Requirements</span></span>



| <span data-ttu-id="93dbe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="93dbe-115">Requirement</span></span> | <span data-ttu-id="93dbe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="93dbe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93dbe-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93dbe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93dbe-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93dbe-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93dbe-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93dbe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93dbe-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93dbe-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93dbe-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93dbe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="93dbe-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93dbe-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

