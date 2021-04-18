---
title: Autenticando o provedor de serviços
description: Autenticando o provedor de serviços
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media Gerenciador de Dispositivos, autenticação
- Gerenciador de Dispositivos, autenticação
- Guia de programação, autenticação
- provedores de serviços, autenticação
- criando provedores de serviços, autenticação
- autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760483"
---
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="756ef-109">Autenticando o provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="756ef-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="756ef-110">Para ser acessível do Windows Media Gerenciador de Dispositivos, um provedor de serviços deve herdar e implementar a interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="756ef-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="756ef-111">Para se autenticar, um provedor de serviços executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="756ef-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="756ef-112">Na instanciação, ele cria um novo objeto global [CSecureChannelServer](csecurechannelserver-class.md) e define os valores de certificado e chave de seu arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="756ef-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="756ef-113">Ele implementa os métodos [**IComponentAuthenticate:: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) e [**IComponentAuthenticate:: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) simplesmente passando os parâmetros para seu membro CSecureChannelServer global.</span><span class="sxs-lookup"><span data-stu-id="756ef-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="756ef-114">Antes de manipular qualquer método implementado do Windows Media Gerenciador de Dispositivos, o provedor de serviços deve verificar a autenticação do chamador chamando CSecureChannelServer:: fIsAuthenticated e falhando se o chamador não estiver autenticado.</span><span class="sxs-lookup"><span data-stu-id="756ef-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="756ef-115">Essas etapas são mostradas nos exemplos de C++ a seguir.</span><span class="sxs-lookup"><span data-stu-id="756ef-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="756ef-116">**Criando o objeto CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="756ef-116">**Creating the CSecureChannelServer object**</span></span>


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



<span data-ttu-id="756ef-117">**Implementando os métodos IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="756ef-117">**Implementing the IComponentAuthenticate methods**</span></span>


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



<span data-ttu-id="756ef-118">**Verificando a autenticação do chamador**</span><span class="sxs-lookup"><span data-stu-id="756ef-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="756ef-119">O exemplo de código a seguir mostra um provedor de serviços verificando a autenticação do chamador como parte de sua implementação da interface **IMDServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="756ef-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="756ef-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="756ef-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="756ef-121">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="756ef-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




