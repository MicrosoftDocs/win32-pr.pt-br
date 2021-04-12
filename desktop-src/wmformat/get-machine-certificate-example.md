---
title: Obter exemplo de certificado de computador
description: Obter exemplo de certificado de computador
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- SDK do Windows Media Format, certificados de máquina
- SDK do Windows Media Format, certificados
- SDK do Windows Media Format, código de exemplo
- SDK do Windows Media Format, exemplos de código
- DRM (gerenciamento de direitos digitais), certificados de máquina
- DRM (gerenciamento de direitos digitais), certificados de máquina
- DRM (gerenciamento de direitos digitais), certificados
- DRM (gerenciamento de direitos digitais), certificados
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- APIs estendidas do cliente DRM, certificados de máquina
- APIs estendidas do cliente, certificados de máquina
- APIs estendidas do cliente DRM, certificados
- APIs estendidas do cliente, certificados
- APIs estendidas do cliente DRM, código de exemplo
- APIs estendidas do cliente, código de exemplo
- APIs estendidas do cliente DRM, exemplos de código
- APIs estendidas do cliente, exemplos de código
- certificados, exemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364313"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="d1b25-124">Obter exemplo de certificado de computador</span><span class="sxs-lookup"><span data-stu-id="d1b25-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="d1b25-125">O exemplo a seguir mostra como recuperar a coleção de certificados do computador:</span><span class="sxs-lookup"><span data-stu-id="d1b25-125">The following example shows how to retrieve the machine certificate collection:</span></span>


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d1b25-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1b25-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1b25-127">**Exemplos de importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="d1b25-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




