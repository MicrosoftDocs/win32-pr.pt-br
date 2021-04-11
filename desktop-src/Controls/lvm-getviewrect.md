---
title: Mensagem de LVM_GETVIEWRECT (commctrl. h)
description: Recupera o retângulo delimitador de todos os itens no controle de exibição de lista. O modo de exibição de lista deve estar no ícone ou no modo de exibição de ícone pequeno. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetViewRect do ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Controles de LVM_GETVIEWRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009646"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="2c918-106">\_Mensagem GETVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="2c918-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="2c918-107">Recupera o retângulo delimitador de todos os itens no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="2c918-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="2c918-108">O modo de exibição de lista deve estar no ícone ou no modo de exibição de ícone pequeno.</span><span class="sxs-lookup"><span data-stu-id="2c918-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="2c918-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetViewRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .</span><span class="sxs-lookup"><span data-stu-id="2c918-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c918-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c918-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c918-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c918-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c918-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2c918-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2c918-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c918-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c918-114">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2c918-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="2c918-115">Todas as coordenadas são relativas à área visível do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="2c918-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c918-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c918-116">Return value</span></span>

<span data-ttu-id="2c918-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2c918-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c918-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c918-118">Requirements</span></span>



| <span data-ttu-id="2c918-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c918-119">Requirement</span></span> | <span data-ttu-id="2c918-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2c918-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c918-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c918-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c918-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c918-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c918-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c918-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c918-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c918-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c918-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c918-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c918-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c918-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

