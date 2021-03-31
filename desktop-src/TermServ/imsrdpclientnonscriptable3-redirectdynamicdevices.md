---
title: Propriedade IMsRdpClientNonScriptable3 RedirectDynamicDevices
description: Especifica ou recupera se os dispositivos PnP (Plug and Play dinamicamente anexados) que são enumerados enquanto estão em uma sessão estão disponíveis para redirecionamento.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDevices
- Propriedade RedirectDynamicDevices Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644374"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="25a68-120">Propriedade IMsRdpClientNonScriptable3:: RedirectDynamicDevices</span><span class="sxs-lookup"><span data-stu-id="25a68-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="25a68-121">Especifica ou recupera se os dispositivos PnP (Plug and Play dinamicamente anexados) que são enumerados enquanto estão em uma sessão estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="25a68-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="25a68-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="25a68-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="25a68-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="25a68-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="25a68-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="25a68-124">Property value</span></span>

<span data-ttu-id="25a68-125">Especifica se dispositivos PnP dinamicamente anexados que são enumerados enquanto estão em uma sessão estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="25a68-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="25a68-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25a68-126">Requirements</span></span>



| <span data-ttu-id="25a68-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="25a68-127">Requirement</span></span> | <span data-ttu-id="25a68-128">Valor</span><span class="sxs-lookup"><span data-stu-id="25a68-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25a68-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25a68-129">Minimum supported client</span></span><br/> | <span data-ttu-id="25a68-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25a68-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="25a68-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25a68-131">Minimum supported server</span></span><br/> | <span data-ttu-id="25a68-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25a68-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="25a68-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="25a68-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="25a68-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25a68-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="25a68-135">DLL</span><span class="sxs-lookup"><span data-stu-id="25a68-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25a68-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25a68-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="25a68-137">IID</span><span class="sxs-lookup"><span data-stu-id="25a68-137">IID</span></span><br/>                      | <span data-ttu-id="25a68-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="25a68-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25a68-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="25a68-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a68-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="25a68-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="25a68-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="25a68-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="25a68-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="25a68-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





