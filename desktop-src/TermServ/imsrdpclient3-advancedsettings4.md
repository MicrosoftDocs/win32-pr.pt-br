---
title: Propriedade IMsRdpClient3 AdvancedSettings4
description: Recupera um ponteiro para a interface IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings4
- Propriedade AdvancedSettings4 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824232"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="a4b1a-120">Propriedade IMsRdpClient3:: AdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="a4b1a-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="a4b1a-121">Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b1a-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="a4b1a-122">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b1a-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4b1a-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="a4b1a-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a4b1a-124">Property value</span></span>

<span data-ttu-id="a4b1a-125">Ponteiro para a interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b1a-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="a4b1a-126">A interface pode ser usada para definir configurações avançadas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4b1a-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a4b1a-127">Error codes</span></span>

<span data-ttu-id="a4b1a-128">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="a4b1a-129">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b1a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b1a-130">Remarks</span></span>

<span data-ttu-id="a4b1a-131">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="a4b1a-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a4b1a-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b1a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b1a-133">Requirements</span></span>



| <span data-ttu-id="a4b1a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b1a-134">Requirement</span></span> | <span data-ttu-id="a4b1a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b1a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b1a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b1a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b1a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4b1a-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a4b1a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b1a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b1a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4b1a-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a4b1a-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a4b1a-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4b1a-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b1a-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4b1a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b1a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4b1a-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b1a-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4b1a-144">IID</span><span class="sxs-lookup"><span data-stu-id="a4b1a-144">IID</span></span><br/>                      | <span data-ttu-id="a4b1a-145">IID \_ IMsRdpClient3 é definido como 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="a4b1a-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a4b1a-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b1a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b1a-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a4b1a-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a4b1a-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





