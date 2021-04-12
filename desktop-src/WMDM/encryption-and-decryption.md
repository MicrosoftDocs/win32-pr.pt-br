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
# <a name="encryption-and-decryption"></a>Criptografia e descriptografia

O Windows Media Gerenciador de Dispositivos requer a criptografia de arquivos enviados entre o provedor de serviços e o aplicativo. Isso pode ser feito de duas maneiras:

-   Se o provedor de serviços oferecer suporte apenas a [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) e [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), os dados deverão ser criptografados e descriptografados pelo aplicativo e pelo provedor de serviços usando os métodos [CSecureChannelClient](csecurechannelclient-class.md) e [CSecureChannelServer](csecurechannelserver-class.md) , respectivamente.
-   Se o provedor de serviços oferecer suporte a [**IMDSPObject2:: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) e [**IMDSPObject2:: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), seu aplicativo poderá evitar a dispendiosa autenticação de mensagens de canal seguro. (O canal seguro é mantido para que os provedores de serviços herdados que não implementam o [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) ainda possam continuar a funcionar.)

O requisito de criptografia impede que aplicativos mal-intencionados obtenham dados que estão sendo passados entre componentes de software e também protege a integridade dos dados enviados de ou para o dispositivo.

Os três métodos a seguir exigem criptografia ou descriptografia.



| Método                                                                          | Descrição                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | Aplicativo Criptografia ou descriptografia, dependendo se o aplicativo está enviando ou recebendo dados. |
| [**IMDSPObject:: ler**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Provedor de serviços) Encripta.                                                                             |
| [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Provedor de serviços) Descriptografia.                                                                             |



 

A criptografia e a descriptografia são feitas por chamadas de método único. A criptografia é feita por [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)) para aplicativos ou por [**CSecureChannelServer:: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) para provedores de serviço. A descriptografia é feita por [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) for Applications ou [**CSecureChannelServer::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) for Service Providers. Os parâmetros são idênticos entre os métodos de cliente e servidor.

As etapas a seguir mostram como criptografar e descriptografar dados. (Essas etapas serão importantes somente se seu aplicativo se comunicar com um provedor de serviços herdado que não implementa [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)

**Criptografia**

1.  Crie a chave MAC para os dados criptografados, conforme descrito em [autenticação de mensagens](message-authentication.md).
2.  Chame **EncryptParam** com os dados a serem criptografados para executar a criptografia in-loco.

O exemplo de código a seguir demonstra a implementação de um provedor de serviço de [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read). Esse método cria a chave MAC usando os dados para criptografar e o tamanho dos dados e os envia para o aplicativo.


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



**Descriptografia**

1.  Chame **DecryptParam** com os dados a serem criptografados para executar a descriptografia in-loco.
2.  Verifique a chave MAC para os dados descriptografados, conforme descrito em [autenticação de mensagens](message-authentication.md).

O exemplo de código a seguir demonstra a implementação de um provedor de serviço de [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write). Esse método cria a chave MAC usando os dados para criptografar e o tamanho dos dados e os envia para o aplicativo.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando canais autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 