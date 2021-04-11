---
title: Mensagem de BM_GETIMAGE (WinUser. h)
description: Recupera um identificador para a imagem (ícone ou bitmap) associado ao botão.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Controles de BM_GETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295842"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="0db10-104">\_Mensagem BM GETimage</span><span class="sxs-lookup"><span data-stu-id="0db10-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="0db10-105">Recupera um identificador para a imagem (ícone ou bitmap) associado ao botão.</span><span class="sxs-lookup"><span data-stu-id="0db10-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="0db10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0db10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db10-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0db10-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0db10-108">O tipo de imagem a ser associado ao botão.</span><span class="sxs-lookup"><span data-stu-id="0db10-108">The type of image to associate with the button.</span></span> <span data-ttu-id="0db10-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0db10-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0db10-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0db10-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="0db10-111">Significado</span><span class="sxs-lookup"><span data-stu-id="0db10-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="0db10-112"><dt>**BITMAP de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db10-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="0db10-113">Um bitmap.</span><span class="sxs-lookup"><span data-stu-id="0db10-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="0db10-114"><dt>**ícone de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db10-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="0db10-115">Um ícone.</span><span class="sxs-lookup"><span data-stu-id="0db10-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="0db10-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0db10-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0db10-117">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="0db10-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db10-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0db10-118">Return value</span></span>

<span data-ttu-id="0db10-119">O valor de retorno é um identificador para a imagem, se houver; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0db10-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db10-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db10-120">Requirements</span></span>



| <span data-ttu-id="0db10-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db10-121">Requirement</span></span> | <span data-ttu-id="0db10-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0db10-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db10-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0db10-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0db10-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0db10-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0db10-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0db10-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0db10-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0db10-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0db10-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0db10-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db10-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0db10-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db10-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0db10-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0db10-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0db10-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0db10-131">**BM \_ SETimage**</span><span class="sxs-lookup"><span data-stu-id="0db10-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="0db10-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0db10-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0db10-133">Botões</span><span class="sxs-lookup"><span data-stu-id="0db10-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





