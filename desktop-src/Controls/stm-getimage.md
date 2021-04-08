---
title: Mensagem de STM_GETIMAGE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem STM GetImage para recuperar um identificador para a imagem (ícone ou bitmap) associado a um controle estático.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Controles de STM_GETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008921"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="bdacf-104">\_Mensagem de GETIMAGE STM</span><span class="sxs-lookup"><span data-stu-id="bdacf-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="bdacf-105">Um aplicativo envia uma mensagem **STM \_ GetImage** para recuperar um identificador para a imagem (ícone ou bitmap) associado a um controle estático.</span><span class="sxs-lookup"><span data-stu-id="bdacf-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdacf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdacf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdacf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdacf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdacf-108">Especifica o tipo de imagem a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bdacf-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="bdacf-109">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bdacf-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="bdacf-110">Valor</span><span class="sxs-lookup"><span data-stu-id="bdacf-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="bdacf-111">Significado</span><span class="sxs-lookup"><span data-stu-id="bdacf-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="bdacf-112"><dt>**BITMAP de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bdacf-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="bdacf-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="bdacf-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="bdacf-114"><dt>**CURSOR de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bdacf-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="bdacf-115">Posição.</span><span class="sxs-lookup"><span data-stu-id="bdacf-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="bdacf-116"><dt>**ENHMETAFILE de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bdacf-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="bdacf-117">Metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="bdacf-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="bdacf-118"><dt>**ícone de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bdacf-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="bdacf-119">Cone.</span><span class="sxs-lookup"><span data-stu-id="bdacf-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="bdacf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdacf-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdacf-121">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="bdacf-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdacf-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdacf-122">Return value</span></span>

<span data-ttu-id="bdacf-123">O valor de retorno é um identificador para a imagem, se houver; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bdacf-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdacf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdacf-124">Requirements</span></span>



| <span data-ttu-id="bdacf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdacf-125">Requirement</span></span> | <span data-ttu-id="bdacf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bdacf-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdacf-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdacf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bdacf-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdacf-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdacf-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdacf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bdacf-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdacf-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdacf-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdacf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdacf-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdacf-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdacf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdacf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdacf-134">**\_imagem STM**</span><span class="sxs-lookup"><span data-stu-id="bdacf-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





