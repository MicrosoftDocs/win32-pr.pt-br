---
title: Mensagem de TBM_SETTOOLTIPS (commctrl. h)
description: Atribui um controle ToolTip a um controle TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- Controles de TBM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454877"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="a75fe-104">\_Mensagem tbm SETtooltips</span><span class="sxs-lookup"><span data-stu-id="a75fe-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="a75fe-105">Atribui um controle ToolTip a um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a75fe-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a75fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a75fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a75fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a75fe-108">Identificador para um controle ToolTip existente.</span><span class="sxs-lookup"><span data-stu-id="a75fe-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="a75fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a75fe-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a75fe-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a75fe-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a75fe-111">Return value</span></span>

<span data-ttu-id="a75fe-112">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="a75fe-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75fe-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a75fe-113">Remarks</span></span>

<span data-ttu-id="a75fe-114">Quando um controle TrackBar é criado com o estilo de [**\_ dicas de ferramenta TBS**](trackbar-control-styles.md) , ele cria um controle ToolTip padrão que aparece ao lado do controle deslizante, exibindo a posição atual do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="a75fe-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75fe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a75fe-115">Requirements</span></span>



| <span data-ttu-id="a75fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75fe-116">Requirement</span></span> | <span data-ttu-id="a75fe-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a75fe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a75fe-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a75fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a75fe-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a75fe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a75fe-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a75fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a75fe-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a75fe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a75fe-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a75fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75fe-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75fe-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





