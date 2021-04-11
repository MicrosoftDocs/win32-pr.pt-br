---
title: Inicializar exemplo de importação de DRM
description: Inicializar exemplo de importação de DRM
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, código de exemplo
- SDK do Windows Media Format, exemplos de código
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), inicializar importação
- DRM (gerenciamento de direitos digitais), inicializar importação
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- APIs estendidas do cliente DRM, inicializar importação
- APIs estendidas do cliente, inicializar importação
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, código de exemplo
- APIs estendidas do cliente, código de exemplo
- APIs estendidas do cliente DRM, exemplos de código
- APIs estendidas do cliente, exemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160357"
---
# <a name="initialize-drm-import-example"></a>Inicializar exemplo de importação de DRM

O exemplo de código a seguir ilustra como inicializar um objeto gravador de DRM para a importação DRM:


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criar exemplo de chave de conteúdo**](create-content-key-example.md)
</dt> <dt>

[**Criar exemplo de chave de sessão**](create-session-key-example.md)
</dt> <dt>

[**Exemplos de importação de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




