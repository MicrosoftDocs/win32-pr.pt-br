---
title: Propriedade IMsRdpClientAdvancedSettings GrabFocusOnConnect
description: Especifica se o controle de cliente deve ter o foco durante a conexão.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade GrabFocusOnConnect
- Propriedade GrabFocusOnConnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade GrabFocusOnConnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753330"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="3d14b-120">Propriedade IMsRdpClientAdvancedSettings:: GrabFocusOnConnect</span><span class="sxs-lookup"><span data-stu-id="3d14b-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="3d14b-121">Especifica se o controle de cliente deve ter o foco durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="3d14b-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="3d14b-122">O controle não tentará obter o foco de uma janela em execução em um processo diferente.</span><span class="sxs-lookup"><span data-stu-id="3d14b-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="3d14b-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d14b-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d14b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d14b-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="3d14b-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d14b-125">Property value</span></span>

<span data-ttu-id="3d14b-126">Defina esse parâmetro como **Variant \_ false** para desabilitar o recurso ou a **variante \_ true** para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="3d14b-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="3d14b-127">Definir essa propriedade como **Variant \_ false** impede que o controle se concentre na conexão.</span><span class="sxs-lookup"><span data-stu-id="3d14b-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d14b-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3d14b-128">Error codes</span></span>

<span data-ttu-id="3d14b-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3d14b-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d14b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d14b-130">Remarks</span></span>

<span data-ttu-id="3d14b-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3d14b-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d14b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d14b-132">Requirements</span></span>



| <span data-ttu-id="3d14b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d14b-133">Requirement</span></span> | <span data-ttu-id="3d14b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3d14b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d14b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d14b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3d14b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d14b-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3d14b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d14b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3d14b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d14b-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3d14b-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3d14b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d14b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d14b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d14b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d14b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d14b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d14b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d14b-143">IID</span><span class="sxs-lookup"><span data-stu-id="3d14b-143">IID</span></span><br/>                      | <span data-ttu-id="3d14b-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="3d14b-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d14b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d14b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d14b-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="3d14b-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="3d14b-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="3d14b-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3d14b-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="3d14b-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="3d14b-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3d14b-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="3d14b-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3d14b-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3d14b-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3d14b-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3d14b-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3d14b-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3d14b-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="3d14b-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





