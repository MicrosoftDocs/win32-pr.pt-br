---
title: Mensagem de EM_GETRECT (WinUser. h)
description: Obtém o retângulo de formatação de um controle de edição.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Controles de EM_GETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824475"
---
# <a name="em_getrect-message"></a><span data-ttu-id="959d8-104">\_Mensagem em GETrect</span><span class="sxs-lookup"><span data-stu-id="959d8-104">EM\_GETRECT message</span></span>

<span data-ttu-id="959d8-105">Obtém o [retângulo de formatação](about-edit-controls.md) de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="959d8-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="959d8-106">O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto.</span><span class="sxs-lookup"><span data-stu-id="959d8-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="959d8-107">O retângulo de limitação é independente do tamanho da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="959d8-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="959d8-108">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="959d8-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="959d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="959d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959d8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="959d8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="959d8-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="959d8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="959d8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="959d8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="959d8-113">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo de formatação.</span><span class="sxs-lookup"><span data-stu-id="959d8-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959d8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="959d8-114">Return value</span></span>

<span data-ttu-id="959d8-115">O valor de retorno não é significativo.</span><span class="sxs-lookup"><span data-stu-id="959d8-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="959d8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="959d8-116">Remarks</span></span>

<span data-ttu-id="959d8-117">Você pode modificar o retângulo de formatação de um controle de edição de várias linhas usando as mensagens [**em \_ SETRECTNP**](em-setrectnp.md) [**\_ SetRect**](em-setrect.md) e em.</span><span class="sxs-lookup"><span data-stu-id="959d8-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="959d8-118">Em determinadas condições, **em \_ GetRect** pode não retornar os valores exatos que em [**\_ SetRect**](em-setrect.md) ou em [**\_ SETRECTNP**](em-setrectnp.md) defini-lo será aproximadamente correto, mas pode ser desativado por alguns pixels.</span><span class="sxs-lookup"><span data-stu-id="959d8-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="959d8-119">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="959d8-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="959d8-120">O retângulo de formatação não inclui a barra de seleção, que é uma área desmarcada à esquerda de cada parágrafo.</span><span class="sxs-lookup"><span data-stu-id="959d8-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="959d8-121">Quando clicado, a barra de seleção seleciona a linha.</span><span class="sxs-lookup"><span data-stu-id="959d8-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="959d8-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="959d8-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="959d8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="959d8-123">Requirements</span></span>



| <span data-ttu-id="959d8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="959d8-124">Requirement</span></span> | <span data-ttu-id="959d8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="959d8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959d8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="959d8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="959d8-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="959d8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="959d8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="959d8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="959d8-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="959d8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="959d8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="959d8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="959d8-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="959d8-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="959d8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="959d8-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="959d8-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="959d8-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="959d8-134">**em \_ SETrect**</span><span class="sxs-lookup"><span data-stu-id="959d8-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="959d8-135">**em \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="959d8-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="959d8-136">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="959d8-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="959d8-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="959d8-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

