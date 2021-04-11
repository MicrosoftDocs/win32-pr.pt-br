---
title: Noções básicas do aplicativo
description: Noções básicas do aplicativo
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK do Windows Media Format, noções básicas do aplicativo DRM
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159364"
---
# <a name="application-basics"></a><span data-ttu-id="df08b-109">Noções básicas do aplicativo</span><span class="sxs-lookup"><span data-stu-id="df08b-109">Application Basics</span></span>

<span data-ttu-id="df08b-110">Há algum processamento extra que você deve executar para qualquer aplicativo que use as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="df08b-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="df08b-111">Este tópico descreve os requisitos para um aplicativo simples.</span><span class="sxs-lookup"><span data-stu-id="df08b-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="df08b-112">Primeiro, você deve inicializar as APIs estendidas do cliente DRM do Windows Media chamando a função [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="df08b-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="df08b-113">Os objetos do SDK são objetos COM, mas você não precisa chamar **CoIntialize**, pois a função **WMDRMStatup** inicializa com para você.</span><span class="sxs-lookup"><span data-stu-id="df08b-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="df08b-114">O Windows Media Format SDK usa apenas um subconjunto de COM, portanto, se você usar objetos COM diferentes daqueles na API estendida do cliente DRM do Windows Media, ainda deverá chamar **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="df08b-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="df08b-115">Todos os objetos das APIs estendidas do cliente DRM do Windows Media são criados usando funções e métodos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="df08b-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="df08b-116">Você nunca precisa chamar **CoCreateInstance** para criar um objeto.</span><span class="sxs-lookup"><span data-stu-id="df08b-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="df08b-117">A primeira interface a ser instanciada para qualquer aplicativo que usa o SDK é [**IWMDRMProvider**](iwmdrmprovider.md), que você pode usar para instanciar todas as outras interfaces base.</span><span class="sxs-lookup"><span data-stu-id="df08b-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="df08b-118">Para obter uma instância de **IWMDRMProvider**, você deve chamar [**WMDRMCreateProvider**](wmdrmcreateprovider.md) ou [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span><span class="sxs-lookup"><span data-stu-id="df08b-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="df08b-119">A diferença entre essas funções é que o **WMDRMCreateProvider** cria um objeto que, por sua vez, pode criar apenas objetos que não dão suporte a métodos que exigem a biblioteca de stub.</span><span class="sxs-lookup"><span data-stu-id="df08b-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="df08b-120">Depois de ter uma instância do **IWMDRMProvider**, você pode criar os outros objetos necessários chamando [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="df08b-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="df08b-121">Quando estiver pronto para sair do aplicativo, você deverá liberar os recursos do subsistema DRM chamando a função [**WMDRMShutdown**](wmdrmshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="df08b-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="df08b-122">Essa função também desliga o COM para você.</span><span class="sxs-lookup"><span data-stu-id="df08b-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="df08b-123">O exemplo de código a seguir demonstra como inicializar e concluir um aplicativo que usa as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="df08b-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="df08b-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df08b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df08b-125">**Introdução**</span><span class="sxs-lookup"><span data-stu-id="df08b-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




