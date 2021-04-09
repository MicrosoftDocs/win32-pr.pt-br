---
title: Mensagem de TTM_TRACKPOSITION (commctrl. h)
description: Define a posição de uma dica de ferramenta de rastreamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Controles de TTM_TRACKPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009519"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="b2192-104">\_Mensagem TTM TRACKPOSITION</span><span class="sxs-lookup"><span data-stu-id="b2192-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="b2192-105">Define a posição de uma dica de ferramenta de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b2192-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2192-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2192-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2192-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2192-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2192-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b2192-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b2192-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2192-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2192-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a coordenada x do ponto no qual a dica de ferramenta de rastreamento será exibida, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="b2192-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="b2192-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a coordenada y do ponto no qual a dica de ferramenta de rastreamento será exibida, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="b2192-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2192-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2192-112">Return value</span></span>

<span data-ttu-id="b2192-113">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="b2192-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2192-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2192-114">Remarks</span></span>

<span data-ttu-id="b2192-115">O controle ToolTip escolhe onde exibir a janela de dica de ferramenta com base nas coordenadas fornecidas com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="b2192-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="b2192-116">Isso faz com que a janela ToolTip apareça ao lado da ferramenta à qual ela corresponde.</span><span class="sxs-lookup"><span data-stu-id="b2192-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="b2192-117">Para que as janelas de dica de ferramenta sejam exibidas em coordenadas específicas, inclua o sinalizador de TTF \_ Absolute no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ao adicionar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="b2192-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2192-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2192-118">Requirements</span></span>



| <span data-ttu-id="b2192-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2192-119">Requirement</span></span> | <span data-ttu-id="b2192-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b2192-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2192-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2192-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b2192-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2192-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2192-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2192-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b2192-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2192-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2192-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2192-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2192-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2192-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2192-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2192-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2192-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b2192-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2192-129">**TTM \_ TRACKACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="b2192-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="b2192-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b2192-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2192-131">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="b2192-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

