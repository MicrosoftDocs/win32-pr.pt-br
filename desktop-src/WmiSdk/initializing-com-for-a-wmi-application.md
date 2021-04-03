---
description: A primeira etapa na conexão com o WMI é configurar as chamadas COM para CoInitializeEx e CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Inicializando COM para um aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922778"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="668e1-103">Inicializando COM para um aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="668e1-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="668e1-104">A primeira etapa na conexão com o WMI é configurar as chamadas COM para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="668e1-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="668e1-105">Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="668e1-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="668e1-106">O procedimento a seguir descreve como inicializar COM de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="668e1-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="668e1-107">**Para inicializar COM de um aplicativo cliente**</span><span class="sxs-lookup"><span data-stu-id="668e1-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="668e1-108">Inicialize com com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="668e1-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="668e1-109">Chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) é um procedimento padrão para configurar uma interface com.</span><span class="sxs-lookup"><span data-stu-id="668e1-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="668e1-110">Portanto, o WMI não exige que você observe quaisquer procedimentos adicionais ao chamar **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="668e1-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="668e1-111">Para obter mais informações, consulte [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="668e1-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="668e1-112">O exemplo de código a seguir descreve como chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="668e1-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="668e1-113">Defina os níveis gerais de segurança com com uma chamada para a interface [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="668e1-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="668e1-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) é uma função padrão que você deve chamar ao configurar uma interface com para um processo.</span><span class="sxs-lookup"><span data-stu-id="668e1-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="668e1-115">Chame **CoInitializeSecurity** se você quiser definir as configurações de segurança padrão para autenticação, representação ou serviço de autenticação para um processo inteiro.</span><span class="sxs-lookup"><span data-stu-id="668e1-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="668e1-116">Para obter mais informações, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="668e1-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="668e1-117">Se você quiser definir ou alterar a segurança de um proxy específico, deverá chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="668e1-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="668e1-118">Use **CoSetProxyBlanket** sempre que for necessário definir ou alterar a segurança com ao executar dentro de outro processo em que você não possa controlar as configurações de segurança padrão para autenticação, representação ou serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="668e1-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="668e1-119">Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md) e [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="668e1-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="668e1-120">O WMI tem vários problemas de segurança dos quais você deve estar atento ao programar um aplicativo cliente do WMI.</span><span class="sxs-lookup"><span data-stu-id="668e1-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="668e1-121">Para obter mais informações, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="668e1-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="668e1-122">O exemplo de código a seguir descreve como chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança com no processo.</span><span class="sxs-lookup"><span data-stu-id="668e1-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

<span data-ttu-id="668e1-123">Depois de inicializar o COM, a próxima etapa é criar uma conexão com um namespace do WMI.</span><span class="sxs-lookup"><span data-stu-id="668e1-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="668e1-124">Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="668e1-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="668e1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="668e1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668e1-126">Criando um aplicativo WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="668e1-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="668e1-127">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="668e1-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
