---
title: TVN_DELETEITEM código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que um item está sendo excluído. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455223"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="027e7-105">Código de notificação do TVN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="027e7-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="027e7-106">Notifica uma janela pai do controle de exibição de árvore que um item está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="027e7-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="027e7-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="027e7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="027e7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="027e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="027e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="027e7-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="027e7-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="027e7-111">O membro **itemOld** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **hItem** e **lParam** contêm informações válidas sobre o item que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="027e7-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027e7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="027e7-112">Return value</span></span>

<span data-ttu-id="027e7-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="027e7-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="027e7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="027e7-114">Remarks</span></span>

<span data-ttu-id="027e7-115">Se o membro **lParam** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) apontar para a memória alocada pelo seu aplicativo, você poderá liberá-lo quando receber o \_ código de notificação TVN DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="027e7-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="027e7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="027e7-116">Requirements</span></span>



| <span data-ttu-id="027e7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="027e7-117">Requirement</span></span> | <span data-ttu-id="027e7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="027e7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027e7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="027e7-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="027e7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="027e7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="027e7-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="027e7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="027e7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="027e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="027e7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="027e7-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="027e7-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="027e7-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="027e7-126">**TVN \_ DELETEITEMW** (Unicode) e **TVN \_ DELETEITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="027e7-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





