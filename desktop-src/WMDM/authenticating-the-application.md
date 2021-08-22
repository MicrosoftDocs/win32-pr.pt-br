---
title: Autenticando o aplicativo
description: Autenticando o aplicativo
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Gerenciador de Dispositivos de mídia, autenticação
- Gerenciador de Dispositivos, autenticação
- Guia de programação, autenticação
- aplicativos de área de trabalho, autenticação
- criando Windows aplicativos de Gerenciador de Dispositivos de mídia, autenticação
- autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b67ad7c603bbfd3a56667bfcfe8742775c8ae5683888d72661e0a0974aa5358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586731"
---
# <a name="authenticating-the-application"></a>Autenticando o aplicativo

A primeira etapa que seu aplicativo deve executar é a autenticação. a autenticação verifica a identidade do aplicativo para Windows Gerenciador de Dispositivos de mídia. Depois de autenticar seu aplicativo, você pode chamar **QueryInterface** para obter a interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raiz, que pode ser consultada para outras interfaces necessárias, que podem ser consultadas para todas as outras interfaces. A autenticação precisa ocorrer apenas uma vez, na inicialização.

Para autenticar seu aplicativo, execute estas etapas:

1.  Cocrie o objeto **MediaDevMgr** (ID de classe MediaDevMgr) e solicite uma interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .
2.  Crie um objeto [CSecureChannelClient](csecurechannelclient-class.md) para manipular a autenticação.
3.  Passe a chave do aplicativo e transfira o certificado para o objeto de canal seguro. Você pode usar a chave ou o certificado fictício mostrado no código de exemplo a seguir para obter a funcionalidade básica das funções do SDK. No entanto, para obter a funcionalidade completa (importante para passar arquivos de e para o dispositivo), você deve solicitar uma chave e um certificado da Microsoft, conforme descrito em [ferramentas para desenvolvimento](tools-for-development.md).
4.  Passe a interface **IComponentAuthenticate** criada na etapa 1 para o objeto de canal seguro.
5.  Chame [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) para autenticar seu aplicativo.
6.  Consulta **IComponentAuthenticate** para a interface **IWMDeviceManager** .

Essas etapas são mostradas no código C++ a seguir.


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**criando um aplicativo de Gerenciador de Dispositivos de mídia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 