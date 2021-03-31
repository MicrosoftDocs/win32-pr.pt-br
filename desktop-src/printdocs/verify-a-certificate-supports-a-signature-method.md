---
description: Este tópico descreve como verificar se um certificado dá suporte a um método de assinatura específico.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Verificar se um certificado dá suporte a um método de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836886"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="e62e5-103">Verificar se um certificado dá suporte a um método de assinatura</span><span class="sxs-lookup"><span data-stu-id="e62e5-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="e62e5-104">Este tópico descreve como verificar se um certificado dá suporte a um método de assinatura específico.</span><span class="sxs-lookup"><span data-stu-id="e62e5-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="e62e5-105">O **CryptXmlEnumAlgorithmInfo** na API de criptografia da Microsoft enumera as propriedades de um certificado e é usado neste exemplo de código para enumerar os métodos de assinatura aos quais o certificado dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e62e5-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="e62e5-106">Para usar **CryptXmlEnumAlgorithmInfo** para enumerar os métodos de assinatura aos quais o certificado dá suporte, o chamador deve fornecer um método de retorno de chamada e uma estrutura de dados na chamada para **CryptXmlEnumAlgorithmInfo**, permitindo que ele passe dados para o método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e62e5-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="e62e5-107">A estrutura de dados usada no próximo exemplo de código tem os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="e62e5-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="e62e5-108">Campo</span><span class="sxs-lookup"><span data-stu-id="e62e5-108">Field</span></span>                               | <span data-ttu-id="e62e5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e62e5-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e62e5-110">**userSignatureAlgorithmToCheck**</span><span class="sxs-lookup"><span data-stu-id="e62e5-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="e62e5-111">Um campo **LPWSTR** que aponta para a cadeia de caracteres que contém o URI do algoritmo de assinatura a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="e62e5-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="e62e5-112">**certificateAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="e62e5-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="e62e5-113">Um ponteiro para uma estrutura de **\_ \_ informações de OID cript** que contém informações sobre um algoritmo de assinatura que é suportado pelo certificado.</span><span class="sxs-lookup"><span data-stu-id="e62e5-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="e62e5-114">**userSignatureAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="e62e5-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="e62e5-115">Um valor **booliano** que indica se há suporte para o algoritmo de assinatura no certificado.</span><span class="sxs-lookup"><span data-stu-id="e62e5-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="e62e5-116">O método de API de criptografia que verifica o certificado usa um método de retorno de chamada para retornar dados ao chamador.</span><span class="sxs-lookup"><span data-stu-id="e62e5-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="e62e5-117">**CryptXmlEnumAlgorithmInfo** enumera os métodos de assinatura aos quais o certificado dá suporte e chama o método de retorno de chamada para cada método de assinatura até que o método de retorno de chamada retorne **false** ou até que todos os métodos de assinatura no certificado tenham sido enumerados.</span><span class="sxs-lookup"><span data-stu-id="e62e5-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="e62e5-118">O método de retorno de chamada no próximo exemplo de código pesquisa um método de assinatura passado por **CryptXmlEnumAlgorithmInfo** que corresponde ao método de assinatura fornecido pelo método de chamada.</span><span class="sxs-lookup"><span data-stu-id="e62e5-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="e62e5-119">Quando uma correspondência é encontrada, o método de retorno de chamada verifica se o método de assinatura também tem suporte no sistema.</span><span class="sxs-lookup"><span data-stu-id="e62e5-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="e62e5-120">Se os métodos de assinatura corresponderem e tiverem suporte do sistema, o método de assinatura será marcado como com suporte do sistema e o método de retorno de chamada retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


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



<span data-ttu-id="e62e5-121">O exemplo de código a seguir encapsula a funcionalidade de validação em um único método.</span><span class="sxs-lookup"><span data-stu-id="e62e5-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="e62e5-122">Esse método retorna um valor **booliano** que indica se o certificado oferece suporte ao método de assinatura e se o método de assinatura tem suporte no sistema.</span><span class="sxs-lookup"><span data-stu-id="e62e5-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e62e5-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e62e5-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e62e5-124">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="e62e5-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="e62e5-125">Carregar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="e62e5-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="e62e5-126">Verificar se o sistema dá suporte a um método Digest</span><span class="sxs-lookup"><span data-stu-id="e62e5-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="e62e5-127">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="e62e5-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="e62e5-128">**Usado neste exemplo**</span><span class="sxs-lookup"><span data-stu-id="e62e5-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="e62e5-129">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="e62e5-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="e62e5-130">**\_informações de OID cript \_**</span><span class="sxs-lookup"><span data-stu-id="e62e5-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="e62e5-131">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="e62e5-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="e62e5-132">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="e62e5-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="e62e5-133">API de criptografia</span><span class="sxs-lookup"><span data-stu-id="e62e5-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="e62e5-134">Funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="e62e5-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="e62e5-135">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="e62e5-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="e62e5-136">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="e62e5-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="e62e5-137">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="e62e5-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
