---
title: Propriedade IMsRdpClientNonScriptable3 NegotiateSecurityLayer
description: Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781022"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="0cbc0-120">Propriedade IMsRdpClientNonScriptable3:: NegotiateSecurityLayer</span><span class="sxs-lookup"><span data-stu-id="0cbc0-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="0cbc0-121">Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="0cbc0-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbc0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cbc0-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="0cbc0-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0cbc0-124">Property value</span></span>

<span data-ttu-id="0cbc0-125">Especifica se a negociação da camada de segurança deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbc0-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cbc0-126">Remarks</span></span>

<span data-ttu-id="0cbc0-127">Se essa propriedade for definida como **Variant \_ FALSE** e autenticação no nível da rede (NLA) estiver habilitada no sistema operacional do cliente, o cliente não negociará a camada de segurança e, em vez disso, usará o NLA para proteger a conexão RDP.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="0cbc0-128">Se essa propriedade for definida como **Variant \_ true**, o cliente negociará entre a NLA e a segurança de RDP básica.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="0cbc0-129">A desabilitação da negociação da camada de segurança só é possível ao se conectar a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) que executa o Windows Vista ou sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="0cbc0-130">Se essa propriedade estiver habilitada e o cliente tentar se conectar a um servidor de Host da Sessão RD que executa um sistema operacional anterior, a conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0cbc0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cbc0-131">Requirements</span></span>



| <span data-ttu-id="0cbc0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cbc0-132">Requirement</span></span> | <span data-ttu-id="0cbc0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0cbc0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbc0-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cbc0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0cbc0-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cbc0-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0cbc0-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cbc0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0cbc0-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cbc0-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0cbc0-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0cbc0-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cbc0-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cbc0-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0cbc0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0cbc0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cbc0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cbc0-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0cbc0-142">IID</span><span class="sxs-lookup"><span data-stu-id="0cbc0-142">IID</span></span><br/>                      | <span data-ttu-id="0cbc0-143">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="0cbc0-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cbc0-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cbc0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbc0-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0cbc0-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="0cbc0-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0cbc0-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="0cbc0-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="0cbc0-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





