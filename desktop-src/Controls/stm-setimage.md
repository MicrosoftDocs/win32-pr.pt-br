---
title: Mensagem de STM_SETIMAGE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem STM SetImage para associar uma nova imagem a um controle estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Controles de STM_SETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918118"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="32ebe-104">\_Mensagem de imagem STM</span><span class="sxs-lookup"><span data-stu-id="32ebe-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="32ebe-105">Um aplicativo envia uma mensagem **STM \_ SetImage** para associar uma nova imagem a um controle estático.</span><span class="sxs-lookup"><span data-stu-id="32ebe-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="32ebe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32ebe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ebe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ebe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ebe-108">Especifica o tipo de imagem a ser associado ao controle estático.</span><span class="sxs-lookup"><span data-stu-id="32ebe-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="32ebe-109">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="32ebe-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="32ebe-110">Valor</span><span class="sxs-lookup"><span data-stu-id="32ebe-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="32ebe-111">Significado</span><span class="sxs-lookup"><span data-stu-id="32ebe-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="32ebe-112"><dt>**BITMAP de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32ebe-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="32ebe-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="32ebe-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="32ebe-114"><dt>**CURSOR de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32ebe-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="32ebe-115">Posição.</span><span class="sxs-lookup"><span data-stu-id="32ebe-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="32ebe-116"><dt>**ENHMETAFILE de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32ebe-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="32ebe-117">Metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="32ebe-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="32ebe-118"><dt>**ícone de imagem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32ebe-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="32ebe-119">Cone.</span><span class="sxs-lookup"><span data-stu-id="32ebe-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="32ebe-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ebe-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ebe-121">Manipule a imagem a ser associada ao controle estático.</span><span class="sxs-lookup"><span data-stu-id="32ebe-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ebe-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32ebe-122">Return value</span></span>

<span data-ttu-id="32ebe-123">O valor de retorno é um identificador para a imagem associada anteriormente ao controle estático, se houver; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="32ebe-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ebe-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ebe-124">Remarks</span></span>

<span data-ttu-id="32ebe-125">Para associar uma imagem a um controle estático, o controle deve ter o estilo adequado.</span><span class="sxs-lookup"><span data-stu-id="32ebe-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="32ebe-126">A tabela a seguir mostra o estilo necessário para cada tipo de imagem.</span><span class="sxs-lookup"><span data-stu-id="32ebe-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="32ebe-127">Tipo de imagem</span><span class="sxs-lookup"><span data-stu-id="32ebe-127">Image type</span></span>         | <span data-ttu-id="32ebe-128">Estilo de controle estático</span><span class="sxs-lookup"><span data-stu-id="32ebe-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="32ebe-129">BITMAP de imagem \_</span><span class="sxs-lookup"><span data-stu-id="32ebe-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="32ebe-130">\_bitmap SS</span><span class="sxs-lookup"><span data-stu-id="32ebe-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="32ebe-131">CURSOR de imagem \_</span><span class="sxs-lookup"><span data-stu-id="32ebe-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="32ebe-132">\_ícone SS</span><span class="sxs-lookup"><span data-stu-id="32ebe-132">SS\_ICON</span></span>             |
| <span data-ttu-id="32ebe-133">ENHMETAFILE de imagem \_</span><span class="sxs-lookup"><span data-stu-id="32ebe-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="32ebe-134">\_ENHMETAFILE SS</span><span class="sxs-lookup"><span data-stu-id="32ebe-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="32ebe-135">ícone de imagem \_</span><span class="sxs-lookup"><span data-stu-id="32ebe-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="32ebe-136">\_ícone SS</span><span class="sxs-lookup"><span data-stu-id="32ebe-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="32ebe-137">Na versão 6 dos controles Microsoft Win32, um bitmap passado para um controle estático usando a mensagem **STM \_ SetImage** era o mesmo bitmap retornado por uma mensagem **STM \_ SetImage** subsequente.</span><span class="sxs-lookup"><span data-stu-id="32ebe-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="32ebe-138">O cliente é responsável por excluir qualquer bitmap enviado para um controle estático.</span><span class="sxs-lookup"><span data-stu-id="32ebe-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="32ebe-139">Com o Windows XP, se o bitmap passado na mensagem **STM \_ SetImage** contiver pixels com alfa diferente de zero, o controle estático usará uma cópia do bitmap.</span><span class="sxs-lookup"><span data-stu-id="32ebe-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="32ebe-140">Esse bitmap copiado é retornado pela próxima mensagem do **STM \_ SetImage** .</span><span class="sxs-lookup"><span data-stu-id="32ebe-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="32ebe-141">O código do cliente pode rastrear de forma independente os bitmaps passados para o controle estático, mas se ele não verificar e liberar os bitmaps retornados de mensagens **\_ SetImage de STM** , os bitmaps serão vazados.</span><span class="sxs-lookup"><span data-stu-id="32ebe-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32ebe-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32ebe-142">Requirements</span></span>



| <span data-ttu-id="32ebe-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ebe-143">Requirement</span></span> | <span data-ttu-id="32ebe-144">Valor</span><span class="sxs-lookup"><span data-stu-id="32ebe-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ebe-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ebe-145">Minimum supported client</span></span><br/> | <span data-ttu-id="32ebe-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32ebe-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32ebe-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ebe-147">Minimum supported server</span></span><br/> | <span data-ttu-id="32ebe-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32ebe-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32ebe-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32ebe-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ebe-150"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32ebe-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ebe-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="32ebe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ebe-152">**STM \_ GETimage**</span><span class="sxs-lookup"><span data-stu-id="32ebe-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





