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
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="de71c-103">Verificar se o sistema dá suporte a um método Digest</span><span class="sxs-lookup"><span data-stu-id="de71c-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="de71c-104">Este tópico descreve como verificar se o sistema dá suporte a um método Digest.</span><span class="sxs-lookup"><span data-stu-id="de71c-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="de71c-105">As assinaturas digitais XPS usam a API de criptografia, que fornece métodos para verificar se o sistema dá suporte a um método de resumo específico.</span><span class="sxs-lookup"><span data-stu-id="de71c-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="de71c-106">Para usar a função **CryptXmlEnumAlgorithmInfo** da API de criptografia para enumerar os métodos de resumo que são suportados pelo sistema, o chamador deve fornecer um método de retorno de chamada e uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="de71c-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="de71c-107">A função **CryptXmlEnumAlgorithmInfo** passa os dados de enumeração de volta para o chamador por meio do método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="de71c-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="de71c-108">A estrutura de dados usada neste exemplo é mostrada no exemplo de código a seguir e contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="de71c-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="de71c-109">Campo</span><span class="sxs-lookup"><span data-stu-id="de71c-109">Field</span></span>                            | <span data-ttu-id="de71c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="de71c-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de71c-111">**userDigestAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="de71c-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="de71c-112">Um campo **LPWSTR** que aponta para a cadeia de caracteres que contém o URI do algoritmo de resumo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="de71c-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="de71c-113">**userDigestAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="de71c-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="de71c-114">Um valor **booliano** que indica se há suporte para o algoritmo Digest no certificado.</span><span class="sxs-lookup"><span data-stu-id="de71c-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="de71c-115">O método de API de criptografia que enumera os métodos Digest usa um método de retorno de chamada para retornar dados ao chamador.</span><span class="sxs-lookup"><span data-stu-id="de71c-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="de71c-116">**CryptXmlEnumAlgorithmInfo** enumera os métodos de resumo que são suportados pelo sistema e chama o método de retorno de chamada para cada método de resumo que ele enumera, até que o método de retorno de chamada retorne **false** ou até que todos os métodos de resumo com suporte do sistema sejam enumerados.</span><span class="sxs-lookup"><span data-stu-id="de71c-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="de71c-117">O método de retorno de chamada neste exemplo compara o método Digest passado pelo **CryptXmlEnumAlgorithmInfo** com o método Digest fornecido pelo método de chamada.</span><span class="sxs-lookup"><span data-stu-id="de71c-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


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



<span data-ttu-id="de71c-118">O exemplo de código a seguir encapsula a funcionalidade de validação em um único método, que retorna um valor **booliano** que indica se o sistema dá suporte ao método Digest.</span><span class="sxs-lookup"><span data-stu-id="de71c-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="de71c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de71c-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="de71c-120">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="de71c-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="de71c-121">Carregar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="de71c-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="de71c-122">Verificar se um certificado dá suporte a um método de assinatura</span><span class="sxs-lookup"><span data-stu-id="de71c-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="de71c-123">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="de71c-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="de71c-124">**Usado neste exemplo**</span><span class="sxs-lookup"><span data-stu-id="de71c-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="de71c-125">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="de71c-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="de71c-126">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="de71c-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="de71c-127">API de criptografia</span><span class="sxs-lookup"><span data-stu-id="de71c-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="de71c-128">Funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="de71c-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="de71c-129">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="de71c-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="de71c-130">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="de71c-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="de71c-131">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="de71c-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
