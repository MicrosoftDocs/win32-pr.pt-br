---
title: Propriedade IMsRdpClientNonScriptable3 RedirectDynamicDrives
description: Especifica ou recupera se as unidades PnP (Plug and Play conectadas dinamicamente) que são enumeradas enquanto estiverem em uma sessão estão disponíveis para redirecionamento.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645186"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="c5f13-120">Propriedade IMsRdpClientNonScriptable3:: RedirectDynamicDrives</span><span class="sxs-lookup"><span data-stu-id="c5f13-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="c5f13-121">Especifica ou recupera se as unidades PnP (Plug and Play conectadas dinamicamente) que são enumeradas enquanto estiverem em uma sessão estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="c5f13-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="c5f13-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c5f13-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f13-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f13-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="c5f13-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c5f13-124">Property value</span></span>

<span data-ttu-id="c5f13-125">Especifica se as unidades PnP conectadas dinamicamente que são enumeradas enquanto estiverem em uma sessão estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="c5f13-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5f13-126">Requirements</span></span>



| <span data-ttu-id="c5f13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f13-127">Requirement</span></span> | <span data-ttu-id="c5f13-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c5f13-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f13-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5f13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f13-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5f13-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c5f13-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5f13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f13-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5f13-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c5f13-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5f13-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5f13-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5f13-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c5f13-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c5f13-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5f13-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5f13-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c5f13-137">IID</span><span class="sxs-lookup"><span data-stu-id="c5f13-137">IID</span></span><br/>                      | <span data-ttu-id="c5f13-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="c5f13-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5f13-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5f13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f13-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c5f13-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c5f13-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c5f13-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c5f13-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c5f13-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





