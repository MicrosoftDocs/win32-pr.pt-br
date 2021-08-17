---
description: Este tópico contém um código de exemplo para usar o Gerenciador de Proteção de Saída.
ms.assetid: ad2303a0-f3f3-43a0-83eb-023640da2ece
title: Código de exemplo do OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075b3fc8b88d87b80126c8dea307cf151e5f9fc817fa61b9ed8be37ef12c5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102116"
---
# <a name="opm-example-code"></a>Código de exemplo do OPM

Este tópico contém um código de exemplo para usar [o Gerenciador de Proteção de Saída](output-protection-manager.md).

O código de exemplo neste tópico demonstra como executar o handshake do OPM, enviar uma solicitação de status e enviar um comando OPM. Para operações criptográficas, o código usa a API de Criptografia: CNG (Próxima Geração). O foco deste tópico é mostrar a funcionalidade do OPM, portanto, as tarefas relacionadas ao certificado X.509, como análise e validação do certificado, não são mostradas.

Os procedimentos mostrados neste tópico são explicados mais detalhadamente em [Usando o Gerenciador de Proteção de Saída](using-output-protection-manager.md).

-   [Executando o handshake do OPM](#performing-the-opm-handshake)
-   [Enviando uma solicitação de status do OPM](#sending-an-opm-status-request)
-   [Enviando um comando OPM](#sending-an-opm-command)
-   [Computando o valor OMAC-1](#computing-the-omac-1-value)
-   [Tópicos relacionados](#related-topics)

## <a name="performing-the-opm-handshake"></a>Executando o handshake do OPM

1.  Depois de enumerar os dispositivos OPM e selecionar uma saída de vídeo (não mostrada), a primeira etapa é chamar [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) para obter a cadeia de certificados X.509 do dispositivo:

    ```C++
        OPM_RANDOM_NUMBER random;   // Random number from driver.
        ZeroMemory(&random, sizeof(random));

        BYTE *pbCertificate = NULL; // Pointer to a buffer to hold the certificate.
        ULONG cbCertificate = 0;    // Size of the certificate in bytes.

        PUBLIC_KEY_VALUES *pKey = NULL; // The driver's public key.

        // Get the driver's certificate chain + random number
        hr = pVideoOutput->StartInitialization(
            &random, 
            &pbCertificate, 
            &cbCertificate
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Validate the X.509 certificate. (Not shown.)
        hr = ValidateX509Certificate(pbCertificate, cbCertificate);

        if (FAILED(hr))
        {
            goto done;
        }

        // Get the public key from the certificate. (Not shown.)
        hr = GetPublicKeyFromCertificate(
            pbCertificate,
            cbCertificate,
            &pKey
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Load and initialize a CNG provider (Cryptography API: Next Generation)

        BCRYPT_ALG_HANDLE hAlg = 0;

        hr = BCryptOpenAlgorithmProvider(
            &hAlg, 
            BCRYPT_RSA_ALGORITHM, 
            MS_PRIMITIVE_PROVIDER, 
            0
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Import the public key into the CNG provider.

        BCRYPT_KEY_HANDLE hPublicKey = 0;

        // Import the RSA public key.
        hr = ImportRsaPublicKey(hAlg, pKey, &hPublicKey);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  O aplicativo deve validar a cadeia de certificados e obter a chave pública do certificado folha na cadeia. Essas etapas não são mostradas aqui.
3.  Depois de ter a chave pública, você pode importar a chave para um provedor de algoritmo CNG. Chame a **função BCryptOpenAlgorithmProvider** para carregar o provedor. A função definida `ImportRsaPublicKey` pelo aplicativo importa a chave e retorna um alça para a chave importada:
    ```C++
    void ReverseMemCopy(BYTE *pbDest, BYTE const *pbSource, DWORD cb)
    {
        for (DWORD i = 0; i < cb; i++) 
        {
            pbDest[cb - 1 - i] = pbSource[i];
        }
    }
    ```

    

    ```C++
    //------------------------------------------------------------------------
    //
    // ImportRsaPublicKey
    //
    // Converts an RSA public key from an RSAPUBKEY blob into an 
    // BCRYPT_RSAKEY_BLOB and sets the public key on the CNG provider.
    //
    //------------------------------------------------------------------------

    HRESULT ImportRsaPublicKey(
        BCRYPT_ALG_HANDLE hAlg,     // CNG provider
        PUBLIC_KEY_VALUES *pKey,    // Pointer to the RSAPUBKEY blob.
        BCRYPT_KEY_HANDLE *phKey    // Receives a handle the imported public key.
        )
    {
        HRESULT hr = S_OK;

        BYTE *pbPublicKey = NULL;
        DWORD cbKey = 0;

        // Layout of the RSA public key blob:

        //  +----------------------------------------------------------------+
        //  |     BCRYPT_RSAKEY_BLOB    | BE( dwExp ) |   BE( Modulus )      |
        //  +----------------------------------------------------------------+
        //
        //  sizeof(BCRYPT_RSAKEY_BLOB)       cbExp           cbModulus 
        //  <--------------------------><------------><---------------------->
        //
        //   BE = Big Endian Format                                                     

        DWORD cbModulus = (pKey->rsapubkey.bitlen + 7) / 8;
        DWORD dwExp = pKey->rsapubkey.pubexp;
        DWORD cbExp = (dwExp & 0xFF000000) ? 4 :
                      (dwExp & 0x00FF0000) ? 3 :
                      (dwExp & 0x0000FF00) ? 2 : 1;

        BCRYPT_RSAKEY_BLOB *pRsaBlob;
        PBYTE pbCurrent;

        hr = DWordAdd(cbModulus, sizeof(BCRYPT_RSAKEY_BLOB), &cbKey);

        if (FAILED(hr))
        {
            goto done;
        }

        cbKey += cbExp;

        pbPublicKey = (BYTE*)CoTaskMemAlloc(cbKey);
        if (NULL == pbPublicKey) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }    
        
        ZeroMemory(pbPublicKey, cbKey);
        pRsaBlob = (BCRYPT_RSAKEY_BLOB *)(pbPublicKey);
        
        // Make the Public Key Blob Header
        pRsaBlob->Magic = BCRYPT_RSAPUBLIC_MAGIC;
        pRsaBlob->BitLength = pKey->rsapubkey.bitlen;
        pRsaBlob->cbPublicExp = cbExp;
        pRsaBlob->cbModulus = cbModulus;
        pRsaBlob->cbPrime1 = 0;
        pRsaBlob->cbPrime2 = 0;

        pbCurrent = (PBYTE)(pRsaBlob + 1);
        
        // Copy pubExp Big Endian 
        ReverseMemCopy(pbCurrent, (PBYTE)&dwExp, cbExp);
        pbCurrent += cbExp;

        // Copy Modulus Big Endian 
        ReverseMemCopy(pbCurrent, pKey->modulus, cbModulus);

        // Set the key.
        hr = BCryptImportKeyPair(
            hAlg, 
            NULL, 
            BCRYPT_RSAPUBLIC_BLOB, 
            phKey,
            (PUCHAR)pbPublicKey,
            cbKey,
            0
            );

    done:
        CoTaskMemFree(pbPublicKey);
        return hr;
    }
    ```

    

4.  Em seguida, prepare o buffer que contém os números de sequência inicial e a chave de sessão AES.
    ```C++
    void CopyAndAdvancePtr(BYTE*& pDest, const BYTE* pSrc, DWORD cb)
    {
        memcpy(pDest, pSrc, cb);
        pDest += cb;
    }
    ```

    

    ```C++
        //--------------------------------------------------------------------
        // Prepare the signature for key exchnage.
        //--------------------------------------------------------------------

        UINT uStatusSeq = 0;     // Status sequence number.
        UINT uCommandSeq = 0;    // Command sequence number.

        OPM_RANDOM_NUMBER AesKey;   // Session key

        // Generate the starting sequence number for queries.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uStatusSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }


        // Generate the starting sequence number for commands.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uCommandSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Generate the AES session key.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&AesKey, 
            sizeof(AesKey), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Fill in the initialization structure.
        OPM_ENCRYPTED_INITIALIZATION_PARAMETERS initParams;
        ZeroMemory(&initParams, sizeof(initParams));
        
        // Use a temporary pointer for copying into the array.
        BYTE *pBuffer = &initParams.abEncryptedInitializationParameters[0];

        CopyAndAdvancePtr(pBuffer, random.abRandomNumber, sizeof(random)); // Random number from the friver.
        CopyAndAdvancePtr(pBuffer, AesKey.abRandomNumber, sizeof(AesKey)); // Session key.
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uStatusSeq, sizeof(uStatusSeq));
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uCommandSeq, sizeof(uCommandSeq));
    ```

    

5.  Criptografe esse buffer com criptografia RSAES-OAEP usando a chave pública do driver.
    ```C++
        //--------------------------------------------------------------------
        // RSAES-OAEP encrypt the signature. Use SHA2 hashing algorithm.
        //--------------------------------------------------------------------

        PBYTE pbDataIn = &initParams.abEncryptedInitializationParameters[0];
        ULONG cbDataIn = (ULONG)(pBuffer - pbDataIn);  

        DWORD cbOutput = 0;
        DWORD cbDataOut= 0;

        BYTE *pbDataOut = NULL;

        BCRYPT_OAEP_PADDING_INFO paddingInfo;
        ZeroMemory(&paddingInfo, sizeof(paddingInfo));

        paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

        //Encrypt the signature.
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &cbOutput,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }


        pbDataOut = new (std::nothrow) BYTE[cbOutput];
        if (NULL == pbDataOut) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            pbDataOut,
            cbOutput,
            &cbDataOut,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

6.  Chame [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) para concluir o handshake.
    ```C++
        // Complete the handshake.
        hr = pVideoOutput->FinishInitialization(
            (OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *)pbDataOut
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

## <a name="sending-an-opm-status-request"></a>Enviando uma solicitação de status do OPM

O exemplo a seguir mostra como enviar a solicitação de status [**OPM \_ GET CONNECTOR \_ \_ TYPE.**](opm-get-connector-type.md)

1.  Preencha uma estrutura [**GET \_ INFO \_ \_ PARAMETERS do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) com as informações da solicitação de status.
    ```C++
        //--------------------------------------------------------------------
        // Prepare the status request structure.
        //--------------------------------------------------------------------

        OPM_GET_INFO_PARAMETERS     StatusInput;
        OPM_REQUESTED_INFORMATION   StatusOutput;

        ZeroMemory(&StatusInput, sizeof(StatusInput));
        ZeroMemory(&StatusOutput, sizeof(StatusOutput));

        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&(StatusInput.rnRandomNumber), 
            OPM_128_BIT_RANDOM_NUMBER_SIZE, 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        StatusInput.guidInformation = OPM_GET_CONNECTOR_TYPE; // Request GUID.
        StatusInput.ulSequenceNumber = uStatusSeq;            // Sequence number.

        //  Sign the request structure, not including the omac field.

        hr = ComputeOMAC(
            AesKey,                                             // Session key.
            (BYTE*)&StatusInput + OPM_OMAC_SIZE,                // Data
            sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE,    // Size
            &StatusInput.omac                                   // Receives the OMAC
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  O **membro omac** da estrutura [**GET INFO \_ \_ \_ PARAMETERS do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) é um OMAC (CBC MAC) de uma chave computado para o restante da estrutura. A função ComputeOMAC (mostrada posteriormente) é declarada da seguinte forma:
    ```C++
    HRESULT ComputeOMAC(
        OPM_RANDOM_NUMBER&  AesKey,     // Session key
        PUCHAR pb,                      // Data
        DWORD cb,                       // Size
        OPM_OMAC *pTag                  // Receives the OMAC
        );
    ```

    

3.  Chame [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) para enviar a solicitação de status.
    ```C++
        //  Send the status request.
        hr = pVideoOutput->GetInformation(&StatusInput, &StatusOutput);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

4.  O driver grava a resposta na estrutura [**\_ INFORMAÇÕES SOLICITADAS \_ do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) A estrutura de resposta inclui um valor OMAC, calculado para o restante da estrutura. Verifique esse valor antes de confiar nos dados de resposta:
    ```C++
        //--------------------------------------------------------------------
        // Verify the signature.
        //--------------------------------------------------------------------

        OPM_OMAC rgbSignature = { 0 };

        // Calculate our own signature.

        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&StatusOutput + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &rgbSignature
            );

        if (FAILED(hr))
        {
            goto done;
        }

        if (memcmp(StatusOutput.omac.abOMAC, rgbSignature.abOMAC, OPM_OMAC_SIZE))
        {
            // The signature does not match.
            hr = E_FAIL; 
            goto done;
        }

        // Update the sequence number.
        uStatusSeq++;
    ```

    

5.  O **membro abRequestedInformation da** estrutura [**\_ OPM REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contém os dados de resposta. Para a [**solicitação OPM \_ GET CONNECTOR \_ \_ TYPE,**](opm-get-connector-type.md) os dados de resposta consistem em uma estrutura [**de INFORMAÇÕES PADRÃO \_ \_ do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
    ```C++
        // Examine the response. 
        // The response data is an OPM_STANDARD_INFORMATION structure.

        OPM_STANDARD_INFORMATION StatusInfo;
        ZeroMemory(&StatusInfo, sizeof(StatusInfo));

        ULONG cbLen = min(sizeof(OPM_STANDARD_INFORMATION), StatusOutput.cbRequestedInformationSize);    

        if (cbLen != 0)
        {
            // Copy the repinse into the array.
            CopyMemory((BYTE*)&StatusInfo, StatusOutput.abRequestedInformation, cbLen);
        }
        
        //  Verify the random number.
        if (0!= memcmp(
            (BYTE*)&StatusInfo.rnRandomNumber, 
            (BYTE*)&StatusInput.rnRandomNumber, 
            sizeof(OPM_RANDOM_NUMBER)) 
            ) 
        {
            hr = E_FAIL;
            goto done;
        }    

        // Verify the status of the OPM session.
        if (StatusInfo.ulStatusFlags != OPM_STATUS_NORMAL)
        {
            // Abnormal status
            hr = E_FAIL;
            goto done;
        }    
        
        ULONG ConnectorType = StatusInfo.ulInformation & OPM_BUS_TYPE_MASK;
    ```

    

## <a name="sending-an-opm-command"></a>Enviando um comando OPM

O exemplo a seguir mostra como habilitar High-Bandwidth HDCP (Proteção de Conteúdo Digital) enviando o comando [**OPM \_ SET PROTECTION \_ \_ LEVEL.**](opm-set-protection-level.md)

1.  Todos os comandos do OPM usam a [**estrutura \_ CONFIGURE \_ PARAMETERS do OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) para dados de entrada. A **matriz abParameters** nessa estrutura contém dados específicos do comando. Para o [**comando OPM \_ SET PROTECTION \_ \_ LEVEL,**](opm-set-protection-level.md) a **matriz abParameters** contém uma [**estrutura OPM SET PROTECTION LEVEL \_ \_ \_ \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) Preencha essa estrutura da seguinte forma:
    ```C++
        //--------------------------------------------------------------------
        // Prepare the command structure.
        //--------------------------------------------------------------------

        // Data specific to the OPM_SET_PROTECTION_LEVEL command.
        OPM_SET_PROTECTION_LEVEL_PARAMETERS CommandInput;

        ZeroMemory(&CommandInput, sizeof(CommandInput));

        CommandInput.ulProtectionType = OPM_PROTECTION_TYPE_HDCP;   
        CommandInput.ulProtectionLevel = OPM_HDCP_ON;        

        ULONG ulAdditionalParametersSize = 0;
        BYTE* pbAdditionalParameters = NULL;
    ```

    

2.  Em seguida, preencha a estrutura [**\_ CONFIGURE \_ PARAMETERS do OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) e compute o OMAC.
    ```C++
        // Common command parameters
        OPM_CONFIGURE_PARAMETERS Command;
        ZeroMemory(&Command, sizeof(Command));

        Command.guidSetting = OPM_SET_PROTECTION_LEVEL;
        Command.ulSequenceNumber = uCommandSeq;
        Command.cbParametersSize = sizeof(OPM_SET_PROTECTION_LEVEL_PARAMETERS);
        CopyMemory(&Command.abParameters[0], (BYTE*)&CommandInput, Command.cbParametersSize);

        //  Sign the command structure, not including the omac field.
        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&Command + OPM_OMAC_SIZE, 
            sizeof(OPM_CONFIGURE_PARAMETERS) - OPM_OMAC_SIZE,
            &Command.omac
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

3.  Para enviar o comando, chame [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Lembre-se de incrementar o número da sequência de comandos após cada comando.
    ```C++
        //  Send the command.
        hr = pVideoOutput->Configure(
            &Command, 
            0,      // Size of additional command data.
            NULL    // Additional command data.
            );

        if (FAILED(hr))
        {
            goto done;
        }

        //  Update the sequence number.
        uCommandSeq++;    
    ```

    

4.  Para verificar se o HDCP está habilitado, envie uma solicitação de status [**GET VIRTUAL PROTECTION LEVEL \_ \_ \_ \_ do OPM**](opm-get-virtual-protection-level.md) (não mostrada).

## <a name="computing-the-omac-1-value"></a>Computando o valor OMAC-1

O código a seguir mostra como calcular o valor OMAC-1 usado para assinar as estruturas de solicitação e comando do OPM.


```C++
// Helper functions for some bitwise operations.

#define AES_BLOCKLEN    (16)
#define AES_KEYSIZE_128 (16)

inline void XOR( 
    BYTE *lpbLHS, 
    const BYTE *lpbRHS, 
    DWORD cbSize = AES_BLOCKLEN 
    )
{
    for( DWORD i = 0; i < cbSize; i++ )
    {
        lpbLHS[i] ^= lpbRHS[i];
    }
}

inline void LShift(const BYTE *lpbOpd, BYTE *lpbRes)
{
    for( DWORD i = 0; i < AES_BLOCKLEN; i++ )
    {
        lpbRes[i] = lpbOpd[i] << 1;
        if( i < AES_BLOCKLEN - 1 )
        {
            lpbRes[i] |= ( (unsigned char)lpbOpd[i+1] ) >> 7;
        }
    }
}

//  Generate OMAC1 signature using AES128

HRESULT ComputeOMAC(
    OPM_RANDOM_NUMBER&  AesKey,     // Session key
    PUCHAR pb,                      // Data
    DWORD cb,                       // Size of the data
    OPM_OMAC *pTag                  // Receives the OMAC
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    DWORD cbKeyObject = 0;
    DWORD cbData = 0;
    PBYTE pbKeyObject = NULL;

    PUCHAR Key = (PUCHAR)AesKey.abRandomNumber;

    struct 
    {
        BCRYPT_KEY_DATA_BLOB_HEADER Header;
        UCHAR Key[AES_KEYSIZE_128];
    } KeyBlob;

    KeyBlob.Header.dwMagic = BCRYPT_KEY_DATA_BLOB_MAGIC;
    KeyBlob.Header.dwVersion = BCRYPT_KEY_DATA_BLOB_VERSION1;
    KeyBlob.Header.cbKeyData = AES_KEYSIZE_128;
    CopyMemory(KeyBlob.Key, Key, sizeof(KeyBlob.Key));

    BYTE rgbLU[OPM_OMAC_SIZE];
    BYTE rgbLU_1[OPM_OMAC_SIZE];
    BYTE rBuffer[OPM_OMAC_SIZE];

    hr = BCryptOpenAlgorithmProvider(
        &hAlg, 
        BCRYPT_AES_ALGORITHM, 
        MS_PRIMITIVE_PROVIDER, 
        0
        );

    //  Get the size needed for the key data
    if (S_OK == hr) 
    {
        hr = BCryptGetProperty(
            hAlg, 
            BCRYPT_OBJECT_LENGTH, 
            (PBYTE)&cbKeyObject, 
            sizeof(DWORD), 
            &cbData, 
            0
            );
    }

    //  Allocate the key data object
    if (S_OK == hr) 
    {
        pbKeyObject = new (std::nothrow) BYTE[cbKeyObject];
        if (NULL == pbKeyObject) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    //  Set to CBC chain mode
    if (S_OK == hr) 
    {
        hr = BCryptSetProperty(
            hAlg, 
            BCRYPT_CHAINING_MODE, 
            (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
            sizeof(BCRYPT_CHAIN_MODE_CBC), 
            0
            );
    }

    //  Set the key
    if (S_OK == hr) 
    {
        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey, 
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    //  Encrypt 0s
    if (S_OK == hr) 
    {
        DWORD cbBuffer = sizeof(rBuffer);
        ZeroMemory(rBuffer, sizeof(rBuffer));

        hr = BCryptEncrypt(hKey, rBuffer, cbBuffer, NULL, NULL, 0, 
            rBuffer, sizeof(rBuffer), &cbBuffer, 0);
    }

    //  Compute OMAC1 parameters
    if (S_OK == hr)
    {
        const BYTE bLU_ComputationConstant = 0x87;
        LPBYTE pbL = rBuffer;

        LShift( pbL, rgbLU );
        if( pbL[0] & 0x80 )
        {
            rgbLU[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
        LShift( rgbLU, rgbLU_1 );
        if( rgbLU[0] & 0x80 )
        {
            rgbLU_1[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
    }

    //  Generate the hash. 
    if (S_OK == hr) 
    {
        // Redo the key to restart the CBC.

        BCryptDestroyKey(hKey);
        hKey = NULL;

        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey,
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    if (S_OK == hr) 
    {
        PUCHAR pbDataInCur = pb;
        cbData = cb;
        do
        {
            DWORD cbBuffer = 0;

            if (cbData > OPM_OMAC_SIZE) 
            {
                CopyMemory( rBuffer, pbDataInCur, OPM_OMAC_SIZE );

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, 
                    NULL, 0, rBuffer, sizeof(rBuffer), &cbBuffer, 0);

                pbDataInCur += OPM_OMAC_SIZE;
                cbData -= OPM_OMAC_SIZE;
            }
            else 
            {   
                if (cbData == OPM_OMAC_SIZE)
                {
                    CopyMemory(rBuffer, pbDataInCur, OPM_OMAC_SIZE);
                    XOR(rBuffer, rgbLU);
                }
                else 
                {
                    ZeroMemory( rBuffer, OPM_OMAC_SIZE );
                    CopyMemory( rBuffer, pbDataInCur, cbData );
                    rBuffer[ cbData ] = 0x80;

                    XOR(rBuffer, rgbLU_1);
                }

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, NULL, 
                    0, (PUCHAR)pTag->abOMAC, OPM_OMAC_SIZE, &cbBuffer, 0);

                cbData = 0;
            }
                
        } while( S_OK == hr && cbData > 0 );
    }

    //  Clean up
    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbKeyObject;
    return hr;
}
```



O algoritmo OMAC-1 é descrito em detalhes em <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html> .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de Proteção de Saída](output-protection-manager.md)
</dt> </dl>

 

 



