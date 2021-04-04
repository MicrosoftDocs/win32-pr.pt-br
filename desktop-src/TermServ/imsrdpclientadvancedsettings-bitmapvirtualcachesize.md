---
title: Propriedade IMsRdpClientAdvancedSettings BitmapVirtualCacheSize
description: Especifica o tamanho, em megabytes, do arquivo de cache de bitmap persistente a ser usado para a cor de 8 bits por pixel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapVirtualCacheSize
- Propriedade BitmapVirtualCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009092"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a><span data-ttu-id="513a0-120">Propriedade IMsRdpClientAdvancedSettings:: BitmapVirtualCacheSize</span><span class="sxs-lookup"><span data-stu-id="513a0-120">IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize property</span></span>

<span data-ttu-id="513a0-121">Especifica o tamanho, em megabytes, do arquivo de cache de bitmap persistente a ser usado para a cor de 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="513a0-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for 8-bits-per-pixel color.</span></span>

<span data-ttu-id="513a0-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="513a0-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="513a0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="513a0-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="513a0-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="513a0-124">Property value</span></span>

<span data-ttu-id="513a0-125">O novo tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="513a0-125">The new cache size.</span></span> <span data-ttu-id="513a0-126">Os valores válidos são de 1 a 32, inclusive.</span><span class="sxs-lookup"><span data-stu-id="513a0-126">The valid values are 1 to 32 inclusive.</span></span> <span data-ttu-id="513a0-127">Observe que o tamanho máximo de todos os arquivos de cache virtual é de 128 MB.</span><span class="sxs-lookup"><span data-stu-id="513a0-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="513a0-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="513a0-128">Error codes</span></span>

<span data-ttu-id="513a0-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="513a0-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="513a0-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="513a0-130">Remarks</span></span>

<span data-ttu-id="513a0-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="513a0-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="513a0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513a0-132">Requirements</span></span>



| <span data-ttu-id="513a0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="513a0-133">Requirement</span></span> | <span data-ttu-id="513a0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="513a0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513a0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513a0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="513a0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="513a0-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="513a0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513a0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="513a0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="513a0-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="513a0-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="513a0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="513a0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="513a0-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="513a0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="513a0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="513a0-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="513a0-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="513a0-143">IID</span><span class="sxs-lookup"><span data-stu-id="513a0-143">IID</span></span><br/>                      | <span data-ttu-id="513a0-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="513a0-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="513a0-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="513a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513a0-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="513a0-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="513a0-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="513a0-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="513a0-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="513a0-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="513a0-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="513a0-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="513a0-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="513a0-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="513a0-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="513a0-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="513a0-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="513a0-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="513a0-153">**BitmapVirtualCache16BppSize**</span><span class="sxs-lookup"><span data-stu-id="513a0-153">**BitmapVirtualCache16BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[<span data-ttu-id="513a0-154">**BitmapVirtualCache24BppSize**</span><span class="sxs-lookup"><span data-stu-id="513a0-154">**BitmapVirtualCache24BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[<span data-ttu-id="513a0-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="513a0-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





