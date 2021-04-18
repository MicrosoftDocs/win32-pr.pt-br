---
title: Propriedade IMsRdpClientAdvancedSettings CachePersistenceActive
description: Especifica se o cache de bitmap persistente deve ser usado. O cache persistente pode melhorar o desempenho, mas requer espaço em disco adicional.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade CachePersistenceActive
- Propriedade CachePersistenceActive Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756972"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="e4717-121">Propriedade IMsRdpClientAdvancedSettings:: CachePersistenceActive</span><span class="sxs-lookup"><span data-stu-id="e4717-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="e4717-122">Especifica se o cache de bitmap persistente deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="e4717-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="e4717-123">O cache persistente pode melhorar o desempenho, mas requer espaço em disco adicional.</span><span class="sxs-lookup"><span data-stu-id="e4717-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="e4717-124">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e4717-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4717-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4717-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="e4717-126">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e4717-126">Property value</span></span>

<span data-ttu-id="e4717-127">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="e4717-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4717-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e4717-128">Error codes</span></span>

<span data-ttu-id="e4717-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e4717-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4717-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4717-130">Remarks</span></span>

<span data-ttu-id="e4717-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e4717-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4717-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4717-132">Requirements</span></span>



| <span data-ttu-id="e4717-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4717-133">Requirement</span></span> | <span data-ttu-id="e4717-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e4717-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4717-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4717-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4717-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4717-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e4717-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4717-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4717-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4717-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e4717-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e4717-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4717-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4717-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e4717-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e4717-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4717-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4717-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e4717-143">IID</span><span class="sxs-lookup"><span data-stu-id="e4717-143">IID</span></span><br/>                      | <span data-ttu-id="e4717-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e4717-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4717-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4717-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4717-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e4717-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e4717-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e4717-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e4717-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e4717-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e4717-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e4717-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e4717-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e4717-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e4717-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e4717-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e4717-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e4717-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e4717-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e4717-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





