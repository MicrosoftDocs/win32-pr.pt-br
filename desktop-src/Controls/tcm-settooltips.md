---
title: Mensagem de TCM_SETTOOLTIPS (commctrl. h)
description: Atribui um controle ToolTip a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetToolTips do TabCtrl.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Controles de TCM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644242"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="ab19e-105">Mensagem do TCM \_ SETtooltips</span><span class="sxs-lookup"><span data-stu-id="ab19e-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="ab19e-106">Atribui um controle ToolTip a um controle guia.</span><span class="sxs-lookup"><span data-stu-id="ab19e-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="ab19e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetToolTips do TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="ab19e-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab19e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab19e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab19e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab19e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab19e-110">Identificador para o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="ab19e-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="ab19e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab19e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ab19e-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ab19e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab19e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab19e-113">Return value</span></span>

<span data-ttu-id="ab19e-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ab19e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab19e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab19e-115">Remarks</span></span>

<span data-ttu-id="ab19e-116">Você pode recuperar o controle de dica de ferramenta associado a um controle guia usando a mensagem [**TCM \_ GetToolTips**](tcm-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="ab19e-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab19e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab19e-117">Requirements</span></span>



| <span data-ttu-id="ab19e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab19e-118">Requirement</span></span> | <span data-ttu-id="ab19e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ab19e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab19e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab19e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab19e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab19e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab19e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab19e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab19e-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab19e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab19e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab19e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab19e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab19e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





