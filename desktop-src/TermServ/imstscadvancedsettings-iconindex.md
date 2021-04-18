---
title: Propriedade IMsTscAdvancedSettings IconIndex
description: Especifica o índice do ícone dentro do arquivo de ícone atual.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade IconIndex
- Propriedade IconIndex Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade IconIndex
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499365"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="11a12-122">Propriedade IMsTscAdvancedSettings:: IconIndex</span><span class="sxs-lookup"><span data-stu-id="11a12-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="11a12-123">Especifica o índice do ícone dentro do arquivo de ícone atual.</span><span class="sxs-lookup"><span data-stu-id="11a12-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="11a12-124">Não há suporte para essa propriedade no controle ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="11a12-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="11a12-125">Há suporte na biblioteca MsTscAx.dll incluída no cliente Standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="11a12-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="11a12-126">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="11a12-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a12-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a12-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="11a12-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="11a12-128">Property value</span></span>

<span data-ttu-id="11a12-129">O índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="11a12-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11a12-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="11a12-130">Error codes</span></span>

<span data-ttu-id="11a12-131">Retorna **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="11a12-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a12-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="11a12-132">Remarks</span></span>

<span data-ttu-id="11a12-133">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="11a12-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11a12-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11a12-134">Requirements</span></span>



| <span data-ttu-id="11a12-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="11a12-135">Requirement</span></span> | <span data-ttu-id="11a12-136">Valor</span><span class="sxs-lookup"><span data-stu-id="11a12-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a12-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11a12-137">Minimum supported client</span></span><br/> | <span data-ttu-id="11a12-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11a12-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="11a12-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11a12-139">Minimum supported server</span></span><br/> | <span data-ttu-id="11a12-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11a12-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="11a12-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="11a12-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="11a12-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a12-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="11a12-143">DLL</span><span class="sxs-lookup"><span data-stu-id="11a12-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11a12-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a12-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="11a12-145">IID</span><span class="sxs-lookup"><span data-stu-id="11a12-145">IID</span></span><br/>                      | <span data-ttu-id="11a12-146">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="11a12-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11a12-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="11a12-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a12-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="11a12-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="11a12-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="11a12-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="11a12-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="11a12-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="11a12-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="11a12-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="11a12-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="11a12-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="11a12-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="11a12-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="11a12-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="11a12-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="11a12-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="11a12-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="11a12-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="11a12-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





