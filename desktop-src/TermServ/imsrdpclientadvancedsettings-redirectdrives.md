---
title: Propriedade IMsRdpClientAdvancedSettings RedirectDrives
description: Especifica se o redirecionamento de unidades de disco é permitido.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectDrives
- Propriedade RedirectDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645188"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="3a381-120">Propriedade IMsRdpClientAdvancedSettings:: RedirectDrives</span><span class="sxs-lookup"><span data-stu-id="3a381-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="3a381-121">Especifica se o redirecionamento de unidades de disco é permitido.</span><span class="sxs-lookup"><span data-stu-id="3a381-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="3a381-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3a381-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a381-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a381-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="3a381-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3a381-124">Property value</span></span>

<span data-ttu-id="3a381-125">Defina esse parâmetro como **Variant \_ true** para permitir redirecionamento ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3a381-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="3a381-126">**Variante \_ VERDADEIRO** solicita que o usuário confirme a permissão de redirecionamento no momento da conexão, para fins de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a381-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a381-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3a381-127">Error codes</span></span>

<span data-ttu-id="3a381-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3a381-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a381-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a381-129">Remarks</span></span>

<span data-ttu-id="3a381-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3a381-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a381-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a381-131">Requirements</span></span>



| <span data-ttu-id="3a381-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a381-132">Requirement</span></span> | <span data-ttu-id="3a381-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3a381-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a381-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a381-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3a381-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a381-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3a381-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a381-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3a381-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a381-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3a381-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3a381-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a381-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a381-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3a381-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3a381-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a381-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a381-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3a381-142">IID</span><span class="sxs-lookup"><span data-stu-id="3a381-142">IID</span></span><br/>                      | <span data-ttu-id="3a381-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="3a381-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a381-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a381-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a381-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="3a381-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="3a381-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="3a381-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3a381-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="3a381-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="3a381-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3a381-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="3a381-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3a381-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3a381-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3a381-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3a381-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3a381-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3a381-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="3a381-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





