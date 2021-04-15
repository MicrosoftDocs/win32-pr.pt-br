---
description: 'Depois de definir as chamadas padrão para COM, você deve conectar-se ao WMI por meio de uma chamada para o método IWbemLocator:: ConnectServer.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Criando uma conexão com um namespace WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461315"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="3dd62-103">Criando uma conexão com um namespace WMI</span><span class="sxs-lookup"><span data-stu-id="3dd62-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="3dd62-104">Depois de definir as chamadas padrão para COM, você deve conectar-se ao WMI por meio de uma chamada para o método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="3dd62-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="3dd62-105">O método **ConnectServer** retorna um proxy de uma interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="3dd62-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="3dd62-106">Por meio de **IWbemServices**, você pode acessar os diferentes recursos do WMI.</span><span class="sxs-lookup"><span data-stu-id="3dd62-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="3dd62-107">Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="3dd62-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="3dd62-108">O procedimento a seguir descreve como criar uma conexão com um namespace do WMI.</span><span class="sxs-lookup"><span data-stu-id="3dd62-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="3dd62-109">**Para criar uma conexão com um namespace WMI**</span><span class="sxs-lookup"><span data-stu-id="3dd62-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="3dd62-110">Inicialize a interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) por meio de uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3dd62-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="3dd62-111">O WMI não requer que você execute nenhum procedimento adicional ao chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="3dd62-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="3dd62-112">O exemplo de código a seguir descreve como inicializar o [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="3dd62-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   <span data-ttu-id="3dd62-113">Conecte-se ao WMI por meio de uma chamada para o método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="3dd62-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="3dd62-114">O método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) retorna um proxy para uma interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que usa o para acessar o namespace WMI local ou remoto especificado em sua chamada para **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="3dd62-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="3dd62-115">O exemplo de código a seguir descreve como chamar [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="3dd62-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

<span data-ttu-id="3dd62-116">Depois de ter recebido um ponteiro para o proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você deve definir a segurança no proxy para acessar o WMI.</span><span class="sxs-lookup"><span data-stu-id="3dd62-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="3dd62-117">Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3dd62-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dd62-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dd62-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd62-119">Criando um aplicativo WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="3dd62-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="3dd62-120">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="3dd62-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
