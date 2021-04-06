---
title: LVN_BEGINRDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão direito do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918030"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="8373c-105">Código de notificação do LVN \_ BEGINRDRAG</span><span class="sxs-lookup"><span data-stu-id="8373c-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="8373c-106">Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão direito do mouse está sendo iniciada.</span><span class="sxs-lookup"><span data-stu-id="8373c-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="8373c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8373c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8373c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8373c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8373c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8373c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8373c-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="8373c-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="8373c-111">O membro **iItem** identifica o item que está sendo arrastado e os outros membros são zero.</span><span class="sxs-lookup"><span data-stu-id="8373c-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8373c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8373c-112">Return value</span></span>

<span data-ttu-id="8373c-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8373c-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8373c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8373c-114">Requirements</span></span>



| <span data-ttu-id="8373c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8373c-115">Requirement</span></span> | <span data-ttu-id="8373c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8373c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8373c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8373c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8373c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8373c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8373c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8373c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8373c-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8373c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8373c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8373c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8373c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8373c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





