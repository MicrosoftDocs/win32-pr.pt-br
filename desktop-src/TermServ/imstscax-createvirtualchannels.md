---
title: Método IMsTscAx CreateVirtualChannels
description: Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método CreateVirtualChannels
- Método CreateVirtualChannels Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455485"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="a44f6-124">Método IMsTscAx:: CreateVirtualChannels</span><span class="sxs-lookup"><span data-stu-id="a44f6-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="a44f6-125">Cria um objeto de canal virtual do lado do cliente para cada nome de canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="a44f6-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44f6-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a44f6-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a44f6-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a44f6-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a44f6-128">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a44f6-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a44f6-129">Uma lista separada por vírgulas de nomes de canais virtuais válidos.</span><span class="sxs-lookup"><span data-stu-id="a44f6-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="a44f6-130">O comprimento de cada nome nessa lista pode ser um mínimo de um e um máximo de sete caracteres alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="a44f6-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="a44f6-131">O comprimento de toda a cadeia de caracteres pode ser um mínimo de um e um máximo de 300 caracteres alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="a44f6-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a44f6-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a44f6-132">Return value</span></span>

<span data-ttu-id="a44f6-133">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a44f6-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a44f6-134">Retorna **E \_ INVALIDARG** se o parâmetro passado não atender aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="a44f6-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a44f6-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="a44f6-135">Remarks</span></span>

<span data-ttu-id="a44f6-136">Chame esse método antes de chamar o método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="a44f6-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="a44f6-137">Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obter informações sobre restrições de nomenclatura de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="a44f6-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="a44f6-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a44f6-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a44f6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a44f6-139">Requirements</span></span>



| <span data-ttu-id="a44f6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44f6-140">Requirement</span></span> | <span data-ttu-id="a44f6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a44f6-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a44f6-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a44f6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a44f6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a44f6-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a44f6-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a44f6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a44f6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a44f6-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a44f6-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a44f6-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a44f6-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44f6-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a44f6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a44f6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44f6-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44f6-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a44f6-150">IID</span><span class="sxs-lookup"><span data-stu-id="a44f6-150">IID</span></span><br/>                      | <span data-ttu-id="a44f6-151">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a44f6-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a44f6-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="a44f6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a44f6-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a44f6-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a44f6-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a44f6-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a44f6-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a44f6-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a44f6-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a44f6-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a44f6-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a44f6-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a44f6-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a44f6-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a44f6-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a44f6-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a44f6-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a44f6-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a44f6-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a44f6-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a44f6-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a44f6-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





