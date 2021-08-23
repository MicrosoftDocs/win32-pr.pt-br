---
description: Este tópico descreve como verificar se um certificado dá suporte a um método de assinatura específico.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Verificar se um certificado dá suporte a um método de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098708"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Verificar se um certificado dá suporte a um método de assinatura

Este tópico descreve como verificar se um certificado dá suporte a um método de assinatura específico.

O **CryptXmlEnumAlgorithmInfo** na API de Criptografia da Microsoft enumera as propriedades de um certificado e é usado neste exemplo de código para enumerar os métodos de assinatura compatíveis com o certificado. Para usar **CryptXmlEnumAlgorithmInfo** para enumerar os métodos de assinatura compatíveis com o certificado, o chamador deve fornecer um método de retorno de chamada e uma estrutura de dados na chamada para **CryptXmlEnumAlgorithmInfo,** permitindo que ele passe dados para o método de retorno de chamada.

A estrutura de dados usada no próximo exemplo de código tem os seguintes campos:

| Campo                               | Descrição                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | Um **campo LPWSTR** que aponta para a cadeia de caracteres que contém o URI do algoritmo de assinatura a ser verificado.                             |
| **certificateAlgorithmInfo**        | Um ponteiro para uma estrutura **CRYPT \_ OID \_ INFO** que contém informações sobre um algoritmo de assinatura com suporte pelo certificado. |
| **userSignatureAlgorithmSupported** | Um **valor booliana** que indica se o algoritmo de assinatura é suportado pelo certificado.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



O método da API de Criptografia que verifica o certificado usa um método de retorno de chamada para retornar dados ao chamador. **CryptXmlEnumAlgorithmInfo** enumera os métodos de assinatura compatíveis com o certificado e chama o método de retorno de chamada para cada método de assinatura até que o método de retorno de chamada retorne **FALSE** ou até que todos os métodos de assinatura no certificado tenham sido enumerados.

O método de retorno de chamada no próximo exemplo de código pesquisa um método de assinatura passado por **CryptXmlEnumAlgorithmInfo** que corresponde ao método de assinatura fornecido pelo método de chamada. Quando uma corresponder é encontrada, o método de retorno de chamada verifica se o método de assinatura também é suportado pelo sistema. Se os métodos de assinatura corresponderem e o sistema tiver suporte, o método de assinatura será marcado como com suporte do sistema e o método de retorno de chamada **retornará FALSE.**


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



O exemplo de código a seguir envolve a funcionalidade de validação em um único método. Esse método retorna um **valor booliana** que indica se o certificado dá suporte ao método de assinatura e se o método de assinatura é compatível com o sistema.


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Carregar um certificado de um arquivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Usado neste exemplo**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**CRYPT \_ OID \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[API de criptografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Erros da API de Assinatura Digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erros de documento XPS](xps-document-errors.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
