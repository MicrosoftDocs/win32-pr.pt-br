---
description: Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, lê alguns dados e limpa.
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: 'Exemplo: Criando um aplicativo WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e76836090d09ecee413da34d9a15381b9d0a891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773030"
---
# <a name="example-creating-a-wmi-application"></a><span data-ttu-id="7ce8f-103">Exemplo: Criando um aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="7ce8f-103">Example: Creating a WMI Application</span></span>

<span data-ttu-id="7ce8f-104">Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, lê alguns dados e limpa.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, reads some data, and cleans up.</span></span> <span data-ttu-id="7ce8f-105">[Conectar-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md) descreve como obter dados de computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-105">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) describes how to obtain data from remote computers.</span></span>

<span data-ttu-id="7ce8f-106">O procedimento a seguir inclui todas as etapas necessárias para todos os aplicativos WMI do C++.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-106">This following procedure includes all of the steps that are required by all C++ WMI applications.</span></span>

1.  <span data-ttu-id="7ce8f-107">Inicialize parâmetros COM com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-107">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="7ce8f-108">Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-108">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="7ce8f-109">Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-109">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="7ce8f-110">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-110">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="7ce8f-111">Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para um namespace em um computador host especificado — o computador local no caso simples — chamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-111">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for a namespace on a specified host computer—the local computer in the simple case—by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

    <span data-ttu-id="7ce8f-112">Para se conectar a um computador remoto, por exemplo, computador \_ a, use o seguinte parâmetro de caminho de objeto:</span><span class="sxs-lookup"><span data-stu-id="7ce8f-112">To connect to a remote computer, for example Computer\_A, use the following object path parameter:</span></span>

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    <span data-ttu-id="7ce8f-113">Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-113">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="7ce8f-114">Defina a segurança do proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-114">Set the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="7ce8f-115">Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-115">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

5.  <span data-ttu-id="7ce8f-116">Use o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações do WMI.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-116">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="7ce8f-117">Por exemplo, consultar todas as instâncias de [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) para determinar quais serviços são interrompidos.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-117">For example, querying for all the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instances to determine which services are stopped.</span></span>

    <span data-ttu-id="7ce8f-118">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [consultando o WMI](querying-wmi.md)e [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

6.  <span data-ttu-id="7ce8f-119">Limpar objetos e COM.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-119">Clean up objects and COM.</span></span>

    <span data-ttu-id="7ce8f-120">Para obter mais informações, consulte [limpando e desligando um aplicativo WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="7ce8f-120">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

<span data-ttu-id="7ce8f-121">O código de exemplo a seguir é um aplicativo cliente WMI completo.</span><span class="sxs-lookup"><span data-stu-id="7ce8f-121">The following example code is a complete WMI client application.</span></span>


```C++

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Initialize COM.
    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        return 1;              // Program has failed.
    }

    // Initialize 
    hres =  CoInitializeSecurity(
        NULL,     
        -1,      // COM negotiates service                  
        NULL,    // Authentication services
        NULL,    // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,    // authentication
        RPC_C_IMP_LEVEL_IMPERSONATE,  // Impersonation
        NULL,             // Authentication info 
        EOAC_NONE,        // Additional capabilities
        NULL              // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;          // Program has failed.
    }

    // Obtain the initial locator to Windows Management
    // on a particular host computer.
    IWbemLocator *pLoc = 0;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
            << "Error code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;       // Program has failed.
    }

    IWbemServices *pSvc = 0;

    // Connect to the root\cimv2 namespace with the
    // current user and obtain pointer pSvc
    // to make IWbemServices calls.

    hres = pLoc->ConnectServer(
        
        _bstr_t(L"ROOT\\CIMV2"), // WMI namespace
        NULL,                    // User name
        NULL,                    // User password
        0,                       // Locale
        NULL,                    // Security flags                 
        0,                       // Authority       
        0,                       // Context object
        &pSvc                    // IWbemServices proxy
        );                              
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
            << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;

    // Set the IWbemServices proxy so that impersonation
    // of the user (client) occurs.
    hres = CoSetProxyBlanket(
       
       pSvc,                         // the proxy to set
       RPC_C_AUTHN_WINNT,            // authentication service
       RPC_C_AUTHZ_NONE,             // authorization service
       NULL,                         // Server principal name
       RPC_C_AUTHN_LEVEL_CALL,       // authentication level
       RPC_C_IMP_LEVEL_IMPERSONATE,  // impersonation level
       NULL,                         // client identity 
       EOAC_NONE                     // proxy capabilities     
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }


    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:

    // For example, query for all the running processes
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_Process"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
    else
    { 
        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
   
        while (pEnumerator)
        {
            hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                &pclsObj, &uReturn);

            if(0 == uReturn)
            {
                break;
            }

            VARIANT vtProp;

            // Get the value of the Name property
            hres = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
            wcout << "Process Name : " << vtProp.bstrVal << endl;
            VariantClear(&vtProp);
            
            pclsObj->Release();
            pclsObj = NULL;
        }
         
    }
 
    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();  
    
    CoUninitialize();

    return 0;   // Program successfully completed.
}
```



 

 
