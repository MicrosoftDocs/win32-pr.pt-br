---
title: Mensagem de LVM_SETTOOLTIPS (commctrl. h)
description: Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Controles de LVM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454932"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="313ad-105">Mensagem do LVM \_ SETtooltips</span><span class="sxs-lookup"><span data-stu-id="313ad-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="313ad-106">Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="313ad-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="313ad-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="313ad-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="313ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="313ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="313ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="313ad-110">Identificador para o controle de dica de ferramenta a ser definido.</span><span class="sxs-lookup"><span data-stu-id="313ad-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="313ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="313ad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313ad-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="313ad-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313ad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="313ad-113">Return value</span></span>

<span data-ttu-id="313ad-114">Retorna o identificador para o controle ToolTip anterior.</span><span class="sxs-lookup"><span data-stu-id="313ad-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="313ad-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313ad-115">Requirements</span></span>



| <span data-ttu-id="313ad-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="313ad-116">Requirement</span></span> | <span data-ttu-id="313ad-117">Valor</span><span class="sxs-lookup"><span data-stu-id="313ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313ad-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="313ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="313ad-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="313ad-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="313ad-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="313ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="313ad-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="313ad-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="313ad-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="313ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="313ad-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313ad-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="313ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313ad-125">**LVM \_ GETtooltips**</span><span class="sxs-lookup"><span data-stu-id="313ad-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





