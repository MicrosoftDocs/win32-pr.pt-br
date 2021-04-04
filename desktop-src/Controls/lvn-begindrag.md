---
title: LVN_BEGINDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008932"
---
# <a name="lvn_begindrag-notification-code"></a><span data-ttu-id="0100c-105">Código de notificação do LVN \_ BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="0100c-105">LVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="0100c-106">Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada.</span><span class="sxs-lookup"><span data-stu-id="0100c-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="0100c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0100c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0100c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0100c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0100c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0100c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0100c-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="0100c-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="0100c-111">O membro **iItem** identifica o item que está sendo arrastado e os outros membros são zero.</span><span class="sxs-lookup"><span data-stu-id="0100c-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0100c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0100c-112">Return value</span></span>

<span data-ttu-id="0100c-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0100c-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0100c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0100c-114">Requirements</span></span>



| <span data-ttu-id="0100c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0100c-115">Requirement</span></span> | <span data-ttu-id="0100c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0100c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0100c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0100c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0100c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0100c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0100c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0100c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0100c-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0100c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0100c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0100c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0100c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0100c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





