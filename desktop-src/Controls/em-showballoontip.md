---
title: Mensagem de EM_SHOWBALLOONTIP (commctrl. h)
description: A \_ mensagem em SHOWBALLOONTIP exibe uma dica de balão associada a um controle de edição.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Controles de EM_SHOWBALLOONTIP de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085731"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="d0ce1-104">\_Mensagem em SHOWBALLOONTIP</span><span class="sxs-lookup"><span data-stu-id="d0ce1-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="d0ce1-105">A mensagem em **\_ SHOWBALLOONTIP** exibe uma dica de balão associada a um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0ce1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0ce1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ce1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0ce1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ce1-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0ce1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0ce1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ce1-110">Um ponteiro para uma estrutura [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) que contém informações sobre a dica de balão a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ce1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0ce1-111">Return value</span></span>

<span data-ttu-id="d0ce1-112">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="d0ce1-113">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ce1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0ce1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0ce1-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="d0ce1-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d0ce1-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0ce1-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0ce1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ce1-117">Requirements</span></span>



| <span data-ttu-id="d0ce1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ce1-118">Requirement</span></span> | <span data-ttu-id="d0ce1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ce1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ce1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0ce1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ce1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0ce1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0ce1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0ce1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ce1-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0ce1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0ce1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0ce1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ce1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ce1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ce1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0ce1-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d0ce1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0ce1-128">**EDITBALLOONTIP**</span><span class="sxs-lookup"><span data-stu-id="d0ce1-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="d0ce1-129">**Editar \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="d0ce1-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





