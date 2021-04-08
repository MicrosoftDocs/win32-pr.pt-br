---
title: LVN_ITEMACTIVATE código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário ativa um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086551"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="0037d-105">Código de notificação do LVN \_</span><span class="sxs-lookup"><span data-stu-id="0037d-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="0037d-106">Enviado por um controle de exibição de lista quando o usuário ativa um item.</span><span class="sxs-lookup"><span data-stu-id="0037d-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="0037d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0037d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="0037d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0037d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0037d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0037d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0037d-110">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="0037d-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="0037d-111">Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0037d-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="0037d-112">[Versão 4,70](common-control-versions.md) e anterior.</span><span class="sxs-lookup"><span data-stu-id="0037d-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="0037d-113">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0037d-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0037d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0037d-114">Return value</span></span>

<span data-ttu-id="0037d-115">O aplicativo que recebe esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="0037d-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0037d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0037d-116">Remarks</span></span>

<span data-ttu-id="0037d-117">Para obter os itens que estão sendo ativados, o aplicativo de recebimento deve usar a mensagem [**\_ GETSELECTEDCOUNT LVM**](lvm-getselectedcount.md) para recuperar o número de itens selecionados e, em seguida, enviar a mensagem do [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) com o **LVNI \_ selecionado** até que todos os itens tenham sido recuperados.</span><span class="sxs-lookup"><span data-stu-id="0037d-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="0037d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0037d-118">Requirements</span></span>



| <span data-ttu-id="0037d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0037d-119">Requirement</span></span> | <span data-ttu-id="0037d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0037d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0037d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0037d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0037d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0037d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0037d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0037d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0037d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0037d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0037d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0037d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0037d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0037d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





