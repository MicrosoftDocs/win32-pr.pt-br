---
title: Mensagem de EM_HIDEBALLOONTIP (commctrl. h)
description: Oculta qualquer dica de balão associada a um controle de edição.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- Controles de EM_HIDEBALLOONTIP de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918062"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="01521-104">\_Mensagem em HIDEBALLOONTIP</span><span class="sxs-lookup"><span data-stu-id="01521-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="01521-105">Oculta qualquer dica de balão associada a um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="01521-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01521-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01521-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01521-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01521-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01521-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="01521-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="01521-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01521-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01521-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="01521-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01521-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01521-111">Return value</span></span>

<span data-ttu-id="01521-112">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="01521-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="01521-113">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="01521-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="01521-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="01521-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01521-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="01521-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="01521-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="01521-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01521-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01521-117">Requirements</span></span>



| <span data-ttu-id="01521-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01521-118">Requirement</span></span> | <span data-ttu-id="01521-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01521-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01521-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01521-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01521-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01521-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01521-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01521-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01521-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01521-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01521-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01521-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01521-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01521-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01521-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="01521-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01521-127">**Editar \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="01521-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





