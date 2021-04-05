---
title: Mensagem de EM_SETZOOM (RichEdit. h)
description: Define a taxa de zoom. A proporção deve ser um valor entre 1/64 e 64. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Controles de EM_SETZOOM de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824523"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="32022-106">\_Mensagem em SETzoom</span><span class="sxs-lookup"><span data-stu-id="32022-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="32022-107">Define a taxa de zoom para um controle de edição de várias linhas ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="32022-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="32022-108">A proporção deve ser um valor entre 1/64 e 64.</span><span class="sxs-lookup"><span data-stu-id="32022-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="32022-109">O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="32022-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="32022-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32022-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32022-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32022-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32022-112">Numerador da taxa de zoom.</span><span class="sxs-lookup"><span data-stu-id="32022-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="32022-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32022-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32022-114">O denominador da taxa de zoom.</span><span class="sxs-lookup"><span data-stu-id="32022-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="32022-115">Esses parâmetros podem ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="32022-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="32022-116">Valor</span><span class="sxs-lookup"><span data-stu-id="32022-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="32022-117">Significado</span><span class="sxs-lookup"><span data-stu-id="32022-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="32022-118"><dt>**Ambos 0**</dt></span><span class="sxs-lookup"><span data-stu-id="32022-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="32022-119">Desativa o zoom usando a mensagem em **\_ setZoom** (o zoom ainda pode ocorrer usando [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span><span class="sxs-lookup"><span data-stu-id="32022-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="32022-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="32022-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="32022-121">Amplia a exibição pelo numerador/denominador da taxa de zoom</span><span class="sxs-lookup"><span data-stu-id="32022-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32022-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32022-122">Return value</span></span>

<span data-ttu-id="32022-123">Se a nova configuração de zoom for aceita, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="32022-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="32022-124">Se a nova configuração de zoom não for aceita, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="32022-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32022-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="32022-125">Remarks</span></span>

<span data-ttu-id="32022-126">**Editar:** Com suporte no Windows 10 1809 e posterior.</span><span class="sxs-lookup"><span data-stu-id="32022-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="32022-127">O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="32022-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="32022-128">Para obter informações sobre o controle de edição, consulte [Editar controles](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="32022-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32022-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32022-129">Requirements</span></span>



| <span data-ttu-id="32022-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="32022-130">Requirement</span></span> | <span data-ttu-id="32022-131">Valor</span><span class="sxs-lookup"><span data-stu-id="32022-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32022-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32022-132">Minimum supported client</span></span><br/> | <span data-ttu-id="32022-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32022-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32022-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32022-134">Minimum supported server</span></span><br/> | <span data-ttu-id="32022-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32022-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32022-136">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="32022-136">Redistributable</span></span><br/>          | <span data-ttu-id="32022-137">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="32022-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="32022-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32022-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="32022-139"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32022-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32022-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="32022-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32022-141">**em \_ GETzoom**</span><span class="sxs-lookup"><span data-stu-id="32022-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





