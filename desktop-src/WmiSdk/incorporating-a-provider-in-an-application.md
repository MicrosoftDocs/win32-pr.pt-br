---
description: Descreve como incluir o provedor COM WMI como um componente em um aplicativo em vez de em processo para o WMI. Chamado de provedor dissociado, esse é o tipo recomendado de provedor COM WMI a ser criado para o Windows 2000 e sistemas operacionais posteriores.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporando um provedor em um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551428"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="3e355-104">Incorporando um provedor em um aplicativo</span><span class="sxs-lookup"><span data-stu-id="3e355-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="3e355-105">Ao criar um aplicativo que deve ser instrumentado, a prática recomendada é incluir o provedor como um componente dentro do próprio aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e355-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="3e355-106">Essa prática permite que Instrumentação de Gerenciamento do Windows (WMI) interajam com o provedor de serviços diretamente, em vez de indiretamente por meio da API do programa.</span><span class="sxs-lookup"><span data-stu-id="3e355-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="3e355-107">O desacoplamento do provedor do WMI também coloca o aplicativo no controle do ciclo de vida do provedor, em vez do WMI.</span><span class="sxs-lookup"><span data-stu-id="3e355-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="3e355-108">Para obter mais informações sobre como gravar um provedor que é executado no processo WMI, consulte [fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="3e355-109">Para obter mais informações sobre o modelo de hospedagem e as configurações de segurança para o provedor, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="3e355-110">O diagrama a seguir ilustra a relação entre o WMI, um provedor dissociado e um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e355-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![relação entre WMI, provedor dissociado e aplicativo](images/decoupledprov.png)

<span data-ttu-id="3e355-112">Para obter mais informações sobre métodos de provedor desacoplados, consulte [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) e [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="3e355-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="3e355-113">O provedor dissociado dá suporte a instâncias, métodos, provedores de eventos e consumidores de eventos.</span><span class="sxs-lookup"><span data-stu-id="3e355-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="3e355-114">Ele não dá suporte a provedores de propriedades e de classes.</span><span class="sxs-lookup"><span data-stu-id="3e355-114">It does not support class and property providers.</span></span> <span data-ttu-id="3e355-115">Para obter mais informações, consulte [escrevendo um provedor de classe](writing-a-class-provider.md) e [gravando um provedor de propriedades](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="3e355-116">Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e355-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="3e355-117">O procedimento a seguir usa exemplos de código C++ para descrever como incorporar um provedor dissociado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e355-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="3e355-118">O método de inicialização do aplicativo executa as etapas a seguir para que o WMI interaja apenas com um provedor dissociado registrado.</span><span class="sxs-lookup"><span data-stu-id="3e355-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="3e355-119">**Para implementar um provedor dissociado em um aplicativo C++**</span><span class="sxs-lookup"><span data-stu-id="3e355-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="3e355-120">Inicialize a biblioteca COM para uso pelo thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="3e355-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="3e355-121">O exemplo de código a seguir mostra como inicializar a biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="3e355-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="3e355-122">Defina o nível de segurança do processo padrão.</span><span class="sxs-lookup"><span data-stu-id="3e355-122">Set the default process security level.</span></span>

    <span data-ttu-id="3e355-123">Esse nível estabelece o nível de segurança necessário para que outros processos acessem as informações do processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="3e355-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="3e355-124">O nível de autenticação deve ser o padrão de nível da autenticação RPC \_ C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3e355-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="3e355-125">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="3e355-126">O exemplo de código a seguir mostra como definir o nível de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="3e355-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="3e355-127">Registre o registrador de provedor dissociado.</span><span class="sxs-lookup"><span data-stu-id="3e355-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="3e355-128">O exemplo de código a seguir mostra como registrar o registrador de provedor dissociado.</span><span class="sxs-lookup"><span data-stu-id="3e355-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="3e355-129">Registre o provedor de eventos dissociado.</span><span class="sxs-lookup"><span data-stu-id="3e355-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="3e355-130">O exemplo de código a seguir mostra como registrar o provedor de eventos dissociado.</span><span class="sxs-lookup"><span data-stu-id="3e355-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="3e355-131">Faça as [chamadas para o WMI](making-calls-to-wmi.md) exigidas pela funcionalidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="3e355-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="3e355-132">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="3e355-133">Para obter mais informações se o provedor tiver uma solicitação de dados de um script ou aplicativo, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="3e355-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="3e355-134">Antes de terminar, o aplicativo deve ser limpo após ele mesmo.</span><span class="sxs-lookup"><span data-stu-id="3e355-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="3e355-135">O procedimento a seguir descreve como cancelar o registro do provedor dissociado para que o WMI não tente consultá-lo para obter informações.</span><span class="sxs-lookup"><span data-stu-id="3e355-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="3e355-136">O procedimento a seguir descreve como cancelar o registro do provedor dissociado.</span><span class="sxs-lookup"><span data-stu-id="3e355-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="3e355-137">**Para cancelar o registro do provedor dissociado**</span><span class="sxs-lookup"><span data-stu-id="3e355-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="3e355-138">Cancelar o registro e liberar o registrador.</span><span class="sxs-lookup"><span data-stu-id="3e355-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="3e355-139">O exemplo de código a seguir mostra como cancelar o registro e liberar o registrador.</span><span class="sxs-lookup"><span data-stu-id="3e355-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="3e355-140">Cancelar o registro e liberar o provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="3e355-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="3e355-141">O exemplo de código a seguir mostra como cancelar o registro e liberar o provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="3e355-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="3e355-142">Limpe o servidor COM.</span><span class="sxs-lookup"><span data-stu-id="3e355-142">Clean up the COM server.</span></span>

    <span data-ttu-id="3e355-143">O exemplo de código a seguir mostra como cancelar a inicialização da biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="3e355-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="3e355-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e355-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e355-145">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="3e355-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="3e355-146">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="3e355-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="3e355-147">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="3e355-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



