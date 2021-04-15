---
title: Autenticando o aplicativo
description: Autenticando o aplicativo
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media Gerenciador de Dispositivos, autenticação
- Gerenciador de Dispositivos, autenticação
- Guia de programação, autenticação
- aplicativos de área de trabalho, autenticação
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, autenticação
- autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761501"
---
# <a name="authenticating-the-application"></a><span data-ttu-id="2b73b-109">Autenticando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="2b73b-109">Authenticating the Application</span></span>

<span data-ttu-id="2b73b-110">A primeira etapa que seu aplicativo deve executar é a autenticação.</span><span class="sxs-lookup"><span data-stu-id="2b73b-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="2b73b-111">A autenticação verifica a identidade do aplicativo para o Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2b73b-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="2b73b-112">Depois de autenticar seu aplicativo, você pode chamar **QueryInterface** para obter a interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raiz, que pode ser consultada para outras interfaces necessárias, que podem ser consultadas para todas as outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="2b73b-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="2b73b-113">A autenticação precisa ocorrer apenas uma vez, na inicialização.</span><span class="sxs-lookup"><span data-stu-id="2b73b-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="2b73b-114">Para autenticar seu aplicativo, execute estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2b73b-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="2b73b-115">Cocrie o objeto **MediaDevMgr** (ID de classe MediaDevMgr) e solicite uma interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="2b73b-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="2b73b-116">Crie um objeto [CSecureChannelClient](csecurechannelclient-class.md) para manipular a autenticação.</span><span class="sxs-lookup"><span data-stu-id="2b73b-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="2b73b-117">Passe a chave do aplicativo e transfira o certificado para o objeto de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="2b73b-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="2b73b-118">Você pode usar a chave ou o certificado fictício mostrado no código de exemplo a seguir para obter a funcionalidade básica das funções do SDK.</span><span class="sxs-lookup"><span data-stu-id="2b73b-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="2b73b-119">No entanto, para obter a funcionalidade completa (importante para passar arquivos de e para o dispositivo), você deve solicitar uma chave e um certificado da Microsoft, conforme descrito em [ferramentas para desenvolvimento](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="2b73b-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="2b73b-120">Passe a interface **IComponentAuthenticate** criada na etapa 1 para o objeto de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="2b73b-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="2b73b-121">Chame [**CSecureChannelClient:: Authenticate**](/previous-versions/ms983906(v=msdn.10)) para autenticar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b73b-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="2b73b-122">Consulta **IComponentAuthenticate** para a interface **IWMDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="2b73b-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="2b73b-123">Essas etapas são mostradas no código C++ a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b73b-123">These steps are shown in the following C++ code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2b73b-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b73b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b73b-125">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="2b73b-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 