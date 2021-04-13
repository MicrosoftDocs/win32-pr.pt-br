---
title: Propriedade IMsRdpClientNonScriptable3 WarnAboutClipboardRedirection
description: Especifica ou recupera se a caixa de diálogo aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499297"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="cc2b6-120">Propriedade IMsRdpClientNonScriptable3:: WarnAboutClipboardRedirection</span><span class="sxs-lookup"><span data-stu-id="cc2b6-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="cc2b6-121">Especifica ou recupera se a caixa de diálogo aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="cc2b6-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="cc2b6-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cc2b6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2b6-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc2b6-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="cc2b6-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cc2b6-124">Property value</span></span>

<span data-ttu-id="cc2b6-125">Especifica se a caixa de diálogo de aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="cc2b6-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2b6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2b6-126">Requirements</span></span>



| <span data-ttu-id="cc2b6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2b6-127">Requirement</span></span> | <span data-ttu-id="cc2b6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cc2b6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2b6-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc2b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cc2b6-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc2b6-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="cc2b6-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc2b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cc2b6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc2b6-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="cc2b6-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cc2b6-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc2b6-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b6-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="cc2b6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cc2b6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc2b6-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b6-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="cc2b6-137">IID</span><span class="sxs-lookup"><span data-stu-id="cc2b6-137">IID</span></span><br/>                      | <span data-ttu-id="cc2b6-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="cc2b6-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc2b6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc2b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2b6-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="cc2b6-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="cc2b6-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="cc2b6-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="cc2b6-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="cc2b6-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





