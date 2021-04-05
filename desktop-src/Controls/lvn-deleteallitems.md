---
title: LVN_DELETEALLITEMS código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que todos os itens no controle estão prestes a ser excluídos. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919245"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="21f03-105">Código de notificação do LVN \_ DELETEALLITEMS</span><span class="sxs-lookup"><span data-stu-id="21f03-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="21f03-106">Notifica uma janela pai do controle de exibição de lista que todos os itens no controle estão prestes a ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="21f03-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="21f03-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="21f03-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="21f03-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21f03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21f03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21f03-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="21f03-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="21f03-111">O membro **iItem** é-1 e os outros membros são zero.</span><span class="sxs-lookup"><span data-stu-id="21f03-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f03-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21f03-112">Return value</span></span>

<span data-ttu-id="21f03-113">Para suprimir os códigos de notificação subsequentes do [LVN \_ DELETEITEM](lvn-deleteitem.md) , retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="21f03-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="21f03-114">Para receber códigos de notificação [LVN \_ DELETEITEM](lvn-deleteitem.md) subsequentes, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="21f03-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f03-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="21f03-115">Remarks</span></span>

<span data-ttu-id="21f03-116">Um controle de exibição de lista envia o código de notificação do [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) quando ele é destruído ou recebe a mensagem do **LVM \_ DELETEALLITEMS** .</span><span class="sxs-lookup"><span data-stu-id="21f03-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="21f03-117">Se o **LVM \_ DELETEALLITEMS** não retornar **true**, o controle também enviará um código de notificação [LVN \_ DELETEITEM](lvn-deleteitem.md) , pois cada item será excluído.</span><span class="sxs-lookup"><span data-stu-id="21f03-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="21f03-118">Se o manipulador de mensagens [**\_ DELETEALLITEMS do LVM**](lvm-deleteallitems.md) estiver em um procedimento da caixa de diálogo, retorne **verdadeiro** do procedimento da caixa de diálogo e use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT para definir o valor de retorno da mensagem.</span><span class="sxs-lookup"><span data-stu-id="21f03-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f03-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21f03-119">Requirements</span></span>



| <span data-ttu-id="21f03-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f03-120">Requirement</span></span> | <span data-ttu-id="21f03-121">Valor</span><span class="sxs-lookup"><span data-stu-id="21f03-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21f03-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21f03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21f03-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21f03-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21f03-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21f03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21f03-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21f03-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21f03-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21f03-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f03-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f03-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

