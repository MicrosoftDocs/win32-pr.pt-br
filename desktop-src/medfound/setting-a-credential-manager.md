---
description: Configurando um Gerenciador de credenciais
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Configurando um Gerenciador de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808251"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="8b3f5-103">Configurando um Gerenciador de credenciais</span><span class="sxs-lookup"><span data-stu-id="8b3f5-103">Setting a Credential Manager</span></span>

<span data-ttu-id="8b3f5-104">Um aplicativo que fornece credenciais para a fonte de rede deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b3f5-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="8b3f5-105">Implemente um objeto do Gerenciador de credenciais que expõe a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="8b3f5-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="8b3f5-106">Antes de criar a origem da rede, crie um novo repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="8b3f5-107">Defina a propriedade [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) no repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="8b3f5-108">O valor da propriedade é um ponteiro para a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="8b3f5-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="8b3f5-109">Passe um ponteiro para o repositório de propriedades para o resolvedor de origem, conforme descrito em [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8b3f5-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="8b3f5-110">As fontes de rede usam o Gerenciador de credenciais para obter credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="8b3f5-111">Se a origem da rede exigir credenciais para acessar um recurso de rede, ela chamará o método [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="8b3f5-112">Essa chamada inicia uma solicitação assíncrona para obter as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="8b3f5-113">O método **BeginGetCredentials** pode obter as credenciais do cache de credenciais ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="8b3f5-114">As credenciais são armazenadas em um *objeto de credencial*.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="8b3f5-115">Quando a operação for concluída, o aplicativo invocará a interface de retorno de chamada para notificar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="8b3f5-116">A origem da rede chama [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) para concluir a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="8b3f5-117">Como essa é uma operação assíncrona, o aplicativo deve despachar o retorno de chamada no final da operação.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="8b3f5-118">Para obter instruções detalhadas sobre como escrever um método assíncrono, consulte [escrevendo um método assíncrono](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b3f5-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="8b3f5-119">O exemplo a seguir mostra como definir a propriedade [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) na fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="8b3f5-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8b3f5-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b3f5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b3f5-121">Autenticação de origem da rede</span><span class="sxs-lookup"><span data-stu-id="8b3f5-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



