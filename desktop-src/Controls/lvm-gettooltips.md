---
title: Mensagem de LVM_GETTOOLTIPS (commctrl. h)
description: Recupera o controle ToolTip que o controle List-View usa para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetToolTips do ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Controles de LVM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455744"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="89235-105">Mensagem do LVM \_ GETtooltips</span><span class="sxs-lookup"><span data-stu-id="89235-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="89235-106">Recupera o controle ToolTip que o controle List-View usa para exibir dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="89235-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="89235-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetToolTips do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="89235-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89235-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89235-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89235-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89235-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="89235-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89235-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89235-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="89235-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="89235-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89235-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89235-113">Return value</span></span>

<span data-ttu-id="89235-114">Retorna o identificador do controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="89235-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="89235-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89235-115">Requirements</span></span>



| <span data-ttu-id="89235-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89235-116">Requirement</span></span> | <span data-ttu-id="89235-117">Valor</span><span class="sxs-lookup"><span data-stu-id="89235-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89235-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89235-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89235-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89235-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89235-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89235-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89235-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89235-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89235-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89235-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89235-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89235-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89235-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="89235-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89235-125">**autotooltips do LVM \_**</span><span class="sxs-lookup"><span data-stu-id="89235-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





