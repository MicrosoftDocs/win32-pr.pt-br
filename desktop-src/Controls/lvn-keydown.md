---
title: LVN_KEYDOWN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma tecla foi pressionada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919240"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="dd83a-105">Código de notificação do LVN \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="dd83a-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="dd83a-106">Notifica uma janela pai do controle de exibição de lista que uma tecla foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="dd83a-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="dd83a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dd83a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dd83a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd83a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd83a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd83a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd83a-110">Ponteiro para uma estrutura [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="dd83a-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd83a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd83a-111">Return value</span></span>

<span data-ttu-id="dd83a-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="dd83a-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd83a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd83a-113">Requirements</span></span>



| <span data-ttu-id="dd83a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd83a-114">Requirement</span></span> | <span data-ttu-id="dd83a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dd83a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd83a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd83a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd83a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd83a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd83a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd83a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd83a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd83a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd83a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd83a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd83a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd83a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





