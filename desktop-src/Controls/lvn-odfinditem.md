---
title: Mensagem de LVN_ODFINDITEM (commctrl. h)
description: Enviado por um controle de exibição de lista virtual quando ele precisa que o proprietário encontre um item de retorno de chamada específico.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Controles de LVN_ODFINDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085933"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="45fd1-104">\_Mensagem LVN ODFINDITEM</span><span class="sxs-lookup"><span data-stu-id="45fd1-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="45fd1-105">Enviado por um controle de [exibição de lista virtual](list-view-controls-overview.md) quando ele precisa que o proprietário encontre um item de retorno de chamada específico.</span><span class="sxs-lookup"><span data-stu-id="45fd1-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="45fd1-106">Por exemplo, o controle enviará esse código de notificação quando receber a entrada de teclado de atalho ou quando receber uma mensagem [**LVM \_ FINDITEM**](lvm-finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="45fd1-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="45fd1-107">O \_ código de notificação LVN ODFINDITEM é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="45fd1-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="45fd1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45fd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fd1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45fd1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45fd1-110">Ponteiro para uma estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que inclui informações a serem usadas para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="45fd1-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fd1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45fd1-111">Return value</span></span>

<span data-ttu-id="45fd1-112">Retorna o índice do item encontrado ou-1 se nenhum item for encontrado.</span><span class="sxs-lookup"><span data-stu-id="45fd1-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="45fd1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="45fd1-113">Remarks</span></span>

<span data-ttu-id="45fd1-114">As informações de pesquisa são enviadas na forma de uma estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , que é membro da estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="45fd1-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fd1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45fd1-115">Requirements</span></span>



| <span data-ttu-id="45fd1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fd1-116">Requirement</span></span> | <span data-ttu-id="45fd1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="45fd1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45fd1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45fd1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45fd1-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45fd1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45fd1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45fd1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45fd1-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45fd1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45fd1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45fd1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45fd1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45fd1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="45fd1-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="45fd1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="45fd1-125">**LVN \_ ODFINDITEMW** (Unicode) e **LVN \_ ODFINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="45fd1-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





