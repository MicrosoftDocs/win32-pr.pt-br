---
title: LVN_GETEMPTYMARKUP código de notificação (commctrl. h)
description: Enviado por controle de exibição de lista para sua janela pai quando o controle não tem itens. O \_ código de notificação LVN GETEMPTYMARKUP é uma solicitação para que a janela pai forneça o texto de marcação. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824860"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="24897-106">Código de notificação do LVN \_ GETEMPTYMARKUP</span><span class="sxs-lookup"><span data-stu-id="24897-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="24897-107">Enviado por controle de exibição de lista para sua janela pai quando o controle não tem itens.</span><span class="sxs-lookup"><span data-stu-id="24897-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="24897-108">O \_ código de notificação LVN GETEMPTYMARKUP é uma solicitação para que a janela pai forneça o texto de marcação.</span><span class="sxs-lookup"><span data-stu-id="24897-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="24897-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="24897-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="24897-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24897-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24897-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24897-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24897-112">Ponteiro para uma estrutura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="24897-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="24897-113">Defina os membros dessa estrutura para fornecer o texto de marcação para o controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="24897-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24897-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24897-114">Return value</span></span>

<span data-ttu-id="24897-115">Retornar **true** para definir o texto de marcação no controle de exibição de lista ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="24897-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="24897-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="24897-116">Remarks</span></span>

<span data-ttu-id="24897-117">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) .</span><span class="sxs-lookup"><span data-stu-id="24897-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="24897-118">O parâmetro *wParam* contém a ID do controle que envia essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="24897-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="24897-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24897-119">Requirements</span></span>



| <span data-ttu-id="24897-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="24897-120">Requirement</span></span> | <span data-ttu-id="24897-121">Valor</span><span class="sxs-lookup"><span data-stu-id="24897-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24897-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24897-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24897-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24897-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24897-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24897-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24897-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24897-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24897-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24897-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24897-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24897-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





