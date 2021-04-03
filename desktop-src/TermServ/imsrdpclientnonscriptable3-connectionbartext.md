---
title: Propriedade IMsRdpClientNonScriptable3 ConnectionBarText
description: Define ou recupera o texto para atualizar a barra de conexão.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade ConnectionBarText
- Propriedade ConnectionBarText Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645098"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="4a73e-120">Propriedade IMsRdpClientNonScriptable3:: ConnectionBarText</span><span class="sxs-lookup"><span data-stu-id="4a73e-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="4a73e-121">Define ou recupera o texto para atualizar a barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="4a73e-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="4a73e-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4a73e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a73e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a73e-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="4a73e-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4a73e-124">Property value</span></span>

<span data-ttu-id="4a73e-125">Define a cadeia de texto a ser exibida na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="4a73e-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a73e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a73e-126">Remarks</span></span>

<span data-ttu-id="4a73e-127">Você deve chamar o método **IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText** antes de chamar o método [**IMsTscSecuredSettings::p UT \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou o método [**IMsRdpClient::p UT \_ fullscreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="4a73e-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a73e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a73e-128">Requirements</span></span>



| <span data-ttu-id="4a73e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a73e-129">Requirement</span></span> | <span data-ttu-id="4a73e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4a73e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a73e-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a73e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4a73e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a73e-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4a73e-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a73e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4a73e-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a73e-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4a73e-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4a73e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a73e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a73e-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4a73e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4a73e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a73e-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a73e-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4a73e-139">IID</span><span class="sxs-lookup"><span data-stu-id="4a73e-139">IID</span></span><br/>                      | <span data-ttu-id="4a73e-140">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="4a73e-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a73e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a73e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a73e-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="4a73e-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="4a73e-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4a73e-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="4a73e-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="4a73e-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





