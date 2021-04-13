---
title: Propriedade IMsRdpClientAdvancedSettings BitmapPersistence
description: Especifica se o cache de bitmap persistente deve ser usado. O cache persistente pode melhorar o desempenho, mas requer espaço em disco adicional.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapPersistence
- Propriedade BitmapPersistence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369448"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="8262a-121">Propriedade IMsRdpClientAdvancedSettings:: BitmapPersistence</span><span class="sxs-lookup"><span data-stu-id="8262a-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="8262a-122">Especifica se o cache de bitmap persistente deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="8262a-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="8262a-123">O cache persistente pode melhorar o desempenho, mas requer espaço em disco adicional.</span><span class="sxs-lookup"><span data-stu-id="8262a-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="8262a-124">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8262a-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8262a-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="8262a-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="8262a-126">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8262a-126">Property value</span></span>

<span data-ttu-id="8262a-127">Defina esse parâmetro como 0 para desabilitar o cache ou um valor diferente de zero para habilitar o Caching.</span><span class="sxs-lookup"><span data-stu-id="8262a-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="8262a-128">O erro ortográfico no nome do parâmetro está na versão liberada do controle.</span><span class="sxs-lookup"><span data-stu-id="8262a-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="8262a-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8262a-129">Error codes</span></span>

<span data-ttu-id="8262a-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8262a-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8262a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8262a-131">Remarks</span></span>

<span data-ttu-id="8262a-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8262a-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8262a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8262a-133">Requirements</span></span>



| <span data-ttu-id="8262a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8262a-134">Requirement</span></span> | <span data-ttu-id="8262a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8262a-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8262a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8262a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8262a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8262a-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="8262a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8262a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8262a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8262a-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="8262a-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8262a-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="8262a-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8262a-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8262a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8262a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8262a-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8262a-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8262a-144">IID</span><span class="sxs-lookup"><span data-stu-id="8262a-144">IID</span></span><br/>                      | <span data-ttu-id="8262a-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="8262a-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8262a-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8262a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8262a-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8262a-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="8262a-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8262a-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8262a-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8262a-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8262a-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8262a-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8262a-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8262a-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8262a-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8262a-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8262a-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8262a-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8262a-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8262a-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





