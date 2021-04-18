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
# <a name="embed-certificate-chains-in-a-document"></a>Inserir cadeias de certificados em um documento

Este tópico descreve como inserir os certificados que compõem uma cadeia de certificados em um documento XPS. Uma cadeia de certificados consiste em todos os certificados, exceto o certificado raiz, que são necessários para certificar a entidade identificada pelo certificado final.

Para inserir uma cadeia de certificados em um documento XPS, primeiro crie a cadeia de certificados, conforme ilustrado no exemplo de código a seguir.

O método **CreateCertificateChain** no exemplo de código aceita *certificateStore* como um parâmetro, que é um valor de **HCERTSTORE** . Se esse valor for **nulo**, os certificados serão recuperados do servidor de certificado do computador cliente. Se o valor for o identificador de um repositório de certificados, os certificados serão recuperados do armazenamento referenciado por *certificateStore* , bem como do servidor de certificados do computador cliente.


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



O exemplo de código a seguir cria uma cadeia de certificados de certificados e, em seguida, adiciona esses certificados a um documento XPS. Observe que o [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) cria a cadeia de certificados na qual o certificado de autenticação é o primeiro e o certificado raiz é o último. O certificado de autenticação e o certificado raiz não são adicionados neste exemplo. Os certificados de autenticação serão adicionados com uma chamada ao método [**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , que deve ser o último método de assinatura chamado no documento. O certificado raiz não é adicionado quando o documento é assinado, pois ele deve ser fornecido pelo servidor de certificado do computador cliente quando a assinatura é validada.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Carregar um certificado de um arquivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Usado neste exemplo**
</dt> <dt>

[**contexto do certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**\_informações de OID cript \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[API de criptografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Certificados digitais](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Cadeias de certificados](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Verificação de confiança de certificado](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[Erros de API de assinatura digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erros de documento XPS](xps-document-errors.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
