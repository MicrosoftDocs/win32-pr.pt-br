---
description: Este tópico descreve como verificar se o sistema dá suporte a um método Digest.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Verificar se o sistema dá suporte a um método Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836887"
---
# <a name="verify-the-system-supports-a-digest-method"></a>Verificar se o sistema dá suporte a um método Digest

Este tópico descreve como verificar se o sistema dá suporte a um método Digest.

As assinaturas digitais XPS usam a API de criptografia, que fornece métodos para verificar se o sistema dá suporte a um método de resumo específico. Para usar a função **CryptXmlEnumAlgorithmInfo** da API de criptografia para enumerar os métodos de resumo que são suportados pelo sistema, o chamador deve fornecer um método de retorno de chamada e uma estrutura de dados. A função **CryptXmlEnumAlgorithmInfo** passa os dados de enumeração de volta para o chamador por meio do método de retorno de chamada.

A estrutura de dados usada neste exemplo é mostrada no exemplo de código a seguir e contém os seguintes campos:

| Campo                            | Descrição                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | Um campo **LPWSTR** que aponta para a cadeia de caracteres que contém o URI do algoritmo de resumo a ser verificado. |
| **userDigestAlgorithmSupported** | Um valor **booliano** que indica se há suporte para o algoritmo Digest no certificado.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



O método de API de criptografia que enumera os métodos Digest usa um método de retorno de chamada para retornar dados ao chamador. **CryptXmlEnumAlgorithmInfo** enumera os métodos de resumo que são suportados pelo sistema e chama o método de retorno de chamada para cada método de resumo que ele enumera, até que o método de retorno de chamada retorne **false** ou até que todos os métodos de resumo com suporte do sistema sejam enumerados. O método de retorno de chamada neste exemplo compara o método Digest passado pelo **CryptXmlEnumAlgorithmInfo** com o método Digest fornecido pelo método de chamada.


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



O exemplo de código a seguir encapsula a funcionalidade de validação em um único método, que retorna um valor **booliano** que indica se o sistema dá suporte ao método Digest.


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Carregar um certificado de um arquivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Usado neste exemplo**
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[API de criptografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Erros de API de assinatura digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erros de documento XPS](xps-document-errors.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
