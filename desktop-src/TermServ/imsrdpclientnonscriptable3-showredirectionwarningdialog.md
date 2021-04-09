---
title: Propriedade IMsRdpClientNonScriptable3 ShowRedirectionWarningDialog
description: Especifica ou recupera se a caixa de diálogo de aviso de redirecionamento deve ser mostrada.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade ShowRedirectionWarningDialog
- Propriedade ShowRedirectionWarningDialog Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade ShowRedirectionWarningDialog
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009090"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="14f73-120">Propriedade IMsRdpClientNonScriptable3:: ShowRedirectionWarningDialog</span><span class="sxs-lookup"><span data-stu-id="14f73-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="14f73-121">Especifica ou recupera se a caixa de diálogo de aviso de redirecionamento deve ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="14f73-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="14f73-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="14f73-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f73-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="14f73-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="14f73-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="14f73-124">Property value</span></span>

<span data-ttu-id="14f73-125">Especifica se a caixa de diálogo de aviso de redirecionamento deve ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="14f73-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f73-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14f73-126">Requirements</span></span>



| <span data-ttu-id="14f73-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f73-127">Requirement</span></span> | <span data-ttu-id="14f73-128">Valor</span><span class="sxs-lookup"><span data-stu-id="14f73-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f73-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14f73-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14f73-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14f73-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="14f73-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14f73-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14f73-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14f73-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="14f73-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="14f73-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="14f73-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14f73-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="14f73-135">DLL</span><span class="sxs-lookup"><span data-stu-id="14f73-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f73-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14f73-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="14f73-137">IID</span><span class="sxs-lookup"><span data-stu-id="14f73-137">IID</span></span><br/>                      | <span data-ttu-id="14f73-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="14f73-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14f73-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="14f73-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f73-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="14f73-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="14f73-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="14f73-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="14f73-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="14f73-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





