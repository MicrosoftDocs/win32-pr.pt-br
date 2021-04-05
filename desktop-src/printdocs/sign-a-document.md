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
# <a name="sign-a-document"></a>Assinar um documento

Este tópico descreve como assinar um documento XPS.

Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).

Para assinar um documento XPS, primeiro carregue-o em um Gerenciador de assinatura, conforme descrito em [inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md).

Para assinar um documento que foi carregado em um Gerenciador de assinatura:

1.  Crie uma instância de uma interface [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .
2.  Defina a política de assinatura.
3.  Defina o método de assinatura. Constantes de cadeia de caracteres de URI de método de assinatura são definidas em cryptxml. h. Para obter mais informações sobre valores de método de assinatura válidos, consulte [**IXpsSigningOptions:: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Defina o método Digest. As constantes de cadeia de caracteres de URI do método Digest são definidas em cryptxml. h. Para obter informações sobre valores de método de resumo válidos, consulte [**IXpsSigningOptions:: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Carregue o certificado conforme descrito em [carregar um certificado de um arquivo](load-a-certificate-from-a-file.md).
6.  Verifique se o certificado dá suporte ao método de assinatura, conforme descrito em [verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md).
7.  Verifique se o método Digest tem suporte no sistema, conforme descrito em [verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md).
8.  Se necessário, incorpore os certificados da cadeia de certificados confiáveis no documento XPS, conforme descrito em [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md).
9.  Assine o documento XPS.

O exemplo de código a seguir ilustra como usar as etapas anteriores em um programa.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Adicionar uma solicitação de assinatura a um documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Verificar assinaturas de documento](verify-document-signatures.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager:: createsignoptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager:: assinar**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions:: setpolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**\_política de assinatura de XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[API de criptografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Carregar um certificado de um arquivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Erros de API de assinatura digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erros de documento XPS](xps-document-errors.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
