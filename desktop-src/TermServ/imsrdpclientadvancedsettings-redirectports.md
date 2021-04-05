---
title: Propriedade IMsRdpClientAdvancedSettings RedirectPorts
description: Especifica se o redirecionamento de portas locais (por exemplo, COM e LPT) é permitido.
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectPorts
- Propriedade RedirectPorts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectPorts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918004"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="ccb80-120">Propriedade IMsRdpClientAdvancedSettings:: RedirectPorts</span><span class="sxs-lookup"><span data-stu-id="ccb80-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="ccb80-121">Especifica se o redirecionamento de portas locais (por exemplo, COM e LPT) é permitido.</span><span class="sxs-lookup"><span data-stu-id="ccb80-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="ccb80-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ccb80-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb80-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccb80-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="ccb80-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ccb80-124">Property value</span></span>

<span data-ttu-id="ccb80-125">Defina esse parâmetro como **Variant \_ true** para permitir redirecionamento ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ccb80-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="ccb80-126">**Variante \_ VERDADEIRO** solicita que o usuário confirme a permissão de redirecionamento no momento da conexão, para fins de segurança.</span><span class="sxs-lookup"><span data-stu-id="ccb80-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccb80-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ccb80-127">Error codes</span></span>

<span data-ttu-id="ccb80-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ccb80-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb80-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccb80-129">Remarks</span></span>

<span data-ttu-id="ccb80-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ccb80-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb80-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb80-131">Requirements</span></span>



| <span data-ttu-id="ccb80-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb80-132">Requirement</span></span> | <span data-ttu-id="ccb80-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb80-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb80-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb80-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb80-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccb80-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ccb80-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb80-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb80-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccb80-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ccb80-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ccb80-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccb80-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb80-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ccb80-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb80-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb80-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb80-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ccb80-142">IID</span><span class="sxs-lookup"><span data-stu-id="ccb80-142">IID</span></span><br/>                      | <span data-ttu-id="ccb80-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ccb80-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccb80-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb80-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb80-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ccb80-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ccb80-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ccb80-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ccb80-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ccb80-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ccb80-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ccb80-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ccb80-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ccb80-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ccb80-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ccb80-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ccb80-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ccb80-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ccb80-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ccb80-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





