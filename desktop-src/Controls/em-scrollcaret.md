---
title: Mensagem de EM_SCROLLCARET (WinUser. h)
description: Rola o cursor para a exibição em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- Controles de EM_SCROLLCARET de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086417"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="8ff79-105">\_Mensagem em SCROLLCARET</span><span class="sxs-lookup"><span data-stu-id="8ff79-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="8ff79-106">Rola o cursor para a exibição em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8ff79-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="8ff79-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="8ff79-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ff79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ff79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ff79-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff79-110">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="8ff79-110">This parameter is reserved.</span></span> <span data-ttu-id="8ff79-111">Ele deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8ff79-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ff79-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ff79-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff79-113">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="8ff79-113">This parameter is reserved.</span></span> <span data-ttu-id="8ff79-114">Ele deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8ff79-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff79-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ff79-115">Return value</span></span>

<span data-ttu-id="8ff79-116">O valor de retorno não é significativo.</span><span class="sxs-lookup"><span data-stu-id="8ff79-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff79-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ff79-117">Remarks</span></span>

<span data-ttu-id="8ff79-118">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="8ff79-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8ff79-119">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8ff79-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff79-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ff79-120">Requirements</span></span>



| <span data-ttu-id="8ff79-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ff79-121">Requirement</span></span> | <span data-ttu-id="8ff79-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8ff79-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff79-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ff79-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff79-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ff79-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ff79-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ff79-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff79-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ff79-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ff79-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ff79-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff79-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff79-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff79-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ff79-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ff79-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8ff79-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ff79-131">**em \_ LINESCROLL**</span><span class="sxs-lookup"><span data-stu-id="8ff79-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="8ff79-132">**\_rolagem em**</span><span class="sxs-lookup"><span data-stu-id="8ff79-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="8ff79-133">**VSCROLL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8ff79-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





