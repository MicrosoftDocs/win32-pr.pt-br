---
title: Propriedade IMsRdpClientAdvancedSettings BitmapCacheSize
description: O tamanho, em kilobytes, do arquivo de cache de bitmap usado para bitmaps de 8 bits por pixel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapCacheSize
- Propriedade BitmapCacheSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369449"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="70a40-120">Propriedade IMsRdpClientAdvancedSettings:: BitmapCacheSize</span><span class="sxs-lookup"><span data-stu-id="70a40-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="70a40-121">O tamanho, em kilobytes, do arquivo de cache de bitmap usado para bitmaps de 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="70a40-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="70a40-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="70a40-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a40-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="70a40-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="70a40-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70a40-124">Property value</span></span>

<span data-ttu-id="70a40-125">O novo tamanho do cache, em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="70a40-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="70a40-126">Os valores numéricos válidos são de 1 a 32, inclusive.</span><span class="sxs-lookup"><span data-stu-id="70a40-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70a40-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="70a40-127">Error codes</span></span>

<span data-ttu-id="70a40-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="70a40-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a40-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="70a40-129">Remarks</span></span>

<span data-ttu-id="70a40-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="70a40-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70a40-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a40-131">Requirements</span></span>



| <span data-ttu-id="70a40-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a40-132">Requirement</span></span> | <span data-ttu-id="70a40-133">Valor</span><span class="sxs-lookup"><span data-stu-id="70a40-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a40-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70a40-134">Minimum supported client</span></span><br/> | <span data-ttu-id="70a40-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70a40-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="70a40-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70a40-136">Minimum supported server</span></span><br/> | <span data-ttu-id="70a40-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70a40-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="70a40-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="70a40-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="70a40-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a40-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="70a40-140">DLL</span><span class="sxs-lookup"><span data-stu-id="70a40-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a40-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a40-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="70a40-142">IID</span><span class="sxs-lookup"><span data-stu-id="70a40-142">IID</span></span><br/>                      | <span data-ttu-id="70a40-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="70a40-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70a40-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="70a40-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a40-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="70a40-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="70a40-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="70a40-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="70a40-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="70a40-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="70a40-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="70a40-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="70a40-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="70a40-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="70a40-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="70a40-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="70a40-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="70a40-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="70a40-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="70a40-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





