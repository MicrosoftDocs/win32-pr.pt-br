---
description: Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, obtém dados de forma assíncrona e, em seguida, limpa.
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: 'Exemplo: obtendo dados do WMI do computador local de forma assíncrona'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acf8df91b5ff279d70a9f76f0a353df90e8ff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091785"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a><span data-ttu-id="3dda3-103">Exemplo: obtendo dados do WMI do computador local de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3dda3-103">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>

<span data-ttu-id="3dda3-104">Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, obtém dados de forma assíncrona e, em seguida, limpa.</span><span class="sxs-lookup"><span data-stu-id="3dda3-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, gets data asynchronously, and then cleans up.</span></span> <span data-ttu-id="3dda3-105">Este exemplo obtém o nome do sistema operacional no computador local e o exibe.</span><span class="sxs-lookup"><span data-stu-id="3dda3-105">This example gets the name of the operating system on the local computer and displays it.</span></span>

<span data-ttu-id="3dda3-106">O procedimento a seguir é usado para executar o aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="3dda3-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="3dda3-107">As etapas de 1 a 5 contêm todas as etapas necessárias para configurar e conectar-se ao WMI, e as etapas 6 e sete são onde o nome do sistema operacional é recuperado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dda3-107">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and seven are where the operating system name is retrieved asynchronously.</span></span>

<span data-ttu-id="3dda3-108">**Para obter dados WMI do computador local de forma assíncrona**</span><span class="sxs-lookup"><span data-stu-id="3dda3-108">**To get WMI data from the local computer asynchronously**</span></span>

1.  <span data-ttu-id="3dda3-109">Inicialize parâmetros COM com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="3dda3-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="3dda3-110">Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="3dda3-111">Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="3dda3-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="3dda3-112">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="3dda3-113">Obtenha o localizador inicial para o WMI chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3dda3-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="3dda3-114">Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="3dda3-115">Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para o \\ namespace raiz cimv2 no computador local chamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="3dda3-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="3dda3-116">Para obter mais informações sobre como se conectar a um computador remoto, consulte [exemplo: obtendo dados WMI de um computador remoto](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-116">For more information about how to connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="3dda3-117">Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="3dda3-118">Defina a segurança do proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="3dda3-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="3dda3-119">Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="3dda3-120">Use o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações ao WMI.</span><span class="sxs-lookup"><span data-stu-id="3dda3-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="3dda3-121">Este exemplo usa o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) para receber os dados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dda3-121">This example uses the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method to receive the data asynchronously.</span></span> <span data-ttu-id="3dda3-122">Sempre que você receber dados de forma assíncrona, deverá fornecer uma implementação de [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-122">Whenever you receive data asynchronously, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="3dda3-123">Este exemplo fornece a implementação na classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="3dda3-123">This example provides the implementation in the QuerySink class.</span></span> <span data-ttu-id="3dda3-124">O código de implementação e o código do arquivo de cabeçalho para essa classe são fornecidos seguindo o exemplo principal.</span><span class="sxs-lookup"><span data-stu-id="3dda3-124">The implementation code and header file code for this class are provided following the main example.</span></span> <span data-ttu-id="3dda3-125">O método **IWbemServices:: ExecQueryAsync** chama o método QuerySink:: indica sempre que os dados são recebidos.</span><span class="sxs-lookup"><span data-stu-id="3dda3-125">The **IWbemServices::ExecQueryAsync** method calls the QuerySink::Indicate method whenever the data is received.</span></span>

    <span data-ttu-id="3dda3-126">Para obter mais informações sobre como criar uma solicitação WMI, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3dda3-126">For more information about how to create a WMI request, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="3dda3-127">Aguarde até que os dados sejam recuperados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dda3-127">Wait for the data to be retrieved asynchronously.</span></span> <span data-ttu-id="3dda3-128">Use o método [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para interromper manualmente a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dda3-128">Use the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method to manually stop the asynchronous call.</span></span>

<span data-ttu-id="3dda3-129">O exemplo de código a seguir obtém dados do WMI do computador local de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3dda3-129">The following code example gets WMI data from the local computer asynchronously.</span></span>


```C++
#include "querysink.h"


int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(NULL, 
                                 -1,                          // COM authentication
                                 NULL,                        // Authentication services
                                 NULL,                        // Reserved
                                 RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
                                 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
                                 NULL,                        // Authentication info
                                 EOAC_NONE,                   // Additional capabilities 
                                 NULL);                       // Reserved

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(_bstr_t(L"ROOT\\CIMV2"), 
                               NULL,
                               NULL,
                               0,
                               NULL,
                               0,
                               0, 
                               &pSvc);
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(pSvc,                        // Indicates the proxy to set
                             RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
                             RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
                             NULL,                        // Server principal name 
                             RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
                             RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
                             NULL,                        // client identity
                             EOAC_NONE);                  // proxy capabilities 

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system.
    // The IWbemService::ExecQueryAsync method will call
    // the QuerySink::Indicate method when it receives a result
    // and the QuerySink::Indicate method will display the OS name
    QuerySink* pResponseSink = new QuerySink();
    pResponseSink->AddRef();
    hres = pSvc->ExecQueryAsync(bstr_t("WQL"), 
                                bstr_t("SELECT * FROM Win32_OperatingSystem"),
                                WBEM_FLAG_BIDIRECTIONAL, 
                                NULL,
                                pResponseSink);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        pResponseSink->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Wait to get the data from the query in step 6 -----------
    Sleep(500);
    pSvc->CancelAsyncCall(pResponseSink);

    // Cleanup
    // ========
    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="3dda3-130">O arquivo de cabeçalho a seguir é usado para a classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="3dda3-130">The following header file is used for the QuerySink class.</span></span> <span data-ttu-id="3dda3-131">A classe QuerySink é usada no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="3dda3-131">The QuerySink class is used in the previous code example.</span></span>


```C++
// QuerySink.h
#ifndef QUERYSINK_H
#define QUERYSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;
 CRITICAL_SECTION threadLock; // for thread safety

public:
    QuerySink() { m_lRef = 0; bDone = false; 
     InitializeCriticalSection(&threadLock); }
    ~QuerySink() { bDone = true;
        DeleteCriticalSection(&threadLock); }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid,
        void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );

 bool IsDone();
};

#endif    // end of QuerySink.h
```



<span data-ttu-id="3dda3-132">O exemplo de código a seguir é uma implementação da classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="3dda3-132">The following code example is an implementation of the QuerySink class.</span></span>


```C++
// QuerySink.cpp
#include "querysink.h"

ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        VARIANT varName;
        hres = apObjArray[i]->Get(_bstr_t(L"Name"),
            0, &varName, 0, 0);

        if (FAILED(hres))
        {
            cout << "Failed to get the data from the query"
                << " Error code = 0x"
                << hex << hres << endl;
            return WBEM_E_FAILED;       // Program has failed.
        }

        printf("Name: %ls\n", V_BSTR(&varName));
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
 if(lFlags == WBEM_STATUS_COMPLETE)
 {
  printf("Call complete.\n");

  EnterCriticalSection(&threadLock);
  bDone = true;
  LeaveCriticalSection(&threadLock);
 }
 else if(lFlags == WBEM_STATUS_PROGRESS)
 {
  printf("Call in progress.\n");
 }
    
    return WBEM_S_NO_ERROR;
}


bool QuerySink::IsDone()
{
    bool done = true;

 EnterCriticalSection(&threadLock);
 done = bDone;
 LeaveCriticalSection(&threadLock);

    return done;
}    // end of QuerySink.cpp
```



 

 
