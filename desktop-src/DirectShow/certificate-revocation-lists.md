---
description: Listas de Revogação de Certificados
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listas de Revogação de Certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105769220"
---
# <a name="certificate-revocation-lists"></a>Listas de Revogação de Certificados

Este tópico descreve como examinar a CRL (lista de certificados revogados) para drivers revogados ao usar o protocolo COPP (certificado de proteção de saída).

A CRL contém resumos de certificados revogados e pode ser fornecida e assinada somente pela Microsoft. A CRL é distribuída por meio de licenças do DRM (gerenciamento de direitos digitais). A CRL pode revogar qualquer certificado na cadeia de certificados do driver. Se qualquer certificado na cadeia for revogado, esse certificado e todos os certificados abaixo dele na cadeia também serão revogados.

Para obter a CRL, o aplicativo deve usar o Windows Media Format SDK, versão 9 ou posterior e executar as seguintes etapas:

1.  Chame **WMCreateReader** para criar o objeto leitor do Windows Media Format SDK.
2.  Consulte o objeto de leitor para a interface **IWMDRMReader** .
3.  Chame **IWMDRMReader:: GetDRMProperty** com um valor de g \_ wszWMDRMNet \_ revogação para obter a CRL. Você deve chamar esse método duas vezes: uma vez para obter o tamanho do buffer a ser alocado e uma vez para preencher o buffer. A segunda chamada retorna uma cadeia de caracteres que contém a CRL. A cadeia de caracteres inteira é codificada em base 64.
4.  Decodifique a cadeia de caracteres codificada em base 64. Você pode usar a função **CryptStringToBinary** para fazer isso. Essa função faz parte do CryptoAPI.

> [!Note]  
> Para usar a interface **IWMDRMReader** , você deve obter uma biblioteca de DRM estática da Microsoft e vincular seu aplicativo a esse arquivo de biblioteca. Para obter mais informações, consulte o tópico "obtendo a biblioteca de DRM necessária" na documentação do SDK do Windows Media Format.

 

Se a CRL não estiver presente no computador do usuário, o método **GetDRMProperty** retornará a \_ \_ \_ Propriedade sem suporte do NS E DRM \_ . Atualmente, a única maneira de obter a CRL é adquirir uma licença DRM.

O código a seguir mostra uma função que retorna a CRL:


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



Em seguida, o aplicativo deve verificar se a CRL é válida. Para fazer isso, verifique se o certificado de CRL, que faz parte da CRL, está assinado diretamente pelo certificado raiz da Microsoft e tem o valor do elemento SignCRL definido como 1. Além disso, verifique a assinatura da CRL.

Depois que a CRL é verificada, o aplicativo pode armazená-la. O número de versão da CRL também deve ser verificado antes do armazenamento para que o aplicativo sempre armazene a versão mais recente.

A CRL tem o formato a seguir.



| Seção            | Sumário                                                             |
|--------------------|----------------------------------------------------------------------|
| parâmetro             | version32-bit CRL de 32 bits-número de entradas                           |
| Entradas de revogação | Várias entradas de revogação de 160 bits                                  |
| Certificado        | certificado de comprimento lengthVariable do certificado de 32 bits                 |
| Assinatura          | assinatura de 8 bits type16-bit assinatura lengthVariable-assinatura de comprimento |



 

> [!Note]  
> Todos os valores inteiros não são assinados e são representados na notação big endian (ordem de bytes de rede).

 

Descrições da seção de CRL

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga
</dt> <dd>

O cabeçalho contém o número de versão da CRL e o número de entradas de revogação na CRL. Uma CRL pode conter zero ou mais entradas.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entradas de revogação
</dt> <dd>

Cada entrada de revogação é o resumo de 160 bits de um certificado revogado. Compare esse Resumo com o elemento DigestValue dentro do certificado.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate
</dt> <dd>

A seção de certificado contém um valor de 32 bits que indica o comprimento (em bytes) do certificado XML e sua cadeia de certificados, juntamente com uma matriz de bytes que contém o certificado XML da autoridade de certificação (CA) e a cadeia de certificados que tem a Microsoft como raiz. O certificado deve ser assinado por uma autoridade de certificação que tenha autoridade para emitir CRLs.

> [!Note]  
> O certificado não deve ser encerrado em nulo.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature
</dt> <dd>

A seção assinatura contém o tipo e o comprimento da assinatura e a própria assinatura digital. O tipo de 8 bits é definido como 2 para indicar que ele usa SHA-1 com criptografia RSA de 1024 bits. O comprimento é um valor de 16 bits que contém o comprimento da assinatura digital em bytes. A assinatura digital é calculada em todas as seções anteriores da CRL.

A assinatura é calculada usando o esquema de assinatura digital RSASSA-PSS que é definido no PKCS \# 1 (versão 2,1). A função de hash é SHA-1, que é definida em padrão FIPS (FIPS) 180-2, e a função de geração de máscara é MGF1, que é definida na seção B. 2.1 no PKCS \# 1 (versão 2,1). As operações RSASP1 e RSAVP1 usam RSA com um módulo de 1024 bits com um expoente de verificação de 65537.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



