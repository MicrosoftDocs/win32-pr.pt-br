---
title: Propriedade IMsRdpClientNonScriptable3 WarnAboutSendingCredentials
description: Especifica ou recupera se a caixa de diálogo aviso de segurança deve incluir um aviso sobre o envio de credenciais ao servidor remoto antes de iniciar uma sessão.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782878"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="c8d80-120">Propriedade IMsRdpClientNonScriptable3:: WarnAboutSendingCredentials</span><span class="sxs-lookup"><span data-stu-id="c8d80-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="c8d80-121">Especifica ou recupera se a caixa de diálogo aviso de segurança deve incluir um aviso sobre o envio de credenciais ao servidor remoto antes de iniciar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="c8d80-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="c8d80-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c8d80-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d80-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d80-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="c8d80-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c8d80-124">Property value</span></span>

<span data-ttu-id="c8d80-125">Especifica se a caixa de diálogo aviso de segurança deve incluir um aviso sobre o envio de credenciais ao servidor remoto antes de iniciar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="c8d80-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d80-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8d80-126">Requirements</span></span>



| <span data-ttu-id="c8d80-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8d80-127">Requirement</span></span> | <span data-ttu-id="c8d80-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c8d80-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d80-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8d80-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d80-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8d80-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c8d80-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8d80-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d80-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8d80-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c8d80-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c8d80-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8d80-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8d80-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c8d80-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c8d80-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8d80-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8d80-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c8d80-137">IID</span><span class="sxs-lookup"><span data-stu-id="c8d80-137">IID</span></span><br/>                      | <span data-ttu-id="c8d80-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="c8d80-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8d80-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8d80-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d80-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c8d80-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c8d80-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c8d80-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c8d80-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c8d80-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





