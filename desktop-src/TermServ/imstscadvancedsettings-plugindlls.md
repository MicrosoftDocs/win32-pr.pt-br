---
title: Propriedade IMsTscAdvancedSettings PluginDlls
description: Especifica os nomes das DLLs de cliente do canal virtual a serem carregadas.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade PluginDlls
- Propriedade PluginDlls Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade PluginDlls
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455155"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="31af2-122">IMsTscAdvancedSettings: Propriedade luginDlls de:P</span><span class="sxs-lookup"><span data-stu-id="31af2-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="31af2-123">Especifica os nomes das DLLs de cliente do canal virtual a serem carregadas.</span><span class="sxs-lookup"><span data-stu-id="31af2-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="31af2-124">As DLLs de cliente de canal virtual também são chamadas de DLLs de plug-in.</span><span class="sxs-lookup"><span data-stu-id="31af2-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="31af2-125">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="31af2-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31af2-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="31af2-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="31af2-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="31af2-127">Property value</span></span>

<span data-ttu-id="31af2-128">Lista separada por vírgulas dos nomes das DLLs de cliente do canal virtual a serem carregadas.</span><span class="sxs-lookup"><span data-stu-id="31af2-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="31af2-129">Os nomes de DLL devem conter apenas caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="31af2-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="31af2-130">Para obter mais informações sobre o formato desses nomes, consulte [DVC plug-in Registration](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="31af2-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="31af2-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="31af2-131">Error codes</span></span>

<span data-ttu-id="31af2-132">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="31af2-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="31af2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="31af2-133">Remarks</span></span>

<span data-ttu-id="31af2-134">Por motivos de segurança, se o controle estiver hospedado em uma página da Web, a propriedade **PluginDlls** só aceitará uma lista nomeada de DLLs de cliente de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="31af2-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="31af2-135">O controle retornará um erro se um sistema de arquivos ou caminho UNC for especificado.</span><span class="sxs-lookup"><span data-stu-id="31af2-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="31af2-136">As DLLs de cliente do canal virtual que serão acessadas por meio de uma página da Web devem ser instaladas no diretório "% WinDir% \\ System32" porque o controle ActiveX área de trabalho remota só acessa arquivos dll nesse local.</span><span class="sxs-lookup"><span data-stu-id="31af2-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="31af2-137">Se o controle não estiver hospedado em uma página da Web, essa restrição de segurança não existirá e os caminhos completos poderão ser usados para acessar e carregar as DLLs de cliente do canal virtual localizadas em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="31af2-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="31af2-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31af2-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31af2-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31af2-139">Requirements</span></span>



| <span data-ttu-id="31af2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="31af2-140">Requirement</span></span> | <span data-ttu-id="31af2-141">Valor</span><span class="sxs-lookup"><span data-stu-id="31af2-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31af2-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31af2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="31af2-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31af2-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="31af2-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31af2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="31af2-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31af2-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="31af2-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="31af2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="31af2-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31af2-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="31af2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="31af2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31af2-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31af2-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="31af2-150">IID</span><span class="sxs-lookup"><span data-stu-id="31af2-150">IID</span></span><br/>                      | <span data-ttu-id="31af2-151">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="31af2-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31af2-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="31af2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31af2-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="31af2-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="31af2-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="31af2-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="31af2-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="31af2-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="31af2-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="31af2-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="31af2-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="31af2-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="31af2-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="31af2-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="31af2-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="31af2-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="31af2-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="31af2-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="31af2-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="31af2-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





