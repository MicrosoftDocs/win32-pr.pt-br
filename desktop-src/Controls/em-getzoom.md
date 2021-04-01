---
title: Mensagem de EM_GETZOOM (RichEdit. h)
description: Obtém a taxa de zoom atual. O ração de zoom sempre está entre 1/64 e 64. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Controles de EM_GETZOOM de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644348"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="3085e-106">\_Mensagem em GETzoom</span><span class="sxs-lookup"><span data-stu-id="3085e-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="3085e-107">Obtém a taxa de zoom atual para um controle de edição de várias linhas ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="3085e-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="3085e-108">O ração de zoom sempre está entre 1/64 e 64.</span><span class="sxs-lookup"><span data-stu-id="3085e-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="3085e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3085e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3085e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3085e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3085e-111">Recebe o numerador da taxa de zoom.</span><span class="sxs-lookup"><span data-stu-id="3085e-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="3085e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3085e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3085e-113">Recebe o denominador da taxa de zoom.</span><span class="sxs-lookup"><span data-stu-id="3085e-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3085e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3085e-114">Return value</span></span>

<span data-ttu-id="3085e-115">A mensagem retornará **true** se a mensagem for processada, que será se *wParam* e *lParam* não forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="3085e-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3085e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3085e-116">Remarks</span></span>

<span data-ttu-id="3085e-117">**Editar:** Com suporte no Windows 10 1809 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3085e-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="3085e-118">O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="3085e-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="3085e-119">Para obter informações sobre o controle de edição, consulte [Editar controles](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="3085e-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3085e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3085e-120">Requirements</span></span>



| <span data-ttu-id="3085e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3085e-121">Requirement</span></span> | <span data-ttu-id="3085e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3085e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3085e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3085e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3085e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3085e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3085e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3085e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3085e-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3085e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3085e-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3085e-127">Redistributable</span></span><br/>          | <span data-ttu-id="3085e-128">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="3085e-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="3085e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3085e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3085e-130"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3085e-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3085e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3085e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3085e-132">**em \_ SETzoom**</span><span class="sxs-lookup"><span data-stu-id="3085e-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





