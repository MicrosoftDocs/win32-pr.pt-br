---
description: 'Use o método ICertServerPolicy:: setcertificaproperty para definir as propriedades da entidade de um certificado.'
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Definindo propriedades de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813102"
---
# <a name="setting-certificate-properties"></a><span data-ttu-id="426a3-103">Definindo propriedades de certificado</span><span class="sxs-lookup"><span data-stu-id="426a3-103">Setting Certificate Properties</span></span>

<span data-ttu-id="426a3-104">Use o método [**ICertServerPolicy:: Setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) para definir as propriedades da entidade de um certificado.</span><span class="sxs-lookup"><span data-stu-id="426a3-104">Use the [**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the subject properties of a certificate.</span></span> <span data-ttu-id="426a3-105">As propriedades da entidade são propriedades relacionadas ao proprietário do certificado ou ao indivíduo que solicitou o certificado.</span><span class="sxs-lookup"><span data-stu-id="426a3-105">Subject properties are properties related to the owner of the certificate or the individual who requested the certificate.</span></span> <span data-ttu-id="426a3-106">Para obter uma lista de propriedades de entidades, consulte [Propriedades de nome](name-properties.md).</span><span class="sxs-lookup"><span data-stu-id="426a3-106">For a list of subject properties, see [Name Properties](name-properties.md).</span></span>

<span data-ttu-id="426a3-107">Você também pode usar o método [**Setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) para definir as propriedades do certificado nobefore e não After.</span><span class="sxs-lookup"><span data-stu-id="426a3-107">You can also use the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the NotBefore and NotAfter certificate properties.</span></span> <span data-ttu-id="426a3-108">Para obter uma descrição das propriedades do certificado nobefore e não After, consulte [Propriedades do certificado](certificate-properties.md).</span><span class="sxs-lookup"><span data-stu-id="426a3-108">For a description of the NotBefore and NotAfter certificate properties, see [Certificate Properties](certificate-properties.md).</span></span>

<span data-ttu-id="426a3-109">Use o método [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) para adicionar qualquer número de extensões ao certificado.</span><span class="sxs-lookup"><span data-stu-id="426a3-109">Use the [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) method to add any number of extensions to the certificate.</span></span> <span data-ttu-id="426a3-110">Você pode usar extensões para adicionar informações complementares de assunto ou de uso ao certificado.</span><span class="sxs-lookup"><span data-stu-id="426a3-110">You can use extensions to add supplemental subject or usage information to the certificate.</span></span> <span data-ttu-id="426a3-111">Para obter mais informações, consulte [manipuladores de extensão](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="426a3-111">For more information, see [Extension Handlers](extension-handlers.md).</span></span>

<span data-ttu-id="426a3-112">O exemplo a seguir define uma propriedade e uma extensão de certificado em um certificado.</span><span class="sxs-lookup"><span data-stu-id="426a3-112">The following example sets a certificate property and extension on a certificate.</span></span> <span data-ttu-id="426a3-113">Você chama os métodos [**Setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) e [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) na sua implementação [**ICertPolicy2:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) .</span><span class="sxs-lookup"><span data-stu-id="426a3-113">You call the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) and [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) methods in your [**ICertPolicy2::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) implementation.</span></span> <span data-ttu-id="426a3-114">O exemplo não é uma implementação de **VerifyRequest** completa; o exemplo não mostra a lógica de verificação.</span><span class="sxs-lookup"><span data-stu-id="426a3-114">The example is not a complete **VerifyRequest** implementation; the example does not show verification logic.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



