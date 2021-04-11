---
title: Mensagem de TCM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle de dica de ferramenta associado a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetToolTips TabCtrl.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Controles de TCM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086241"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="183d3-105">Mensagem do TCM \_ GETtooltips</span><span class="sxs-lookup"><span data-stu-id="183d3-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="183d3-106">Recupera o identificador para o controle de dica de ferramenta associado a um controle guia.</span><span class="sxs-lookup"><span data-stu-id="183d3-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="183d3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetToolTips TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="183d3-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="183d3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="183d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="183d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="183d3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="183d3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="183d3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="183d3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="183d3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="183d3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="183d3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="183d3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="183d3-113">Return value</span></span>

<span data-ttu-id="183d3-114">Retorna o identificador para o controle de dica de ferramenta se for bem-sucedido ou **NULL** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="183d3-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="183d3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="183d3-115">Remarks</span></span>

<span data-ttu-id="183d3-116">Um controle guia cria um controle ToolTip se ele tiver o estilo de [**\_ Tooltips de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="183d3-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="183d3-117">Você também pode atribuir um controle de dica de ferramenta a um controle guia usando a mensagem [**TCM \_ SetToolTips**](tcm-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="183d3-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="183d3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="183d3-118">Requirements</span></span>



| <span data-ttu-id="183d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="183d3-119">Requirement</span></span> | <span data-ttu-id="183d3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="183d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="183d3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="183d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="183d3-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="183d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="183d3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="183d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="183d3-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="183d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="183d3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="183d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="183d3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="183d3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





