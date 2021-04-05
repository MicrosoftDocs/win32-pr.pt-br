---
title: Exemplo de criptografia de exemplo de mídia
description: Exemplo de criptografia de exemplo de mídia
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- SDK do Windows Media Format, criptografia de exemplo de mídia
- SDK do Windows Media Format, código de exemplo
- SDK do Windows Media Format, exemplos de código
- DRM (gerenciamento de direitos digitais), criptografia de exemplo de mídia
- DRM (gerenciamento de direitos digitais), criptografia de exemplo de mídia
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- APIs estendidas do cliente DRM, criptografia de exemplo de mídia
- APIs estendidas do cliente, criptografia de exemplo de mídia
- APIs estendidas do cliente DRM, código de exemplo
- APIs estendidas do cliente, código de exemplo
- APIs estendidas do cliente DRM, exemplos de código
- APIs estendidas do cliente, exemplos de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006114"
---
# <a name="media-sample-encryption-example"></a><span data-ttu-id="f15af-118">Exemplo de criptografia de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="f15af-118">Media Sample Encryption Example</span></span>

<span data-ttu-id="f15af-119">O exemplo incompleto a seguir demonstra como criptografar um exemplo de mídia usando a criptografia DRM.</span><span class="sxs-lookup"><span data-stu-id="f15af-119">The following incomplete example demonstrates how to encrypt a media sample using DRM encryption.</span></span> <span data-ttu-id="f15af-120">O algoritmo de criptografia RC4 saiu do exemplo devido a restrições de espaço.</span><span class="sxs-lookup"><span data-stu-id="f15af-120">The RC4 encryption algorithm has been left out of the example due to space restrictions.</span></span>


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f15af-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f15af-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f15af-122">**Exemplos de importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="f15af-122">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




