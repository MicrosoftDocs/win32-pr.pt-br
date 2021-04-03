---
title: Criar exemplo de chave de sessão
description: Criar exemplo de chave de sessão
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- SDK do Windows Media Format, chaves de sessão
- SDK do Windows Media Format, chaves de conteúdo
- SDK do Windows Media Format, código de exemplo
- SDK do Windows Media Format, exemplos de código
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
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006139"
---
# <a name="create-session-key-example"></a><span data-ttu-id="17f14-125">Criar exemplo de chave de sessão</span><span class="sxs-lookup"><span data-stu-id="17f14-125">Create Session Key Example</span></span>

<span data-ttu-id="17f14-126">A chave de sessão é usada para proteger a chave de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="17f14-126">The session key is used to protect the content key.</span></span> <span data-ttu-id="17f14-127">O código a seguir demonstra como criar uma chave de sessão, mas deixa os detalhes da geração de chave aleatória.</span><span class="sxs-lookup"><span data-stu-id="17f14-127">The following code demonstrates how to create a session key, but leaves out the details of random key generation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="17f14-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17f14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17f14-129">**Exemplos de importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="17f14-129">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




