---
description: Demonstra como solicitar um certificado de arquivamento de chave.
ms.assetid: a09f55c1-fb27-41e7-9a2f-617d2360c02f
title: Solicitando um certificado de arquivamento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da1f69338ed4a41986700853ef5d46ee08612e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829155"
---
# <a name="requesting-a-key-archival-certificate"></a>Solicitando um certificado de arquivamento de chave

O exemplo a seguir mostra a criação e o envio de uma [*solicitação de certificado*](../secgloss/c-gly.md) e o recebimento do certificado de arquivamento de chave resultante. Para que este exemplo tenha sucesso, a [*autoridade de certificação*](../secgloss/c-gly.md) (CA) que recebe a solicitação de certificado deve ser configurada para arquivamento de chave.

As etapas a seguir descrevem como criar e enviar uma solicitação de certificado.

**Para criar e enviar uma solicitação de certificado**

1.  Recupere o certificado do Exchange da autoridade de certificação usando o método [**ICertRequest2:: GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) .
2.  Especifique que o certificado de troca de AC recuperado é o certificado de arquivamento de chave usando a propriedade [**ICEnroll4::P rivatekeyarchivecertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) .
3.  Crie uma solicitação de certificado CMC usando o método [**ICEnroll4:: CreateRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) .
4.  Envie a solicitação de certificado a uma AC usando o método [**ICertRequest2:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) . A AC deve ser configurada para dar suporte ao arquivamento de chave.

As etapas a seguir descrevem como recuperar o certificado emitido para fins de arquivamento de chave.

**Para recuperar o certificado emitido para fins de arquivamento de chave**

1.  Recupere a resposta completa, incluindo o certificado emitido, usando o método [**ICertRequest2:: GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) .
2.  Instale o certificado emitido usando o método [**ICEnroll4:: acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) .

O exemplo a seguir mostra a criação e o envio de uma solicitação de certificado e o recebimento do certificado de arquivamento de chave resultante.


```C++
// Pointer to interface objects.
ICEnroll4 * pEnroll = NULL;
ICertRequest2 * pRequest = NULL;

// BSTR variables.
BSTR    bstrCACert = NULL;
BSTR    bstrDN = NULL;
BSTR    bstrCertAuth = NULL;
BSTR    bstrReq = NULL;
BSTR    bstrDispMsg = NULL;
BSTR    bstrErrorMsg = NULL;

VARIANT varFullResp;

LONG    lDisp =0;
LONG    lRequestID = 0;
LONG    lStatus = 0;

HRESULT    hr;

// Initialize COM.
hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
if ( FAILED( hr ) )
{
    printf("Failed CoInitializeEx - [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Enrollment object.
hr = CoCreateInstance( CLSID_CEnroll,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICEnroll4,
                       (void **)&pEnroll);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Request object.
hr = CoCreateInstance( CLSID_CCertRequest,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICertRequest2,
                       (void **)&pRequest);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
    goto error;
}

// Allocate the BSTR that represents the certification authority.
// Note the use of '\\' to produce a single '\' in C++.
bstrCertAuth = SysAllocString(L"Server\\CertAuth");
if (NULL == bstrCertAuth)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Retrieve the CA's exchange certificate.
hr = pRequest->GetCACertificate(TRUE,
                                bstrCertAuth,
                                CR_OUT_BASE64HEADER,
                                &bstrCACert);
if (FAILED(hr))
{
    printf("Failed GetCACertificate [%x]\n", hr);
    goto error;
}

// Specify the retrieved certificate 
// as the key archive certificate.
hr = pEnroll->put_PrivateKeyArchiveCertificate(bstrCACert);
if (FAILED(hr))
{
    printf("put_PrivateKeyArchiveCertificate [%x]\n", hr);
    goto error;
}

// Create the data for the request.
// A user interface or database retrieval could
// be used instead of this example's hard-coded text.
bstrDN = SysAllocString(L"CN=UserName"    // common name
                        L",OU=UserUnit"   // org unit
                        L",O=UserOrg"     // org
                        L",L=UserCity"    // locality
                        L",S=WA"          // state
                        L",C=US");        // country/region
if (NULL == bstrDN)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Create the certificate request.
hr = pEnroll->createRequest( XECR_CMC,
                             bstrDN, 
                             NULL,
                             &bstrReq );
if ( FAILED( hr ) )
{
    printf("Failed createRequest - [%x]\n", hr);
    goto error;
}

// Submit the certificate request.
hr = pRequest->Submit( CR_IN_CMC,
                       bstrReq,
                       NULL,
                       bstrCertAuth,
                       &lDisp );
if ( FAILED( hr ) )
{
    
    printf("Failed Submit - [%x]\n", hr);  
    goto error;
}

// Evaluate the disposition of the submitted request.
switch (lDisp)
{
    case CR_DISP_ISSUED:
           printf("Certificate was issued.\n");
           break;

    case CR_DISP_ISSUED_OUT_OF_BAND:
    case CR_DISP_INCOMPLETE:
    case CR_DISP_ERROR:
    case CR_DISP_DENIED:
    case CR_DISP_UNDER_SUBMISSION:
    case CR_DISP_REVOKED:
            printf("Certificate was not issued: %d\n", lDisp);
            break;

    default:
            printf("Unexpected disposition: %d\n", lDisp);
            goto error;
}

// Retrieve the request ID.
hr = pRequest->GetRequestId(&lRequestID);
if ( FAILED(hr) )
{
    printf("Failed GetRequestId - [%x]\n", hr);  
    goto error;
}
printf("The request ID is %d\n", lRequestID);

if (CR_DISP_ISSUED != lDisp)
{
    // Provide information about why a certificate 
    // was not issued.
    
    // Retrieve the last status.
    hr = pRequest->GetLastStatus(&lStatus);
    if ( FAILED(hr) )
    {
        printf("Failed GetLastStatus - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the disposition message.
    hr = pRequest->GetDispositionMessage(&bstrDispMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetDispositionMessage - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the error message.
    hr = pRequest->GetErrorMessageText(lStatus,
                                       CR_GEMT_HRESULT_STRING,
                                       &bstrErrorMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetErrorMessageText - [%x]\n", hr);  
        goto error;
    }
    
    // Display the information and exit.
    printf("Request ID: %d\nDisposition: %S\nError: %S\n",
           lRequestID,
           bstrDispMsg,
           bstrErrorMsg);
    goto error;
}

// Retrieve the full response.
VariantInit(&varFullResp);
hr = pRequest->GetFullResponseProperty( FR_PROP_FULLRESPONSE,
                                        0,
                                        PROPTYPE_BINARY,
                                        CR_OUT_BASE64,
                                        &varFullResp );
if ( FAILED( hr ) )
{
    printf("Failed GetFullResponseProperty - [%x]\n", hr);
    goto error;
}

// Accept the response.
hr = pEnroll->acceptResponse(varFullResp.bstrVal);
if ( FAILED( hr ) )
{
    printf("Failed AcceptResponse - [%x]\n", hr);
    goto error;
}
else
{
    printf("Successfully completed processing\n");
}

error:

// Done processing.
// Clean up object resources.
if ( NULL != pEnroll )
    pEnroll->Release();
if ( NULL != pRequest )
    pRequest->Release();

// Free BSTR variables.
if ( NULL != bstrCACert )
    SysFreeString ( bstrCACert );
if ( NULL != bstrDN )
    SysFreeString ( bstrDN );
if ( NULL != bstrCertAuth )
    SysFreeString ( bstrCertAuth );
if ( NULL != bstrReq )
    SysFreeString ( bstrReq );
if ( NULL != bstrDispMsg )
    SysFreeString ( bstrDispMsg );
if ( NULL != bstrErrorMsg )
    SysFreeString ( bstrErrorMsg );

// Clear VARIANTS.
VariantClear(&varFullResp);

// Free COM resources.
CoUninitialize();

return hr;
```



 

 
