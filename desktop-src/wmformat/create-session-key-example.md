---
title: Criar exemplo de chave de sessão
description: Criar exemplo de chave de sessão
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows SDK de Formato de Mídia, chaves de sessão
- Windows SDK de Formato de Mídia, chaves de conteúdo
- Windows SDK de Formato de Mídia, código de exemplo
- Windows SDK de Formato de Mídia, exemplos de código
- DRM (gerenciamento de direitos digitais), chaves de sessão
- DRM (gerenciamento de direitos digitais), chaves de sessão
- DRM (gerenciamento de direitos digitais), chaves de conteúdo
- DRM (gerenciamento de direitos digitais), chaves de conteúdo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- APIs estendidas do cliente DRM, chaves de sessão
- APIs estendidas do cliente, chaves de sessão
- APIs estendidas do cliente DRM, chaves de conteúdo
- APIs estendidas do cliente, chaves de conteúdo
- APIs estendidas do cliente DRM, código de exemplo
- APIs estendidas do cliente, código de exemplo
- APIs estendidas do cliente DRM, exemplos de código
- APIs estendidas do cliente, exemplos de código
- chaves de sessão
- chaves de conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef4a9c673b0aef24e010bff0f9a84beaf6321a81fe4ac8a8a9935c126983eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964135"
---
# <a name="create-session-key-example"></a>Criar exemplo de chave de sessão

A chave de sessão é usada para proteger a chave de conteúdo. O código a seguir demonstra como criar uma chave de sessão, mas deixa de fora os detalhes da geração de chave aleatória.


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos de importação de DRM**](drm-import-examples.md)
</dt> </dl>

 

 




