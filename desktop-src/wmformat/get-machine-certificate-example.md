---
title: Obter exemplo de certificado do computador
description: Obter exemplo de certificado do computador
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows SDK de Formato de Mídia, certificados de computador
- Windows SDK de Formato de Mídia, certificados
- Windows SDK de Formato de Mídia, código de exemplo
- Windows SDK de Formato de Mídia, exemplos de código
- DRM (gerenciamento de direitos digitais), certificados de computador
- DRM (gerenciamento de direitos digitais), certificados de computador
- DRM (gerenciamento de direitos digitais), certificados
- DRM (gerenciamento de direitos digitais), certificados
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- APIs estendidas do cliente DRM, certificados de computador
- APIs estendidas do cliente, certificados de computador
- APIs estendidas do cliente DRM, certificados
- APIs estendidas do cliente, certificados
- APIs estendidas do cliente DRM, código de exemplo
- APIs estendidas do cliente, código de exemplo
- APIs estendidas do cliente DRM, exemplos de código
- APIs estendidas do cliente, exemplos de código
- certificados, exemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964005"
---
# <a name="get-machine-certificate-example"></a>Obter exemplo de certificado do computador

O exemplo a seguir mostra como recuperar a coleção de certificados do computador:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos de importação de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




