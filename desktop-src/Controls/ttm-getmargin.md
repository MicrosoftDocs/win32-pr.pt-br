---
title: Mensagem de TTM_GETMARGIN (commctrl. h)
description: Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Controles de TTM_GETMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918470"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="d8b85-105">Mensagem do TTM \_ GETmargin</span><span class="sxs-lookup"><span data-stu-id="d8b85-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="d8b85-106">Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d8b85-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="d8b85-107">Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d8b85-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8b85-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8b85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8b85-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d8b85-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d8b85-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d8b85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8b85-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8b85-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as informações de margem.</span><span class="sxs-lookup"><span data-stu-id="d8b85-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="d8b85-113">Os membros da estrutura **Rect** não definem um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="d8b85-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="d8b85-114">Para fins desta mensagem, os membros da estrutura são interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d8b85-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="d8b85-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d8b85-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="d8b85-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d8b85-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="d8b85-117"><dt>**Início**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b85-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="d8b85-118">Distância entre a borda superior e a parte superior do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d8b85-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="d8b85-119"><dt>**mantida**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b85-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="d8b85-120">Distância entre a borda esquerda e a extremidade esquerda do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d8b85-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="d8b85-121"><dt>**resultado**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b85-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="d8b85-122">Distância entre a borda inferior e a parte inferior do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d8b85-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="d8b85-123"><dt>**Certo**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b85-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="d8b85-124">Distância entre a borda direita e a extremidade direita do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d8b85-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b85-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8b85-125">Return value</span></span>

<span data-ttu-id="d8b85-126">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="d8b85-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b85-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8b85-127">Remarks</span></span>

<span data-ttu-id="d8b85-128">Todas as quatro margens assumem o padrão de zero quando você cria o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d8b85-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b85-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8b85-129">Requirements</span></span>



| <span data-ttu-id="d8b85-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b85-130">Requirement</span></span> | <span data-ttu-id="d8b85-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d8b85-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b85-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b85-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b85-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8b85-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8b85-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b85-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b85-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8b85-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8b85-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8b85-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b85-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b85-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b85-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8b85-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b85-139">**TTM \_ SETmargin**</span><span class="sxs-lookup"><span data-stu-id="d8b85-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

