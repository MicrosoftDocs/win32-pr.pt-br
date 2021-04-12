---
title: Propriedade IMsRdpClient2 AdvancedSettings3
description: Recupera um ponteiro para a interface IMsRdpClientAdvancedSettings2. A interface pode ser usada para definir configurações avançadas para o controle de cliente.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295811"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="79e15-123">Propriedade IMsRdpClient2:: AdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="79e15-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="79e15-124">Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="79e15-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="79e15-125">A interface pode ser usada para definir configurações avançadas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="79e15-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="79e15-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="79e15-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e15-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79e15-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="79e15-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="79e15-128">Property value</span></span>

<span data-ttu-id="79e15-129">Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="79e15-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79e15-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="79e15-130">Error codes</span></span>

<span data-ttu-id="79e15-131">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="79e15-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="79e15-132">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="79e15-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e15-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="79e15-133">Remarks</span></span>

<span data-ttu-id="79e15-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="79e15-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e15-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e15-135">Requirements</span></span>



| <span data-ttu-id="79e15-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e15-136">Requirement</span></span> | <span data-ttu-id="79e15-137">Valor</span><span class="sxs-lookup"><span data-stu-id="79e15-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e15-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e15-138">Minimum supported client</span></span><br/> | <span data-ttu-id="79e15-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79e15-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="79e15-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e15-140">Minimum supported server</span></span><br/> | <span data-ttu-id="79e15-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79e15-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="79e15-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79e15-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="79e15-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e15-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e15-144">DLL</span><span class="sxs-lookup"><span data-stu-id="79e15-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e15-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e15-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e15-146">IID</span><span class="sxs-lookup"><span data-stu-id="79e15-146">IID</span></span><br/>                      | <span data-ttu-id="79e15-147">IID \_ IMsRdpClient2 é definido como e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="79e15-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="79e15-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="79e15-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e15-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="79e15-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="79e15-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="79e15-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="79e15-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="79e15-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="79e15-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="79e15-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="79e15-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="79e15-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="79e15-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="79e15-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="79e15-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="79e15-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="79e15-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="79e15-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="79e15-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="79e15-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





