---
title: Mensagem de TBM_SETTIPSIDE (commctrl. h)
description: Posiciona um controle ToolTip usado por um controle TrackBar. Os controles TrackBar que usam o \_ estilo de dicas de ferramenta TBS exibem dicas de ferramenta.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Controles de TBM_SETTIPSIDE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369418"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="d05d8-105">\_Mensagem tbm SETTIPSIDE</span><span class="sxs-lookup"><span data-stu-id="d05d8-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="d05d8-106">Posiciona um controle ToolTip usado por um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d05d8-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="d05d8-107">Os controles TrackBar que usam o estilo de [**\_ dicas de ferramenta TBS**](trackbar-control-styles.md) exibem dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d05d8-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="d05d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d05d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05d8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d05d8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d05d8-110">Valor que representa o local no qual exibir o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d05d8-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="d05d8-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d05d8-111">This value can be one of the following:</span></span>



| <span data-ttu-id="d05d8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d05d8-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d05d8-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d05d8-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="d05d8-114"><dt>**TBTS \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="d05d8-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="d05d8-115">O controle ToolTip será posicionado acima do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d05d8-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="d05d8-116">Esse sinalizador é para uso com trackbars horizontais.</span><span class="sxs-lookup"><span data-stu-id="d05d8-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="d05d8-117"><dt>**TBTS \_ à esquerda**</dt></span><span class="sxs-lookup"><span data-stu-id="d05d8-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="d05d8-118">O controle ToolTip será posicionado à esquerda do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d05d8-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="d05d8-119">Esse sinalizador é para uso com trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="d05d8-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="d05d8-120"><dt>**TBTS \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="d05d8-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="d05d8-121">O controle ToolTip será posicionado abaixo do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d05d8-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="d05d8-122">Esse sinalizador é para uso com trackbars horizontais.</span><span class="sxs-lookup"><span data-stu-id="d05d8-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="d05d8-123"><dt>**TBTS \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="d05d8-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="d05d8-124">O controle ToolTip será posicionado à direita do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d05d8-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="d05d8-125">Esse sinalizador é para uso com trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="d05d8-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d05d8-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d05d8-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d05d8-127">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d05d8-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05d8-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d05d8-128">Return value</span></span>

<span data-ttu-id="d05d8-129">Retorna um valor que representa o local anterior do controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d05d8-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="d05d8-130">O valor de retorno é igual a um dos valores possíveis para *wParam*.</span><span class="sxs-lookup"><span data-stu-id="d05d8-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05d8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d05d8-131">Requirements</span></span>



| <span data-ttu-id="d05d8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d05d8-132">Requirement</span></span> | <span data-ttu-id="d05d8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d05d8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d05d8-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d05d8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d05d8-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d05d8-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d05d8-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d05d8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d05d8-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d05d8-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d05d8-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d05d8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d05d8-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d05d8-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





