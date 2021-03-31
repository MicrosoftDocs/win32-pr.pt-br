---
title: Propriedade do servidor IMsTscAx (Asptlb. h)
description: Especifica o nome do servidor ao qual o controle atual está conectado.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de Propriedade do servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade de servidor
- Propriedade do servidor Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade de servidor
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918070"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="d92e6-124">Propriedade IMsTscAx:: Server</span><span class="sxs-lookup"><span data-stu-id="d92e6-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="d92e6-125">Especifica o nome do servidor ao qual o controle atual está conectado.</span><span class="sxs-lookup"><span data-stu-id="d92e6-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="d92e6-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d92e6-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92e6-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d92e6-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="d92e6-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d92e6-128">Property value</span></span>

<span data-ttu-id="d92e6-129">O novo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d92e6-129">The new server name.</span></span> <span data-ttu-id="d92e6-130">Esse parâmetro pode ser um nome DNS ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="d92e6-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d92e6-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d92e6-131">Error codes</span></span>

<span data-ttu-id="d92e6-132">Se os métodos forem bem-sucedidos, será retornado **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d92e6-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="d92e6-133">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="d92e6-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92e6-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="d92e6-134">Remarks</span></span>

<span data-ttu-id="d92e6-135">Essa propriedade deve ser definida antes de chamar o método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d92e6-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="d92e6-136">É a única propriedade que deve ser definida antes da conexão.</span><span class="sxs-lookup"><span data-stu-id="d92e6-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="d92e6-137">Essa propriedade só poderá ser definida se o controle não estiver no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="d92e6-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="d92e6-138">Essa propriedade retornará **E \_ falhará** se for chamada quando o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="d92e6-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="d92e6-139">Você pode verificar o estado conectado usando a propriedade [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="d92e6-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="d92e6-140">Esse método aloca a memória necessária para o buffer apontado pelo parâmetro *pserver* .</span><span class="sxs-lookup"><span data-stu-id="d92e6-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="d92e6-141">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="d92e6-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="d92e6-142">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="d92e6-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="d92e6-143">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d92e6-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d92e6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92e6-144">Requirements</span></span>



| <span data-ttu-id="d92e6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92e6-145">Requirement</span></span> | <span data-ttu-id="d92e6-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d92e6-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d92e6-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92e6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d92e6-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d92e6-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d92e6-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92e6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d92e6-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d92e6-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d92e6-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d92e6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92e6-152"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92e6-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="d92e6-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d92e6-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="d92e6-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d92e6-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d92e6-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d92e6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d92e6-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d92e6-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d92e6-157">IID</span><span class="sxs-lookup"><span data-stu-id="d92e6-157">IID</span></span><br/>                      | <span data-ttu-id="d92e6-158">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="d92e6-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d92e6-159">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d92e6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92e6-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="d92e6-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="d92e6-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="d92e6-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="d92e6-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="d92e6-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="d92e6-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="d92e6-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="d92e6-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d92e6-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d92e6-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d92e6-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d92e6-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d92e6-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d92e6-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d92e6-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d92e6-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d92e6-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d92e6-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="d92e6-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

