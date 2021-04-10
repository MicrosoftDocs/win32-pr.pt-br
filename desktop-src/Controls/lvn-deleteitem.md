---
title: LVN_DELETEITEM código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086553"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="d61ea-105">Código de notificação do LVN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="d61ea-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="d61ea-106">Notifica uma janela pai do controle de exibição de lista que um item está prestes a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d61ea-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="d61ea-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d61ea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d61ea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d61ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d61ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d61ea-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="d61ea-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="d61ea-111">O membro **iItem** identifica o item que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="d61ea-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="d61ea-112">Se o controle não tiver o estilo **LVS \_ OWNERDATA** , o *lParam* será os dados definidos pelo aplicativo associados ao item.</span><span class="sxs-lookup"><span data-stu-id="d61ea-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="d61ea-113">Todos os outros membros dessa estrutura são zero.</span><span class="sxs-lookup"><span data-stu-id="d61ea-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61ea-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d61ea-114">Return value</span></span>

<span data-ttu-id="d61ea-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d61ea-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d61ea-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d61ea-116">Remarks</span></span>

<span data-ttu-id="d61ea-117">Não adicione, exclua ou reorganize os itens na exibição de lista durante o processamento deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d61ea-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d61ea-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d61ea-118">Requirements</span></span>



| <span data-ttu-id="d61ea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d61ea-119">Requirement</span></span> | <span data-ttu-id="d61ea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d61ea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d61ea-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d61ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d61ea-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d61ea-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d61ea-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d61ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d61ea-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d61ea-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d61ea-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d61ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61ea-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d61ea-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





