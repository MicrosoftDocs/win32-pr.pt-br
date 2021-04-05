---
description: Este tópico descreve como assinar um documento XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Assinar um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828203"
---
# <a name="sign-a-document"></a><span data-ttu-id="c7846-103">Assinar um documento</span><span class="sxs-lookup"><span data-stu-id="c7846-103">Sign a Document</span></span>

<span data-ttu-id="c7846-104">Este tópico descreve como assinar um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c7846-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="c7846-105">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="c7846-106">Para assinar um documento XPS, primeiro carregue-o em um Gerenciador de assinatura, conforme descrito em [inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="c7846-107">Para assinar um documento que foi carregado em um Gerenciador de assinatura:</span><span class="sxs-lookup"><span data-stu-id="c7846-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="c7846-108">Crie uma instância de uma interface [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .</span><span class="sxs-lookup"><span data-stu-id="c7846-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="c7846-109">Defina a política de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7846-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="c7846-110">Defina o método de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7846-110">Set the signature method.</span></span> <span data-ttu-id="c7846-111">Constantes de cadeia de caracteres de URI de método de assinatura são definidas em cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="c7846-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="c7846-112">Para obter mais informações sobre valores de método de assinatura válidos, consulte [**IXpsSigningOptions:: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="c7846-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="c7846-113">Defina o método Digest.</span><span class="sxs-lookup"><span data-stu-id="c7846-113">Set the digest method.</span></span> <span data-ttu-id="c7846-114">As constantes de cadeia de caracteres de URI do método Digest são definidas em cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="c7846-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="c7846-115">Para obter informações sobre valores de método de resumo válidos, consulte [**IXpsSigningOptions:: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="c7846-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="c7846-116">Carregue o certificado conforme descrito em [carregar um certificado de um arquivo](load-a-certificate-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="c7846-117">Verifique se o certificado dá suporte ao método de assinatura, conforme descrito em [verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="c7846-118">Verifique se o método Digest tem suporte no sistema, conforme descrito em [verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="c7846-119">Se necessário, incorpore os certificados da cadeia de certificados confiáveis no documento XPS, conforme descrito em [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="c7846-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="c7846-120">Assine o documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c7846-120">Sign the XPS document.</span></span>

<span data-ttu-id="c7846-121">O exemplo de código a seguir ilustra como usar as etapas anteriores em um programa.</span><span class="sxs-lookup"><span data-stu-id="c7846-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a><span data-ttu-id="c7846-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7846-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c7846-123">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="c7846-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="c7846-124">Adicionar uma solicitação de assinatura a um documento XPS</span><span class="sxs-lookup"><span data-stu-id="c7846-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="c7846-125">Verificar assinaturas de documento</span><span class="sxs-lookup"><span data-stu-id="c7846-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="c7846-126">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="c7846-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="c7846-127">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="c7846-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="c7846-128">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="c7846-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="c7846-129">**IXpsSignatureManager:: createsignoptions**</span><span class="sxs-lookup"><span data-stu-id="c7846-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="c7846-130">**IXpsSignatureManager:: assinar**</span><span class="sxs-lookup"><span data-stu-id="c7846-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="c7846-131">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="c7846-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="c7846-132">**IXpsSigningOptions::SetDigestMethod**</span><span class="sxs-lookup"><span data-stu-id="c7846-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="c7846-133">**IXpsSigningOptions:: setpolicy**</span><span class="sxs-lookup"><span data-stu-id="c7846-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="c7846-134">**IXpsSigningOptions::SetSignatureMethod**</span><span class="sxs-lookup"><span data-stu-id="c7846-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="c7846-135">**\_política de assinatura de XPS \_**</span><span class="sxs-lookup"><span data-stu-id="c7846-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="c7846-136">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="c7846-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c7846-137">API de criptografia</span><span class="sxs-lookup"><span data-stu-id="c7846-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="c7846-138">Funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="c7846-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="c7846-139">Carregar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="c7846-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="c7846-140">Verificar se um certificado dá suporte a um método de assinatura</span><span class="sxs-lookup"><span data-stu-id="c7846-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="c7846-141">Verificar se o sistema dá suporte a um método Digest</span><span class="sxs-lookup"><span data-stu-id="c7846-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="c7846-142">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="c7846-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="c7846-143">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="c7846-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="c7846-144">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="c7846-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="c7846-145">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="c7846-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
