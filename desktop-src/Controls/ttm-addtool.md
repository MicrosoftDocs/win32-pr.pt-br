---
title: Mensagem de TTM_ADDTOOL (commctrl. h)
description: Registra uma ferramenta com um controle ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Controles de TTM_ADDTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755419"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="68a41-104">\_Mensagem ADDFERRAMENTA TTM</span><span class="sxs-lookup"><span data-stu-id="68a41-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="68a41-105">Registra uma ferramenta com um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="68a41-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="68a41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68a41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68a41-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="68a41-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="68a41-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="68a41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68a41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68a41-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que contém informações que o controle ToolTip precisa para exibir o texto da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="68a41-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="68a41-111">O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="68a41-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a41-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68a41-112">Return value</span></span>

<span data-ttu-id="68a41-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="68a41-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a41-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68a41-114">Requirements</span></span>



| <span data-ttu-id="68a41-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a41-115">Requirement</span></span> | <span data-ttu-id="68a41-116">Valor</span><span class="sxs-lookup"><span data-stu-id="68a41-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68a41-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68a41-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68a41-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68a41-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68a41-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68a41-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68a41-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68a41-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68a41-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68a41-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a41-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a41-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="68a41-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="68a41-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="68a41-124">**TTM \_ ADDTOOLW** (Unicode) e **TTM \_ addferramentaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="68a41-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="68a41-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a41-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="68a41-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="68a41-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68a41-127">**TTM \_ DELTOOL**</span><span class="sxs-lookup"><span data-stu-id="68a41-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="68a41-128">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="68a41-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68a41-129">Sobre os controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="68a41-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





