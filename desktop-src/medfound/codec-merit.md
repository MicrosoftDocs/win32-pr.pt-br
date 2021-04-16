---
description: Mérito do codec
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Mérito do codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550265"
---
# <a name="codec-merit"></a><span data-ttu-id="3a399-103">Mérito do codec</span><span class="sxs-lookup"><span data-stu-id="3a399-103">Codec Merit</span></span>

<span data-ttu-id="3a399-104">A partir do Windows 7, um codec Media Foundation pode ser atribuído a um valor de *mérito* .</span><span class="sxs-lookup"><span data-stu-id="3a399-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="3a399-105">Quando os codecs são enumerados, os codecs com mérito maior são preferenciais sobre codecs com um mérito inferior.</span><span class="sxs-lookup"><span data-stu-id="3a399-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="3a399-106">Os codecs com qualquer valor de mérito são preferenciais sobre codecs sem um mérito atribuído.</span><span class="sxs-lookup"><span data-stu-id="3a399-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="3a399-107">Para obter detalhes sobre a enumeração de codec, consulte [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="3a399-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="3a399-108">Os valores de mérito são atribuídos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a399-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="3a399-109">Atualmente, somente os codecs de hardware estão qualificados a receber um valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="3a399-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="3a399-110">O fornecedor do codec também emitiu um certificado digital, que é usado para verificar o valor de mérito do codec.</span><span class="sxs-lookup"><span data-stu-id="3a399-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="3a399-111">Para obter um certificado, envie uma solicitação de email para wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="3a399-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="3a399-112">O processo de obtenção de um certificado inclui a assinatura de uma licença e o fornecimento de um conjunto de arquivos de informações à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a399-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="3a399-113">O mérito do codec funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3a399-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="3a399-114">O fornecedor do codec implementa um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3a399-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="3a399-115">Um mini-driver AVStream.</span><span class="sxs-lookup"><span data-stu-id="3a399-115">An AVStream mini-driver.</span></span> <span data-ttu-id="3a399-116">Media Foundation fornece um MFT de proxy padrão para drivers AVStream.</span><span class="sxs-lookup"><span data-stu-id="3a399-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="3a399-117">Essa é a opção indicada.</span><span class="sxs-lookup"><span data-stu-id="3a399-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="3a399-118">Uma Media Foundation transformação (MFT) que atua como um proxy para o hardware.</span><span class="sxs-lookup"><span data-stu-id="3a399-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="3a399-119">Para obter mais informações, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="3a399-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="3a399-120">O valor de mérito do codec é armazenado no registro para pesquisa rápida.</span><span class="sxs-lookup"><span data-stu-id="3a399-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="3a399-121">A função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) classifica codecs em ordem de mérito.</span><span class="sxs-lookup"><span data-stu-id="3a399-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="3a399-122">Os codecs com valores de mérito aparecem na lista por trás de codecs registrados localmente (consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), mas à frente de outros codecs.</span><span class="sxs-lookup"><span data-stu-id="3a399-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="3a399-123">Quando o MFT é criado, o mérito do codec é verificado usando a API do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="3a399-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="3a399-124">Para um MFT de proxy, o codec implementa a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="3a399-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="3a399-125">Para um driver AVStream, o codec implementa o \_ conjunto de propriedades KSPROPSETID OPMVideoOutput.</span><span class="sxs-lookup"><span data-stu-id="3a399-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="3a399-126">O diagrama a seguir mostra como o mérito é verificado em ambos os casos:</span><span class="sxs-lookup"><span data-stu-id="3a399-126">The following diagram shows how merit is verified in both cases:</span></span>

![diagrama mostrando dois processos: um deles leva por meio da MFT do proxy do Media Foundation e do driver AVStream, o outro por meio do MFT de proxy personalizado](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="3a399-128">MFT de proxy personalizado</span><span class="sxs-lookup"><span data-stu-id="3a399-128">Custom Proxy MFT</span></span>

<span data-ttu-id="3a399-129">Se você fornecer um MFT de proxy para o codec de hardware, implemente o valor de mérito de codec da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3a399-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="3a399-130">Implemente a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) no MFT.</span><span class="sxs-lookup"><span data-stu-id="3a399-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="3a399-131">O código de exemplo é mostrado na próxima seção deste tópico.</span><span class="sxs-lookup"><span data-stu-id="3a399-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="3a399-132">Adicione o atributo de [ \_ \_ \_ atributo mérito do codec de MFT](mft-codec-merit-attribute.md) ao registro, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3a399-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="3a399-133">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="3a399-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="3a399-134">Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para definir o atributo de [ \_ \_ \_ atributo mérito do codec de MFT](mft-codec-merit-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3a399-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="3a399-135">O valor do atributo é o mérito atribuído do codec.</span><span class="sxs-lookup"><span data-stu-id="3a399-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="3a399-136">Chame [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) para registrar o MFT.</span><span class="sxs-lookup"><span data-stu-id="3a399-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="3a399-137">Passe o repositório de atributos no parâmetro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="3a399-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="3a399-138">O aplicativo chama [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="3a399-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="3a399-139">Essa função retorna uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , uma para cada codec que corresponde aos critérios de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3a399-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="3a399-140">O aplicativo chama [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o MFT.</span><span class="sxs-lookup"><span data-stu-id="3a399-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="3a399-141">O método [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) chama a função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) para verificar o certificado e o valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="3a399-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="3a399-142">A função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) chama [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) e envia uma solicitação de status de informações de codec de obtenção de [**OPM \_ \_ \_**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="3a399-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="3a399-143">Essa solicitação de status retorna o valor de Mérito atribuído do codec.</span><span class="sxs-lookup"><span data-stu-id="3a399-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="3a399-144">Se esse valor não corresponder ao valor do registro, [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="3a399-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="3a399-145">O código a seguir mostra como adicionar o valor de mérito ao registro ao registrar o MFT:</span><span class="sxs-lookup"><span data-stu-id="3a399-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="3a399-146">Implementando o IOPMVideoOutput para o mérito do codec</span><span class="sxs-lookup"><span data-stu-id="3a399-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="3a399-147">O código a seguir mostra como implementar o [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) para o mérito do codec.</span><span class="sxs-lookup"><span data-stu-id="3a399-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="3a399-148">Para obter uma discussão mais geral sobre a API OPM, consulte [Gerenciador de proteção de saída](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3a399-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="3a399-149">O código mostrado aqui não tem ofuscação nem outros mecanismos de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a399-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="3a399-150">Ele é destinado a mostrar a implementação básica do handshake de OPM e a solicitação de status.</span><span class="sxs-lookup"><span data-stu-id="3a399-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="3a399-151">Este exemplo pressupõe que *g \_ TestCert* é uma matriz de bytes que contém a cadeia de certificados do codec, e *g \_ PrivateKey* é uma matriz de bytes que contém a chave privada do certificado:</span><span class="sxs-lookup"><span data-stu-id="3a399-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



<span data-ttu-id="3a399-152">No método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) , gere um número aleatório para o handshake.</span><span class="sxs-lookup"><span data-stu-id="3a399-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="3a399-153">Retornar este número e o certificado ao chamador:</span><span class="sxs-lookup"><span data-stu-id="3a399-153">Return this number and the certificate to the caller:</span></span>


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



<span data-ttu-id="3a399-154">O método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) conclui o HANDSHAKE de OPM:</span><span class="sxs-lookup"><span data-stu-id="3a399-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



<span data-ttu-id="3a399-155">No método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) , implemente a solicitação de status de [**\_ \_ \_ informações de codec do OPM**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="3a399-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="3a399-156">Os dados de entrada são uma estrutura de parâmetros de informações do codec de obtenção de OPM que contém o CLSID de seu MFT. [**\_ \_ \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="3a399-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="3a399-157">Os dados de saída são uma estrutura de [**\_ \_ \_ \_ informações do codec Get do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) que contém o mérito do codec.</span><span class="sxs-lookup"><span data-stu-id="3a399-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



<span data-ttu-id="3a399-158">O método [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) deve calcular um Message Authentication Code (Mac) usando o algoritmo OMAC-1; consulte [computando o valor OMAC-1](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="3a399-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="3a399-159">Não é necessário dar suporte a outras solicitações de status de OPM.</span><span class="sxs-lookup"><span data-stu-id="3a399-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="3a399-160">Os métodos [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) e [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) não são necessários para o mérito do codec, portanto, esses métodos podem retornar **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="3a399-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a><span data-ttu-id="3a399-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a399-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a399-162">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a399-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="3a399-163">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="3a399-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



