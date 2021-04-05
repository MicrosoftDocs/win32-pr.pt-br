---
title: Propriedade IMsRdpClientNonScriptable3 EnableCredSspSupport
description: Especifica ou recupera se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085490"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="8f949-120">Propriedade IMsRdpClientNonScriptable3:: EnableCredSspSupport</span><span class="sxs-lookup"><span data-stu-id="8f949-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="8f949-121">Especifica ou recupera se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="8f949-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="8f949-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8f949-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f949-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f949-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="8f949-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8f949-124">Property value</span></span>

<span data-ttu-id="8f949-125">Especifica se o CredSSP está habilitado para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="8f949-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f949-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f949-126">Requirements</span></span>



| <span data-ttu-id="8f949-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f949-127">Requirement</span></span> | <span data-ttu-id="8f949-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8f949-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f949-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f949-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8f949-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f949-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8f949-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f949-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8f949-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f949-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8f949-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8f949-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f949-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f949-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8f949-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8f949-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f949-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f949-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8f949-137">IID</span><span class="sxs-lookup"><span data-stu-id="8f949-137">IID</span></span><br/>                      | <span data-ttu-id="8f949-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="8f949-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f949-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f949-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f949-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8f949-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="8f949-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8f949-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8f949-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="8f949-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





