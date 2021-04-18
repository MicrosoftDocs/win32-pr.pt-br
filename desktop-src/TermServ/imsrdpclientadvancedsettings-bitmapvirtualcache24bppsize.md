---
title: Propriedade IMsRdpClientAdvancedSettings BitmapVirtualCache24BppSize
description: Especifica o tamanho, em megabytes, do arquivo de cache de bitmap persistente a ser usado para a configuração de alta cores de 24 bits por pixel.
ms.assetid: 5891c90d-f463-4f27-b212-351ebf21ae00
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapVirtualCache24BppSize
- Propriedade BitmapVirtualCache24BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapVirtualCache24BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache24BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fc31954ff191f795146e3894b0394b29484fb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764743"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache24bppsize-property"></a><span data-ttu-id="fffb5-120">Propriedade IMsRdpClientAdvancedSettings:: BitmapVirtualCache24BppSize</span><span class="sxs-lookup"><span data-stu-id="fffb5-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache24BppSize property</span></span>

<span data-ttu-id="fffb5-121">Especifica o tamanho, em megabytes, do arquivo de cache de bitmap persistente a ser usado para a configuração de alta cores de 24 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="fffb5-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 24 bits-per-pixel high-color setting.</span></span>

<span data-ttu-id="fffb5-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fffb5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffb5-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fffb5-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache24BppSize(
  [in]  LONG bitmapVirtualCache24BppSize
);

HRESULT get_BitmapVirtualCache24BppSize(
  [out] LONG *pbitmapVirtualCache24BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="fffb5-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fffb5-124">Property value</span></span>

<span data-ttu-id="fffb5-125">O novo tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="fffb5-125">The new cache size.</span></span> <span data-ttu-id="fffb5-126">Os valores válidos são de 1 a 32, inclusive, e o valor padrão é 30.</span><span class="sxs-lookup"><span data-stu-id="fffb5-126">The valid values are 1 to 32 inclusive, and the default value is 30.</span></span> <span data-ttu-id="fffb5-127">Observe que o tamanho máximo de todos os arquivos de cache virtual é de 128 MB.</span><span class="sxs-lookup"><span data-stu-id="fffb5-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fffb5-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fffb5-128">Error codes</span></span>

<span data-ttu-id="fffb5-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fffb5-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffb5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fffb5-130">Remarks</span></span>

<span data-ttu-id="fffb5-131">As propriedades relacionadas incluem as propriedades **BitmapVirtualCacheSize** e **BitmapVirtualCache16BppSize** .</span><span class="sxs-lookup"><span data-stu-id="fffb5-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache16BppSize** properties.</span></span>

<span data-ttu-id="fffb5-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fffb5-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fffb5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fffb5-133">Requirements</span></span>



| <span data-ttu-id="fffb5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fffb5-134">Requirement</span></span> | <span data-ttu-id="fffb5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fffb5-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffb5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fffb5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fffb5-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fffb5-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fffb5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fffb5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fffb5-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fffb5-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fffb5-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fffb5-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fffb5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffb5-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fffb5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fffb5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffb5-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffb5-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fffb5-144">IID</span><span class="sxs-lookup"><span data-stu-id="fffb5-144">IID</span></span><br/>                      | <span data-ttu-id="fffb5-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fffb5-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fffb5-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="fffb5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffb5-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fffb5-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fffb5-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fffb5-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fffb5-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fffb5-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fffb5-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fffb5-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fffb5-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fffb5-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fffb5-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fffb5-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fffb5-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fffb5-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fffb5-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fffb5-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





