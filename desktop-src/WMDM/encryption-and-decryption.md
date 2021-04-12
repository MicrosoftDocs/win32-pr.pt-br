---
title: Criptografia e descriptografia
description: Criptografia e descriptografia
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Gerenciador de Dispositivos de mídia do Windows, criptografia
- Gerenciador de Dispositivos, criptografia
- aplicativos de área de trabalho, criptografia
- provedores de serviços, criptografia
- Guia de programação, criptografia
- criptografia
- Gerenciador de Dispositivos de mídia do Windows, descriptografia
- Gerenciador de Dispositivos, descriptografia
- aplicativos de área de trabalho, descriptografia
- provedores de serviços, descriptografia
- Guia de programação, descriptografia
- descriptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366612"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="c1146-115">Criptografia e descriptografia</span><span class="sxs-lookup"><span data-stu-id="c1146-115">Encryption and Decryption</span></span>

<span data-ttu-id="c1146-116">O Windows Media Gerenciador de Dispositivos requer a criptografia de arquivos enviados entre o provedor de serviços e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1146-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="c1146-117">Isso pode ser feito de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="c1146-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="c1146-118">Se o provedor de serviços oferecer suporte apenas a [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) e [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), os dados deverão ser criptografados e descriptografados pelo aplicativo e pelo provedor de serviços usando os métodos [CSecureChannelClient](csecurechannelclient-class.md) e [CSecureChannelServer](csecurechannelserver-class.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c1146-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="c1146-119">Se o provedor de serviços oferecer suporte a [**IMDSPObject2:: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) e [**IMDSPObject2:: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), seu aplicativo poderá evitar a dispendiosa autenticação de mensagens de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="c1146-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="c1146-120">(O canal seguro é mantido para que os provedores de serviços herdados que não implementam o [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) ainda possam continuar a funcionar.)</span><span class="sxs-lookup"><span data-stu-id="c1146-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="c1146-121">O requisito de criptografia impede que aplicativos mal-intencionados obtenham dados que estão sendo passados entre componentes de software e também protege a integridade dos dados enviados de ou para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1146-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="c1146-122">Os três métodos a seguir exigem criptografia ou descriptografia.</span><span class="sxs-lookup"><span data-stu-id="c1146-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="c1146-123">Método</span><span class="sxs-lookup"><span data-stu-id="c1146-123">Method</span></span>                                                                          | <span data-ttu-id="c1146-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1146-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1146-125">**IWMDMOperation::TransferObjectData**</span><span class="sxs-lookup"><span data-stu-id="c1146-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="c1146-126">Aplicativo Criptografia ou descriptografia, dependendo se o aplicativo está enviando ou recebendo dados.</span><span class="sxs-lookup"><span data-stu-id="c1146-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="c1146-127">**IMDSPObject:: ler**</span><span class="sxs-lookup"><span data-stu-id="c1146-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="c1146-128">(Provedor de serviços) Encripta.</span><span class="sxs-lookup"><span data-stu-id="c1146-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="c1146-129">**IMDSPObject:: Write**</span><span class="sxs-lookup"><span data-stu-id="c1146-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="c1146-130">(Provedor de serviços) Descriptografia.</span><span class="sxs-lookup"><span data-stu-id="c1146-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="c1146-131">A criptografia e a descriptografia são feitas por chamadas de método único.</span><span class="sxs-lookup"><span data-stu-id="c1146-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="c1146-132">A criptografia é feita por [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)) para aplicativos ou por [**CSecureChannelServer:: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) para provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="c1146-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="c1146-133">A descriptografia é feita por [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) for Applications ou [**CSecureChannelServer::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) for Service Providers.</span><span class="sxs-lookup"><span data-stu-id="c1146-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="c1146-134">Os parâmetros são idênticos entre os métodos de cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="c1146-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="c1146-135">As etapas a seguir mostram como criptografar e descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="c1146-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="c1146-136">(Essas etapas serão importantes somente se seu aplicativo se comunicar com um provedor de serviços herdado que não implementa [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span><span class="sxs-lookup"><span data-stu-id="c1146-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="c1146-137">**Criptografia**</span><span class="sxs-lookup"><span data-stu-id="c1146-137">**Encryption**</span></span>

1.  <span data-ttu-id="c1146-138">Crie a chave MAC para os dados criptografados, conforme descrito em [autenticação de mensagens](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c1146-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="c1146-139">Chame **EncryptParam** com os dados a serem criptografados para executar a criptografia in-loco.</span><span class="sxs-lookup"><span data-stu-id="c1146-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="c1146-140">O exemplo de código a seguir demonstra a implementação de um provedor de serviço de [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span><span class="sxs-lookup"><span data-stu-id="c1146-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="c1146-141">Esse método cria a chave MAC usando os dados para criptografar e o tamanho dos dados e os envia para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1146-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="c1146-142">**Descriptografia**</span><span class="sxs-lookup"><span data-stu-id="c1146-142">**Decryption**</span></span>

1.  <span data-ttu-id="c1146-143">Chame **DecryptParam** com os dados a serem criptografados para executar a descriptografia in-loco.</span><span class="sxs-lookup"><span data-stu-id="c1146-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="c1146-144">Verifique a chave MAC para os dados descriptografados, conforme descrito em [autenticação de mensagens](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c1146-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="c1146-145">O exemplo de código a seguir demonstra a implementação de um provedor de serviço de [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span><span class="sxs-lookup"><span data-stu-id="c1146-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="c1146-146">Esse método cria a chave MAC usando os dados para criptografar e o tamanho dos dados e os envia para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1146-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c1146-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1146-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1146-148">**Usando canais autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="c1146-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 