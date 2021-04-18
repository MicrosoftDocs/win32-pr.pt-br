---
description: Depois de recuperar um ponteiro para um proxy de IWbemServices, você deve definir a segurança no proxy para acessar o WMI por meio do proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Definindo os níveis de segurança em uma conexão WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814394"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="a666d-103">Definindo os níveis de segurança em uma conexão WMI</span><span class="sxs-lookup"><span data-stu-id="a666d-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="a666d-104">Depois de recuperar um ponteiro para um proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você deve definir a segurança no proxy para acessar o WMI por meio do proxy.</span><span class="sxs-lookup"><span data-stu-id="a666d-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="a666d-105">Você deve definir a segurança porque o proxy de **IWbemServices** concede acesso a um objeto fora do processo.</span><span class="sxs-lookup"><span data-stu-id="a666d-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="a666d-106">Em geral, a segurança COM não permite que um processo acesse outro processo se você não definir as propriedades de segurança adequadas.</span><span class="sxs-lookup"><span data-stu-id="a666d-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="a666d-107">Para obter mais informações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="a666d-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="a666d-108">As conexões com diferentes sistemas operacionais exigem níveis variados de autenticação e representação.</span><span class="sxs-lookup"><span data-stu-id="a666d-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="a666d-109">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a666d-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="a666d-110">Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="a666d-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="a666d-111">O procedimento a seguir descreve como definir os níveis de segurança em uma conexão WMI.</span><span class="sxs-lookup"><span data-stu-id="a666d-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="a666d-112">**Para definir os níveis de segurança em uma conexão WMI**</span><span class="sxs-lookup"><span data-stu-id="a666d-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="a666d-113">Defina os níveis de segurança no proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com uma chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="a666d-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="a666d-114">O exemplo de código a seguir descreve uma maneira comum de chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="a666d-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

<span data-ttu-id="a666d-115">Depois de definir os níveis de segurança para o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você pode acessar os vários recursos do WMI.</span><span class="sxs-lookup"><span data-stu-id="a666d-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="a666d-116">Depois de terminar de usar o WMI, você deve desligar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a666d-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="a666d-117">Para obter mais informações, consulte [limpando e desligando um aplicativo WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="a666d-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
