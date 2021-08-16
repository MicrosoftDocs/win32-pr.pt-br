---
description: Codec Merit
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Codec Merit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065115"
---
# <a name="codec-merit"></a>Codec Merit

Começando no Windows 7, um Media Foundation codec pode ser atribuído a um *valor de valor de valor.* Quando os codecs são enumerados, codecs com maior valor são preferenciais em vez de codecs com menor poder. Codecs com qualquer valor de responsabilidade são preferenciais em vez de codecs sem um valor atribuído. Para obter detalhes sobre a enumeração codec, consulte [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

Os valores de valor são atribuídos pela Microsoft. Atualmente, somente os codecs de hardware estão qualificados para receber um valor de valor único. O fornecedor do codec também é emitido um certificado digital, que é usado para verificar o valor do codec. Para obter um certificado, envie uma solicitação de email para wmla@microsoft.com . O processo para obter um certificado inclui a assinatura de uma licença e o fornecimento de um conjunto de arquivos de informações para a Microsoft.

O processo de codec funciona da seguinte forma:

1.  O fornecedor do codec implementa um dos seguintes:
    -   Um mini driver AVStream. Media Foundation fornece um MFT de proxy padrão para drivers AVStream. Essa é a opção indicada.
    -   Uma Media Foundation transformação (MFT) que atua como um proxy para o hardware. Para obter mais informações, consulte [Hardware MFTs](hardware-mfts.md).
2.  O valor do codec é armazenado no Registro para pesquisa rápida.
3.  A [**função MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) classifica codecs em ordem de diodio. Codecs com valores de princípios aparecem na lista por trás de codecs registrados localmente (consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), mas à frente de outros codecs.
4.  Quando o MFT é criado, o valor do codec é verificado usando a API do OPM [(Gerenciador](output-protection-manager.md) de Proteção de Saída).
5.  Para um proxy MFT, o codec implementa a interface [**IOPMVideoOutput.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) Para um driver AVStream, o codec implementa o conjunto de propriedades KSPROPSETID \_ OPMVideoOutput.

O diagrama a seguir mostra como o valor é verificado em ambos os casos:

![diagrama mostrando dois processos: um leva por meio do proxy de base de mídia mft e o driver avstream, o outro por meio do proxy personalizado mft](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>MFT de Proxy Personalizado

Se você fornecer um proxy MFT para o codec de hardware, implemente o valor de codec value da seguinte forma:

1.  Implemente a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) no MFT. O código de exemplo é mostrado na próxima seção deste tópico.
2.  Adicione o [atributo \_ MFT CODEC \_ ATTRIBUTE \_ AO](mft-codec-merit-attribute.md) Registro, da seguinte forma:

    1.  Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo armazenamento de atributos.
    2.  Chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para definir o atributo [ \_ MFT CODEC \_ \_ ATTRIBUTE.](mft-codec-merit-attribute.md) O valor do atributo é o atributo atribuído pelo codec.
    3.  Chame [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) para registrar o MFT. Passe o armazenamento de atributos no *parâmetro pAttributes.*

3.  O aplicativo chama [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Essa função retorna uma matriz de [**ponteiros IMFActivate,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) um para cada codec que corresponde aos critérios de enumeração.
4.  O aplicativo chama [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o MFT.
5.  O [**método ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) chama a [**função MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) para verificar o certificado e o valor de solicitação.
6.  A [**função MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) chama [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) e envia uma solicitação de status GET [**\_ \_ CODEC \_ INFO do OPM.**](opm-get-codec-info.md) Essa solicitação de status retorna o valor de valores atribuídos do codec. Se esse valor não corresponder ao valor do Registro, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) poderá falhar.

O código a seguir mostra como adicionar o valor de valor ao registro quando você registra o MFT:


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implementando IOPMVideoOutput para CodecAlt

O código a seguir mostra como implementar [**IOPMVideoOutput para**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) o codec. Para obter uma discussão mais geral sobre a API do OPM, consulte [Gerenciador de Proteção de Saída](output-protection-manager.md).

> [!Note]  
> O código mostrado aqui não tem ofuscação ou outros mecanismos de segurança. Ele é destinado a mostrar a implementação básica da solicitação de handshake e status do OPM.

 

Este exemplo pressupo que *g \_ TestCert* é uma matriz de byte que contém a cadeia de certificados do codec e *g \_ PrivateKey* é uma matriz de byte que contém a chave privada do certificado:


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



No método [**IOPMVideoOutput::StartInitialization,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) gere um número aleatório para o handshake. Retorne esse número e o certificado para o chamador:


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



O [**método IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) conclui o handshake do OPM:


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



No método [**IOPMVideoOutput::GetInformation,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) implemente a solicitação de status [**GET \_ \_ CODEC \_ INFO do OPM.**](opm-get-codec-info.md) Os dados de entrada são uma [**estrutura \_ GET \_ CODEC INFO \_ \_ PARAMETERS do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) que contém o CLSID do seu MFT. Os dados de saída são uma [**estrutura \_ GET \_ CODEC INFO INFORMATION \_ \_ do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) que contém o valor do codec.


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



O [**método GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) deve calcular uma Message Authentication Code (MAC) usando o algoritmo OMAC-1; consulte [Computando o valor OMAC-1](opm-example-code.md).

Não é necessário dar suporte a nenhuma outra solicitação de status do OPM.

Os métodos [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) e [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) não são necessários para o codec, portanto, esses métodos podem retornar **E \_ NOTIMPL.**


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> <dt>

[Escrevendo um MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



