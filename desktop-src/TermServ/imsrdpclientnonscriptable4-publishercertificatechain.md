---
title: Propriedade IMsRdpClientNonScriptable4 PublisherCertificateChain
description: Controla a cadeia de certificados do Publicador. A cadeia é armazenada em uma variante do tipo VT \_ ByRef que contém um ponteiro para uma \_ estrutura de contexto de cadeia de certificados \_ . Para obter informações sobre as \_ estruturas ByRef do VT, consulte VARIANT e VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
- Propriedade PublisherCertificateChain Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824548"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="bd5e3-118">IMsRdpClientNonScriptable4: Propriedade ublisherCertificateChain de:P</span><span class="sxs-lookup"><span data-stu-id="bd5e3-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="bd5e3-119">Controla a cadeia de certificados do Publicador.</span><span class="sxs-lookup"><span data-stu-id="bd5e3-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="bd5e3-120">A cadeia é armazenada em uma variante do tipo **VT \_ ByRef** que contém um ponteiro para uma estrutura de [**\_ \_ contexto de cadeia de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="bd5e3-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="bd5e3-121">Para obter informações sobre as estruturas **\_ ByRef do VT** , consulte [Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="bd5e3-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="bd5e3-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bd5e3-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5e3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd5e3-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="bd5e3-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bd5e3-124">Property value</span></span>

<span data-ttu-id="bd5e3-125">Define a cadeia de certificados do Publicador.</span><span class="sxs-lookup"><span data-stu-id="bd5e3-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="bd5e3-126">A cadeia é armazenada em uma variante do tipo **VT \_ ByRef** que contém um ponteiro para uma estrutura de [**\_ \_ contexto de cadeia de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="bd5e3-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd5e3-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bd5e3-127">Error codes</span></span>

<span data-ttu-id="bd5e3-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bd5e3-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5e3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd5e3-129">Requirements</span></span>



| <span data-ttu-id="bd5e3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd5e3-130">Requirement</span></span> | <span data-ttu-id="bd5e3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bd5e3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5e3-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd5e3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5e3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd5e3-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bd5e3-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd5e3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5e3-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd5e3-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bd5e3-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bd5e3-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd5e3-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd5e3-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bd5e3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bd5e3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd5e3-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd5e3-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bd5e3-140">IID</span><span class="sxs-lookup"><span data-stu-id="bd5e3-140">IID</span></span><br/>                      | <span data-ttu-id="bd5e3-141">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="bd5e3-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd5e3-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd5e3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5e3-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bd5e3-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bd5e3-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bd5e3-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

