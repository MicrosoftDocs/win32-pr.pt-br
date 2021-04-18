---
title: Mensagem de TTM_SETMARGIN (commctrl. h)
description: Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Controles de TTM_SETMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751300"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="eed34-105">\_Mensagem TTM SETmargin</span><span class="sxs-lookup"><span data-stu-id="eed34-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="eed34-106">Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="eed34-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="eed34-107">Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="eed34-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="eed34-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed34-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eed34-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eed34-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="eed34-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eed34-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eed34-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eed34-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as informações de margem a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="eed34-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="eed34-113">Os membros da estrutura **Rect** não definem um retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="eed34-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="eed34-114">Para fins desta mensagem, os membros da estrutura são interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="eed34-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="eed34-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eed34-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="eed34-116">Significado</span><span class="sxs-lookup"><span data-stu-id="eed34-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="eed34-117"><dt>**Início**</dt></span><span class="sxs-lookup"><span data-stu-id="eed34-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="eed34-118">Distância entre a borda superior e a parte superior do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eed34-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="eed34-119"><dt>**mantida**</dt></span><span class="sxs-lookup"><span data-stu-id="eed34-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="eed34-120">Distância entre a borda esquerda e a extremidade esquerda do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eed34-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="eed34-121"><dt>**resultado**</dt></span><span class="sxs-lookup"><span data-stu-id="eed34-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="eed34-122">Distância entre a borda inferior e a parte inferior do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eed34-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="eed34-123"><dt>**Certo**</dt></span><span class="sxs-lookup"><span data-stu-id="eed34-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="eed34-124">Distância entre a borda direita e a extremidade direita do texto da dica de ferramenta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eed34-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed34-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eed34-125">Return value</span></span>

<span data-ttu-id="eed34-126">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="eed34-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed34-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed34-127">Remarks</span></span>

<span data-ttu-id="eed34-128">Esta mensagem não tem efeito quando o aplicativo é executado no Windows Vista e os estilos visuais estão habilitados para a dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="eed34-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="eed34-129">Você pode desabilitar estilos visuais para a dica de ferramenta usando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span><span class="sxs-lookup"><span data-stu-id="eed34-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="eed34-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed34-130">Requirements</span></span>



| <span data-ttu-id="eed34-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed34-131">Requirement</span></span> | <span data-ttu-id="eed34-132">Valor</span><span class="sxs-lookup"><span data-stu-id="eed34-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eed34-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed34-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eed34-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eed34-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eed34-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eed34-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eed34-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eed34-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eed34-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eed34-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed34-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed34-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed34-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed34-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed34-140">**GetMargin TTM \_**</span><span class="sxs-lookup"><span data-stu-id="eed34-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

