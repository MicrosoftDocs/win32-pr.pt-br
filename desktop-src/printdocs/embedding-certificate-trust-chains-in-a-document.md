---
description: Este tópico descreve como inserir os certificados que compõem uma cadeia de certificados em um documento XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Inserir cadeias de certificados em um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee6476e0c187cf1a62915f0a3ab2b7949586baa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807265"
---
# <a name="embed-certificate-chains-in-a-document"></a><span data-ttu-id="2fbb3-103">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="2fbb3-103">Embed Certificate Chains in a Document</span></span>

<span data-ttu-id="2fbb3-104">Este tópico descreve como inserir os certificados que compõem uma cadeia de certificados em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-104">This topic describes how to embed the certificates that make up a certificate chain into an XPS document.</span></span> <span data-ttu-id="2fbb3-105">Uma cadeia de certificados consiste em todos os certificados, exceto o certificado raiz, que são necessários para certificar a entidade identificada pelo certificado final.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-105">A certificate chain consists of all the certificates, except the root certificate, that are needed to certify the subject identified by the end certificate.</span></span>

<span data-ttu-id="2fbb3-106">Para inserir uma cadeia de certificados em um documento XPS, primeiro crie a cadeia de certificados, conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-106">To embed a certificate chain into an XPS document, first create the certificate chain as illustrated in the following code example.</span></span>

<span data-ttu-id="2fbb3-107">O método **CreateCertificateChain** no exemplo de código aceita *certificateStore* como um parâmetro, que é um valor de **HCERTSTORE** .</span><span class="sxs-lookup"><span data-stu-id="2fbb3-107">The **CreateCertificateChain** method in the code example accepts *certificateStore* as a parameter, which is an **HCERTSTORE** value.</span></span> <span data-ttu-id="2fbb3-108">Se esse valor for **nulo**, os certificados serão recuperados do servidor de certificado do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-108">If this value is **NULL**, the certificates will be retrieved from the client computer's certificate server.</span></span> <span data-ttu-id="2fbb3-109">Se o valor for o identificador de um repositório de certificados, os certificados serão recuperados do armazenamento referenciado por *certificateStore* , bem como do servidor de certificados do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-109">If the value is the handle to a certificate store, the certificates will be retrieved from that store referenced by *certificateStore* as well as from the client computer's certificate server.</span></span>


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



<span data-ttu-id="2fbb3-110">O exemplo de código a seguir cria uma cadeia de certificados de certificados e, em seguida, adiciona esses certificados a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-110">The following code example creates a certificate chain from certificates and then adds these certificates to an XPS document.</span></span> <span data-ttu-id="2fbb3-111">Observe que o [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) cria a cadeia de certificados na qual o certificado de autenticação é o primeiro e o certificado raiz é o último.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-111">Note that [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) creates the certificate chain in which the signing certificate is first and the root certificate is last.</span></span> <span data-ttu-id="2fbb3-112">O certificado de autenticação e o certificado raiz não são adicionados neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-112">The signing certificate and the root certificate are not added in this example.</span></span> <span data-ttu-id="2fbb3-113">Os certificados de autenticação serão adicionados com uma chamada ao método [**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , que deve ser o último método de assinatura chamado no documento.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-113">The signing certificates will be added with a call to the [**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) method, which should be the last signature method called on the document.</span></span> <span data-ttu-id="2fbb3-114">O certificado raiz não é adicionado quando o documento é assinado, pois ele deve ser fornecido pelo servidor de certificado do computador cliente quando a assinatura é validada.</span><span class="sxs-lookup"><span data-stu-id="2fbb3-114">The root certificate is not added when the document is signed, because it must be provided by the client computer's certificate server when the signature is validated.</span></span>


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2fbb3-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fbb3-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2fbb3-116">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="2fbb3-117">Carregar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="2fbb3-117">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="2fbb3-118">Verificar se um certificado dá suporte a um método de assinatura</span><span class="sxs-lookup"><span data-stu-id="2fbb3-118">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="2fbb3-119">Verificar se o sistema dá suporte a um método Digest</span><span class="sxs-lookup"><span data-stu-id="2fbb3-119">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

<span data-ttu-id="2fbb3-120">**Usado neste exemplo**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-120">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="2fbb3-121">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-121">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="2fbb3-122">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-122">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="2fbb3-123">**\_informações de OID cript \_**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-123">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[<span data-ttu-id="2fbb3-124">**IOpcCertificateSet**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-124">**IOpcCertificateSet**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[<span data-ttu-id="2fbb3-125">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-125">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

<span data-ttu-id="2fbb3-126">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="2fbb3-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="2fbb3-127">API de criptografia</span><span class="sxs-lookup"><span data-stu-id="2fbb3-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="2fbb3-128">Funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="2fbb3-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="2fbb3-129">Certificados digitais</span><span class="sxs-lookup"><span data-stu-id="2fbb3-129">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[<span data-ttu-id="2fbb3-130">Cadeias de certificados</span><span class="sxs-lookup"><span data-stu-id="2fbb3-130">Certificate Chains</span></span>](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[<span data-ttu-id="2fbb3-131">Verificação de confiança de certificado</span><span class="sxs-lookup"><span data-stu-id="2fbb3-131">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[<span data-ttu-id="2fbb3-132">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="2fbb3-132">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="2fbb3-133">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="2fbb3-133">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="2fbb3-134">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="2fbb3-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
