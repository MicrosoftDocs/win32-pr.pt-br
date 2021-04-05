---
title: Propriedade IMsRdpClientAdvancedSettings ConnectToServerConsole
description: Não há suporte a esta propriedade. Chamadas para ConnectToServerConsole sempre retornam S \_ false.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectToServerConsole
- Propriedade ConnectToServerConsole Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectToServerConsole
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918371"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="bf9c9-121">Propriedade IMsRdpClientAdvancedSettings:: ConnectToServerConsole</span><span class="sxs-lookup"><span data-stu-id="bf9c9-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="bf9c9-122">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-122">This property is not supported.</span></span> <span data-ttu-id="bf9c9-123">Chamadas para **ConnectToServerConsole** sempre retornam **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="bf9c9-124">Use a propriedade [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) para se conectar à sessão que é usada para fins administrativos.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="bf9c9-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9c9-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf9c9-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="bf9c9-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bf9c9-127">Property value</span></span>

<span data-ttu-id="bf9c9-128">Defina esse parâmetro como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="bf9c9-129">**Variante \_ TRUE** não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf9c9-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bf9c9-130">Error codes</span></span>

<span data-ttu-id="bf9c9-131">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bf9c9-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9c9-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf9c9-132">Remarks</span></span>

<span data-ttu-id="bf9c9-133">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf9c9-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf9c9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf9c9-134">Requirements</span></span>



| <span data-ttu-id="bf9c9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf9c9-135">Requirement</span></span> | <span data-ttu-id="bf9c9-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9c9-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9c9-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf9c9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9c9-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bf9c9-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bf9c9-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf9c9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9c9-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bf9c9-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bf9c9-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bf9c9-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf9c9-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9c9-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bf9c9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9c9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9c9-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9c9-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bf9c9-145">IID</span><span class="sxs-lookup"><span data-stu-id="bf9c9-145">IID</span></span><br/>                      | <span data-ttu-id="bf9c9-146">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="bf9c9-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf9c9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf9c9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9c9-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bf9c9-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bf9c9-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





