---
title: Mensagem de BCM_SETTEXTMARGIN (commctrl. h)
description: A \_ mensagem SETTEXTMARGIN do BCM define as margens para o texto de desenho em um controle de botão.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- Controles de BCM_SETTEXTMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455127"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="6cb0e-104">\_Mensagem SETTEXTMARGIN do BCM</span><span class="sxs-lookup"><span data-stu-id="6cb0e-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="6cb0e-105">A **mensagem \_ SETTEXTMARGIN do BCM** define as margens para o texto de desenho em um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cb0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cb0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb0e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cb0e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb0e-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6cb0e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cb0e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb0e-110">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica as margens a serem usadas para desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb0e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cb0e-111">Return value</span></span>

<span data-ttu-id="6cb0e-112">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="6cb0e-113">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb0e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cb0e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6cb0e-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6cb0e-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6cb0e-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6cb0e-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6cb0e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb0e-117">Requirements</span></span>



| <span data-ttu-id="6cb0e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb0e-118">Requirement</span></span> | <span data-ttu-id="6cb0e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb0e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb0e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb0e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cb0e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cb0e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb0e-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cb0e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cb0e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cb0e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb0e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb0e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb0e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cb0e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6cb0e-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6cb0e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6cb0e-128">**Botão \_ SetTextMargin**</span><span class="sxs-lookup"><span data-stu-id="6cb0e-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="6cb0e-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6cb0e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6cb0e-130">Botões</span><span class="sxs-lookup"><span data-stu-id="6cb0e-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

