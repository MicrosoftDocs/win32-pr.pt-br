---
title: Propriedade IMsRdpClientAdvancedSettings DoubleClickDetect
description: Especifica se o cliente identifica cliques duplos para o servidor.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade DoubleClickDetect
- Propriedade DoubleClickDetect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade DoubleClickDetect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086285"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="4ef42-120">IMsRdpClientAdvancedSettings: Propriedade oubleClickDetect de:D</span><span class="sxs-lookup"><span data-stu-id="4ef42-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="4ef42-121">Especifica se o cliente identifica cliques duplos para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4ef42-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="4ef42-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4ef42-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef42-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ef42-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="4ef42-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4ef42-124">Property value</span></span>

<span data-ttu-id="4ef42-125">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="4ef42-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ef42-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4ef42-126">Error codes</span></span>

<span data-ttu-id="4ef42-127">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4ef42-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef42-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ef42-128">Remarks</span></span>

<span data-ttu-id="4ef42-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4ef42-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef42-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ef42-130">Requirements</span></span>



| <span data-ttu-id="4ef42-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ef42-131">Requirement</span></span> | <span data-ttu-id="4ef42-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4ef42-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef42-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ef42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef42-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ef42-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4ef42-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ef42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef42-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ef42-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4ef42-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ef42-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ef42-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef42-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4ef42-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4ef42-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ef42-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef42-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4ef42-141">IID</span><span class="sxs-lookup"><span data-stu-id="4ef42-141">IID</span></span><br/>                      | <span data-ttu-id="4ef42-142">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4ef42-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ef42-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ef42-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef42-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4ef42-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4ef42-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4ef42-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4ef42-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4ef42-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4ef42-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4ef42-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4ef42-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4ef42-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4ef42-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4ef42-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4ef42-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4ef42-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4ef42-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4ef42-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





