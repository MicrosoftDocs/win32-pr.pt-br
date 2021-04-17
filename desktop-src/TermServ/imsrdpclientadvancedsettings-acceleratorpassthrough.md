---
title: Propriedade IMsRdpClientAdvancedSettings AcceleratorPassthrough
description: Especifica se os aceleradores de teclado devem ser passados para o servidor.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AcceleratorPassthrough
- Propriedade AcceleratorPassthrough Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AcceleratorPassthrough
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755163"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="22d7f-120">Propriedade IMsRdpClientAdvancedSettings:: AcceleratorPassthrough</span><span class="sxs-lookup"><span data-stu-id="22d7f-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="22d7f-121">Especifica se os aceleradores de teclado devem ser passados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="22d7f-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="22d7f-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="22d7f-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d7f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d7f-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="22d7f-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="22d7f-124">Property value</span></span>

<span data-ttu-id="22d7f-125">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="22d7f-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="22d7f-126">O padrão é um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="22d7f-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22d7f-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="22d7f-127">Error codes</span></span>

<span data-ttu-id="22d7f-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="22d7f-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d7f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="22d7f-129">Remarks</span></span>

<span data-ttu-id="22d7f-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="22d7f-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22d7f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22d7f-131">Requirements</span></span>



| <span data-ttu-id="22d7f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d7f-132">Requirement</span></span> | <span data-ttu-id="22d7f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="22d7f-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d7f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22d7f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="22d7f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22d7f-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="22d7f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22d7f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="22d7f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22d7f-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="22d7f-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="22d7f-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="22d7f-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22d7f-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="22d7f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="22d7f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22d7f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22d7f-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="22d7f-142">IID</span><span class="sxs-lookup"><span data-stu-id="22d7f-142">IID</span></span><br/>                      | <span data-ttu-id="22d7f-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="22d7f-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22d7f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="22d7f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d7f-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="22d7f-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="22d7f-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="22d7f-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="22d7f-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="22d7f-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="22d7f-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="22d7f-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="22d7f-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="22d7f-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="22d7f-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="22d7f-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="22d7f-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="22d7f-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="22d7f-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="22d7f-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





