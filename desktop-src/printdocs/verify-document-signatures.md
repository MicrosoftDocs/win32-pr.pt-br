---
description: Este tópico descreve como verificar as assinaturas em um documento XPS e como verificar os certificados relacionados a essas assinaturas.
ms.assetid: fd12abaf-dc0f-4db1-837d-c116627bcc7e
title: Verificar assinaturas e certificados de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47dfee91437f7cc36e754e8c1f97fa89cd2387af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790572"
---
# <a name="verify-document-signatures-and-certificates"></a><span data-ttu-id="731d8-103">Verificar assinaturas e certificados de documentos</span><span class="sxs-lookup"><span data-stu-id="731d8-103">Verify Document Signatures and Certificates</span></span>

<span data-ttu-id="731d8-104">Este tópico descreve como verificar as assinaturas em um documento XPS e como verificar os certificados relacionados a essas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="731d8-104">This topic describes how to verify the signatures in an XPS document and how to verify the certificates that are related to those signatures.</span></span>

<span data-ttu-id="731d8-105">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="731d8-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="731d8-106">O exemplo de código a seguir verifica as assinaturas digitais encontradas em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="731d8-106">The following code example checks the digital signatures that are found in an XPS document.</span></span>

<span data-ttu-id="731d8-107">Para verificar as assinaturas em um documento XPS, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="731d8-107">To check the signatures in an XPS document, perform the following steps:</span></span>

1.  <span data-ttu-id="731d8-108">Carregue o documento em um Gerenciador de assinatura, conforme descrito em [inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="731d8-108">Load the document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="731d8-109">Obtenha a coleção de assinaturas do Gerenciador de assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="731d8-109">Get the collection of signatures from the digital signature manager.</span></span>
3.  <span data-ttu-id="731d8-110">Obtenha o número de assinaturas na coleção.</span><span class="sxs-lookup"><span data-stu-id="731d8-110">Get the number of signatures in the collection.</span></span>
4.  <span data-ttu-id="731d8-111">Para cada assinatura na coleção, chame o método [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="731d8-111">For each signature in the collection, call the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method as shown in the code example that follows.</span></span>


```C++
HRESULT
VerifyAllDigitalSignaturesAndAuthenticateCertificates(
    IXpsSignatureManager *signatureManager
)
{
    HRESULT                       hr                              = S_OK;
    IXpsSignature                 *signature                      = NULL;
    IXpsSignatureCollection       *signaturesInDocument           = NULL;
    UINT32                        numberOfSignaturesInDocument    = NULL;

    hr = signatureManager->GetSignatures(&signaturesInDocument);
    if (SUCCEEDED(hr)) {
        hr = signaturesInDocument->GetCount(&numberOfSignaturesInDocument);
    }

    if (SUCCEEDED(hr)) {
        // Check each signature in the XPS document that was opened in
        //  the signature manager.
        for (UINT32 index = 0; index < numberOfSignaturesInDocument; index++)
        {
            // Get the signature in the current index of the 
            //  IXpsSignatureCollection object
            hr = signaturesInDocument->GetAt(index, &signature);

            if (SUCCEEDED(hr)) {
                PCCERT_CONTEXT       signingCertificate = NULL;
                XPS_SIGNATURE_STATUS signatureStatus; 

                signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                // Verify the signature and authenticate 
                //  its signing certificate
                hr = VerifySignatureAndCertificates (
                        signature,
                        &signingCertificate,
                        &signatureStatus);
                if (FAILED(hr)) {
                    // If a FACILITY_SECURITY error code is returned then 
                    //  the current certificate was not the 
                    //    signing certificate, so continue with 
                    //  the enumeration.
                    if (HRESULT_FACILITY(hr) != FACILITY_SECURITY)
                    {
                        // If the error was not a FACILITY_SECURITY error  
                        //  then exit and return the error
                        break; // out of for loop
                    }
                }
                // release pointers for next loop
                if (NULL != signature) {
                    signature->Release(); 
                    signature = NULL; 
                }
                if (NULL != signingCertificate) {
                    CertFreeCertificateContext (signingCertificate); 
                    signingCertificate = NULL;
                }
            }
        }
    }
    if (NULL != signaturesInDocument) signaturesInDocument->Release();
    
    return hr;
}
```



<span data-ttu-id="731d8-112">Para verificar uma assinatura digital, primeiro verifique a assinatura criada pelo certificado de autenticação e, em seguida, valide o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="731d8-112">To verify a digital signature, first verify the signature created by the signing certificate, then validate the signing certificate.</span></span> <span data-ttu-id="731d8-113">O método de validação usado no exemplo de código a seguir armazena em cache os certificados em um repositório de certificados temporário, que as funções da API de criptografia usam quando são chamadas posteriormente neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="731d8-113">The validation method used in the following code example caches the certificates in a temporary certificate store, which the Crypto API functions use when they are called later in this example.</span></span>

<span data-ttu-id="731d8-114">Para criar um repositório de certificados temporário, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="731d8-114">To create a temporary certificate store, perform the following steps:</span></span>

1.  <span data-ttu-id="731d8-115">Crie um repositório de certificados temporário para manter os certificados usados pela assinatura.</span><span class="sxs-lookup"><span data-stu-id="731d8-115">Create a temporary certificate store to hold the certificates used by the signature.</span></span>
2.  <span data-ttu-id="731d8-116">Itere pelo conjunto de certificados da assinatura e carregue cada certificado no repositório de certificados temporário.</span><span class="sxs-lookup"><span data-stu-id="731d8-116">Iterate through the signature's certificate set, and load each certificate into the temporary certificate store.</span></span>


```C++
HRESULT VerifySignatureAndCertificates (
    IXpsSignature           *signature,
    PCCERT_CONTEXT          *signingCertificate,
    XPS_SIGNATURE_STATUS    *signatureStatus
)
{
    HRESULT                         hr                        = S_OK;
    BOOL                            moreCertificates          = FALSE;
    IOpcCertificateEnumerator       *certificatesInSignature  = NULL;
    
    HCERTSTORE                      signatureCertificateStore = NULL;
    
    // Create a temporary certificate store.  
    signatureCertificateStore = CertOpenStore(
        CERT_STORE_PROV_MEMORY, 
        X509_ASN_ENCODING, 
        NULL, 
        0, 
        NULL);

    // Create a certificate enumerator to store the certificates 
    //  that are associated with the current signature.
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);

    if (SUCCEEDED(hr))
    {
    // We need to call the MoveNext method to initialize the enumerator.
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature, 
        //  and add each one to the temporary certificate store.  
        //  This temporary  certificate store simplifies 
        //  authentication of the signing certificate.
        while (moreCertificates)
        {
            PCCERT_CONTEXT certificate  = NULL;
            hr = certificatesInSignature->GetCurrent(&certificate);
            if (SUCCEEDED(hr))
            {
                // got the next certificate so
                // add the current certificate to the temporary certificate store.
                if (!CertAddCertificateContextToStore(signatureCertificateStore,
                    certificate,
                    CERT_STORE_ADD_REPLACE_EXISTING,
                    NULL))
                {
                    hr = E_FAIL;
                    // ERROR: could not add the certificate to the certificate store
                    break; // out of while loop
                }
                CertFreeCertificateContext (certificate);
            }
            else
            {
                // unable to get the certificate so skip
            }

            // move to next certificate in set
            if (FAILED(hr = certificatesInSignature->MoveNext(&moreCertificates)))
            {
                // ERROR: could not move to the next certificate in the enumerator
                break; // out of while loop
            }
            // moreCertificates == FALSE when the end of the set has been reached.
        }//End while
    }
    if (NULL != certificatesInSignature) certificatesInSignature->Release();

```



<span data-ttu-id="731d8-117">Para verificar a assinatura digital e o certificado usado para assinar o documento, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="731d8-117">To verify the digital signature and the certificate used to sign the document, perform the following steps:</span></span>

1.  <span data-ttu-id="731d8-118">Localize o certificado de autenticação Iterando pelos certificados que são usados pela assinatura.</span><span class="sxs-lookup"><span data-stu-id="731d8-118">Find the signing certificate by iterating through the certificates that are used by the signature.</span></span>
2.  <span data-ttu-id="731d8-119">Teste o certificado verificando a assinatura em relação ao certificado.</span><span class="sxs-lookup"><span data-stu-id="731d8-119">Test the certificate by verifying the signature against the certificate.</span></span> <span data-ttu-id="731d8-120">O certificado de autenticação é encontrado quando o método [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) retorna [**um \_ \_ status de assinatura XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) de **status de \_ assinatura XPS \_ \_ válido** ou **status de \_ assinatura XPS \_ \_ questionável** e não retorna um erro de **\_ segurança de recurso** .</span><span class="sxs-lookup"><span data-stu-id="731d8-120">The signing certificate is found when the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method returns an [**XPS\_SIGNATURE\_STATUS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) of **XPS\_SIGNATURE\_STATUS\_VALID** or **XPS\_SIGNATURE\_STATUS\_QUESTIONABLE**, and does not return a **FACILITY\_SECURITY** error.</span></span>


```C++
    // Reset the enumerator
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);
    if (SUCCEEDED (hr))
    {
        moreCertificates = FALSE;
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature,
        //  and call the IXpsSignature.Verify() method
        //  on each certificate.  
        // A signature can include an entire certificate chain, and so 
        //  only one of the certificates found in this enumeration 
        //  is the certificate that was used to sign the package. 
        //  The signing certificate is the one to authenticate.  
        // To find the signing certificate,  iterate through 
        //  the certificates in the signature and select the certificate that 
        //  returns an XPS_SIGNATURE_STATUS of XPS_SIGNATURE_STATUS_VALID
        //  or XPS_SIGNATURE_STATUS_QUESTIONABLE and does not return a
        //  FACILITY_SECURITY error.
        XPS_SIGNATURE_STATUS localSignatureStatus;
        localSignatureStatus = XPS_SIGNATURE_STATUS_INCOMPLIANT;
        do
        {
            PCCERT_CONTEXT certificate = NULL;
            DWORD certificateStatus = NULL;

            if (FAILED(hr = certificatesInSignature->GetCurrent(&certificate)))
            {
                // We will skip corrupted certificates
                // free this one and move to the next
                CertFreeCertificateContext (certificate);
                hr = certificatesInSignature->MoveNext(&moreCertificates);
                if (FAILED(hr))
                {
                    // ERROR: could not move to the next 
                    //  certificate in the enumerator
                    break; // out of do loop with failed hr
                }
                // continue with next loop iteration
                continue;
            }
            
            // Verify that the signature conforms to the XPS signing policy.
            hr = signature->Verify(certificate, &localSignatureStatus);
            if (FAILED(hr))
            {
                // If a FACILITY_SECURITY error code is returned, then the
                //  current certificate was not the signing certificate,
                //  so continue to the next certificate.
                if (HRESULT_FACILITY(hr) == FACILITY_SECURITY)
                {
                    // free this one and move to the next
                    CertFreeCertificateContext (certificate);
                    hr = certificatesInSignature->MoveNext(&moreCertificates);
                    if (FAILED(hr))
                    {
                        // ERROR: could not move to the next certificate 
                        //  in the enumerator
                        break; // out of do loop with failed hr
                    }
                    continue;
                }
                // ERROR: An attempt to verify the signature has failed
                break; // out of do loop with failed hr
            }
            // if verification was successful, localSignatureStatus will
            //  contain the status of the signature.
            //
            // do loop continues in next code example
```



<span data-ttu-id="731d8-121">Quando o certificado de autenticação for encontrado, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="731d8-121">When the signing certificate has been found, perform the following steps:</span></span>

1.  <span data-ttu-id="731d8-122">Salve o status de assinatura retornado.</span><span class="sxs-lookup"><span data-stu-id="731d8-122">Save the returned signature status.</span></span>
2.  <span data-ttu-id="731d8-123">Atualize o status local, se necessário, para executar os testes de certificado subsequentes:</span><span class="sxs-lookup"><span data-stu-id="731d8-123">Update the local status, if necessary, to perform subsequent certificate tests:</span></span>
    1.  <span data-ttu-id="731d8-124">Se o status da assinatura for bem-sucedido, defina o status local para questionável a fim de testar os certificados.</span><span class="sxs-lookup"><span data-stu-id="731d8-124">If the signature status is successful, set the local status to questionable in order to test the certificates.</span></span>
    2.  <span data-ttu-id="731d8-125">Se o status da assinatura for incompatível, deixe o status local como incompatível.</span><span class="sxs-lookup"><span data-stu-id="731d8-125">If the signature status is incompliant, leave the local status as incompliant.</span></span>
    3.  <span data-ttu-id="731d8-126">Se o status da assinatura for rompido ou incompleto, defina o status local como rompido.</span><span class="sxs-lookup"><span data-stu-id="731d8-126">If the signature status is broken or incomplete, set the local status to broken.</span></span>

<span data-ttu-id="731d8-127">Um status de assinatura **de \_ \_ \_ incompatibilidade de status de assinatura XPS** significa que partes do documento XPS que não deveriam ter sido assinadas foram assinadas ou partes do documento XPS que deveriam ter sido assinadas não foram.</span><span class="sxs-lookup"><span data-stu-id="731d8-127">A signature status of **XPS\_SIGNATURE\_STATUS\_INCOMPLIANT** means that parts of the XPS document that should not have been signed were signed, or parts of the XPS document that should have been signed were not.</span></span> <span data-ttu-id="731d8-128">Se [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) retornar esse status de assinatura, a verificação adicional da assinatura será desnecessária.</span><span class="sxs-lookup"><span data-stu-id="731d8-128">If [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) returns this signature status, further checking of the signature will be unnecessary.</span></span>


```C++
            // continuing do loop from previous code example
            *signingCertificate = certificate;
            *signatureStatus = localSignatureStatus;
            
            // note that this test should only downgrade the 
            // signature status, it should not upgrade it.
            switch (localSignatureStatus) {
                case XPS_SIGNATURE_STATUS_VALID:
                case XPS_SIGNATURE_STATUS_QUESTIONABLE:
                    // the signature is valid or questionable so
                    // save the actual status and set the new status
                    // to questionable so the certificates will be checked.
                    localSignatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLIANT:
                    // the signature is not compliant 
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLETE:
                case XPS_SIGNATURE_STATUS_BROKEN:
                    // The Windows 7 XPS viewer displays incomplete signatures
                    // and broken signatures as broken.
                    *signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    localSignatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    break;

                default:
                    // there should be no other possible status values
                    break;
            }
            // do loop continues in next code example
```



<span data-ttu-id="731d8-129">Para verificar a confiança do certificado se o status da assinatura for válido ou questionável, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="731d8-129">To verify the certificate trust if the signature status was valid or questionable, perform the following steps:</span></span>

1.  <span data-ttu-id="731d8-130">Obtenha o status de confiança do certificado.</span><span class="sxs-lookup"><span data-stu-id="731d8-130">Get the certificate trust status.</span></span>
2.  <span data-ttu-id="731d8-131">Avalie o status de confiança do certificado retornado.</span><span class="sxs-lookup"><span data-stu-id="731d8-131">Evaluate the returned certificate trust status.</span></span>
3.  <span data-ttu-id="731d8-132">Retornar o status resultante.</span><span class="sxs-lookup"><span data-stu-id="731d8-132">Return the resulting status.</span></span>

<span data-ttu-id="731d8-133">O exemplo de código a seguir não testa todos os status de confiança de certificado possíveis.</span><span class="sxs-lookup"><span data-stu-id="731d8-133">The next code example does not test for every possible certificate trust status.</span></span> <span data-ttu-id="731d8-134">Para obter detalhes adicionais sobre os valores de status que podem ser retornados, consulte [**\_ \_ status de confiança do certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).</span><span class="sxs-lookup"><span data-stu-id="731d8-134">For additional details on the status values that can be returned, see [**CERT\_TRUST\_STATUS**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).</span></span>


```C++
            // continuing do loop from previous code example
            //
            // at this point, localSignatureStatus should be less than or 
            // equal to what it was before the test.

            // Check the certificate to see if it is valid
            if ((localSignatureStatus == XPS_SIGNATURE_STATUS_VALID) || 
                (localSignatureStatus == XPS_SIGNATURE_STATUS_QUESTIONABLE))
            {
                // This call builds the certificate trust chain from the 
                //  supplied certificate.  The certificate chain is used to
                //  authenticate the supplied certificate.
                hr = GetCertificateTrustStatus (
                    *signingCertificate, 
                    &signatureCertificateStore,
                    &certificateStatus);
                if (FAILED(hr))
                {
                    // ERROR: An attempt to authenticate the certificate 
                    //  has failed
                    break; // out of do loop with failed hr
                }

                // The Crypt API returns a status that can contain more than
                //  one status value.
                // statusFlagMask is set to test all bits except for the
                //  CERT_TRUST_REVOCATION_STATUS_UNKNOWN
                //  CERT_TRUST_IS_OFFLINE_REVOCATION
                //  CERT_TRUST_IS_NOT_TIME_VALID
                //  values because, for this test, these are not considered
                //  to be error conditions.
                DWORD statusFlagMask = ~(
                    CERT_TRUST_REVOCATION_STATUS_UNKNOWN | 
                    CERT_TRUST_IS_OFFLINE_REVOCATION | 
                    CERT_TRUST_IS_NOT_TIME_VALID);

                if (CERT_TRUST_NO_ERROR == (certificateStatus & statusFlagMask))
                {
                    // If *signatureStatus is already 
                    //    XPS_SIGNATURE_STATUS_VALID then there is no need to 
                    //    change the status as the certificate status has no 
                    //    certificate trust errors.
                    // If *signatureStatus is already 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE then we will not
                    //  upgrade the trust status of the signature just 
                    //  because there is no trust issue with the certificate.
                }
                else
                {
                    // If trust errors were detected with the certificate, 
                    //  then this XPS signature is given a status of 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE
                    *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                }

                // Handle additional certificate errors.  
                //  This is not an exhaustive list of possible errors.

                if (certificateStatus & CERT_TRUST_IS_NOT_TIME_VALID)
                {
                    // The XPS Viewer considers signatures with 
                    //  expired certificates as valid.
                }
                if (certificateStatus & CERT_TRUST_IS_PARTIAL_CHAIN)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_NOT_SIGNATURE_VALID)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_SELF_SIGNED)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
                
                if (certificateStatus & CERT_TRUST_IS_UNTRUSTED_ROOT)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
            }//End if

            hr = certificatesInSignature->MoveNext(&moreCertificates);
            if (FAILED(hr))
            {
                // ERROR: could not move to the next 
                //  certificate in the enumerator
                break; // out of do loop with failed hr
            }
        } while((*signatureStatus != XPS_SIGNATURE_STATUS_VALID) && 
                    moreCertificates);
    } // end if successful

    if (NULL != certificatesInSignature) certificatesInSignature->Release();

    return hr;
}
```



<span data-ttu-id="731d8-135">No próximo exemplo de código, o status de confiança do certificado é obtido chamando o método mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="731d8-135">In the next code example, the certificate trust status is obtained by calling the method shown in the code example that follows.</span></span>


```C++
HRESULT GetCertificateTrustStatus(
    __in PCCERT_CONTEXT certificate,
    __in HCERTSTORE* certificateStore,
    __out DWORD* certificateStatus
)
{
    HRESULT    hr = S_OK;

    // The certificate chain that will be created from 
    //  the PCCERT_CONTEXT object passed in.  
    PCCERT_CHAIN_CONTEXT    certificateChain =    NULL;

    hr = CreateCertificateChain(
        certificate, 
        *certificateStore, 
        &certificateChain);

    if (SUCCEEDED(hr)) { 
        *certificateStatus = 
            certificateChain->TrustStatus.dwErrorStatus;
    }

    return hr;
}
```



<span data-ttu-id="731d8-136">A cadeia de certificados usada no exemplo de código anterior é criada chamando-se o método mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="731d8-136">The certificate chain used in the preceding code example is created by calling the method shown in the following code example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="731d8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="731d8-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="731d8-138">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="731d8-138">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="731d8-139">**\_contexto da cadeia de certificados \_**</span><span class="sxs-lookup"><span data-stu-id="731d8-139">**CERT\_CHAIN\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[<span data-ttu-id="731d8-140">**contexto do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="731d8-140">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="731d8-141">**\_status de confiança do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="731d8-141">**CERT\_TRUST\_STATUS**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[<span data-ttu-id="731d8-142">**CertAddCertificateContextToStore**</span><span class="sxs-lookup"><span data-stu-id="731d8-142">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[<span data-ttu-id="731d8-143">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="731d8-143">**CertOpenStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[<span data-ttu-id="731d8-144">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="731d8-144">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="731d8-145">**IOpcCertificateEnumerator**</span><span class="sxs-lookup"><span data-stu-id="731d8-145">**IOpcCertificateEnumerator**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[<span data-ttu-id="731d8-146">**IOpcCertificateEnumerator:: GetCurrent**</span><span class="sxs-lookup"><span data-stu-id="731d8-146">**IOpcCertificateEnumerator::GetCurrent**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[<span data-ttu-id="731d8-147">**IOpcCertificateEnumerator:: MoveNext**</span><span class="sxs-lookup"><span data-stu-id="731d8-147">**IOpcCertificateEnumerator::MoveNext**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[<span data-ttu-id="731d8-148">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="731d8-148">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[<span data-ttu-id="731d8-149">**IXpsSignature::GetCertificateEnumerator**</span><span class="sxs-lookup"><span data-stu-id="731d8-149">**IXpsSignature::GetCertificateEnumerator**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[<span data-ttu-id="731d8-150">**IXpsSignature:: verificar**</span><span class="sxs-lookup"><span data-stu-id="731d8-150">**IXpsSignature::Verify**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[<span data-ttu-id="731d8-151">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="731d8-151">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[<span data-ttu-id="731d8-152">**IXpsSignatureCollection::GetAt**</span><span class="sxs-lookup"><span data-stu-id="731d8-152">**IXpsSignatureCollection::GetAt**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[<span data-ttu-id="731d8-153">**IXpsSignatureCollection:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="731d8-153">**IXpsSignatureCollection::GetCount**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[<span data-ttu-id="731d8-154">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="731d8-154">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="731d8-155">**IXpsSignatureManager:: getsignatures**</span><span class="sxs-lookup"><span data-stu-id="731d8-155">**IXpsSignatureManager::GetSignatures**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[<span data-ttu-id="731d8-156">**\_status da assinatura XPS \_**</span><span class="sxs-lookup"><span data-stu-id="731d8-156">**XPS\_SIGNATURE\_STATUS**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

<span data-ttu-id="731d8-157">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="731d8-157">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="731d8-158">Inserir cadeias de certificados em um documento</span><span class="sxs-lookup"><span data-stu-id="731d8-158">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="731d8-159">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="731d8-159">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="731d8-160">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="731d8-160">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="731d8-161">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="731d8-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
