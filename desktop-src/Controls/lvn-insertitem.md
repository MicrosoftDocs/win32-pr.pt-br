---
title: LVN_INSERTITEM código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um novo item foi inserido. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456053"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="3616d-105">Código de notificação do LVN \_ INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="3616d-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="3616d-106">Notifica uma janela pai do controle de exibição de lista que um novo item foi inserido.</span><span class="sxs-lookup"><span data-stu-id="3616d-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="3616d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3616d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3616d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3616d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3616d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3616d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3616d-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="3616d-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="3616d-111">O membro **iItem** identifica o novo item e os outros membros são zero.</span><span class="sxs-lookup"><span data-stu-id="3616d-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3616d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3616d-112">Return value</span></span>

<span data-ttu-id="3616d-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3616d-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3616d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3616d-114">Requirements</span></span>



| <span data-ttu-id="3616d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3616d-115">Requirement</span></span> | <span data-ttu-id="3616d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3616d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3616d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3616d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3616d-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3616d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3616d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3616d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3616d-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3616d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3616d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3616d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3616d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3616d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





