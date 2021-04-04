---
title: Propriedade IconFile do IMsTscAdvancedSettings
description: Especifica o nome do arquivo que contém os dados de ícone que serão acessados ao exibir o cliente no modo de tela inteira.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade IconFile
- Propriedade IconFile Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade IconFile
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644651"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="0a15d-122">Propriedade IMsTscAdvancedSettings:: IconFile</span><span class="sxs-lookup"><span data-stu-id="0a15d-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="0a15d-123">Especifica o nome do arquivo que contém os dados de ícone que serão acessados ao exibir o cliente no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="0a15d-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="0a15d-124">Não há suporte para essa propriedade no controle ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="0a15d-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="0a15d-125">Há suporte na biblioteca MsTscAx.dll incluída no cliente Standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="0a15d-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="0a15d-126">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="0a15d-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a15d-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a15d-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="0a15d-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0a15d-128">Property value</span></span>

<span data-ttu-id="0a15d-129">O caminho totalmente qualificado do arquivo de ícone ou um arquivo que contém dados de ícone, como uma DLL.</span><span class="sxs-lookup"><span data-stu-id="0a15d-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a15d-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0a15d-130">Error codes</span></span>

<span data-ttu-id="0a15d-131">Retorna **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a15d-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a15d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a15d-132">Remarks</span></span>

<span data-ttu-id="0a15d-133">A extensão de nome de arquivo de um arquivo de ícone é ". ico".</span><span class="sxs-lookup"><span data-stu-id="0a15d-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="0a15d-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a15d-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a15d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a15d-135">Requirements</span></span>



| <span data-ttu-id="0a15d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a15d-136">Requirement</span></span> | <span data-ttu-id="0a15d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0a15d-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a15d-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a15d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0a15d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a15d-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="0a15d-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a15d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0a15d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a15d-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0a15d-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a15d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a15d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a15d-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0a15d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0a15d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a15d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a15d-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0a15d-146">IID</span><span class="sxs-lookup"><span data-stu-id="0a15d-146">IID</span></span><br/>                      | <span data-ttu-id="0a15d-147">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="0a15d-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a15d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a15d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a15d-149">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0a15d-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0a15d-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0a15d-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0a15d-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0a15d-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="0a15d-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0a15d-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0a15d-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0a15d-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0a15d-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0a15d-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0a15d-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0a15d-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0a15d-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0a15d-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0a15d-157">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0a15d-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





