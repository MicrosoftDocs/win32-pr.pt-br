---
description: Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa a inicialização COM, conecta-se ao WMI no computador local, obtém dados de forma assíncrona e, em seguida, limpa.
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: 'Exemplo: Obter dados WMI do computador local de forma assíncrona'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67eb71247816319553389c451dd2e7ad268c49ee7aadeaddc118a3f08448171b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319424"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a>Exemplo: Obter dados WMI do computador local de forma assíncrona

Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa a inicialização COM, conecta-se ao WMI no computador local, obtém dados de forma assíncrona e, em seguida, limpa. Este exemplo obtém o nome do sistema operacional no computador local e o exibe.

O procedimento a seguir é usado para executar o aplicativo WMI. As etapas 1 a 5 contêm todas as etapas necessárias para configurar e se conectar ao WMI, e as etapas 6 e 7 são onde o nome do sistema operacional é recuperado de forma assíncrona.

**Para obter dados WMI do computador local de forma assíncrona**

1.  Inicialize parâmetros COM com uma chamada para [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Para obter mais informações, consulte [Inicializando COM para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

2.  Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Para obter mais informações, consulte [Definindo o nível de segurança do processo padrão usando C++.](setting-the-default-process-security-level-using-c-.md)

3.  Obtenha o localizador inicial para o WMI chamando [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Para obter mais informações, consulte [Criando uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para o namespace raiz cimv2 no computador local chamando \\ [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Para obter mais informações sobre como se conectar a um computador remoto, consulte [Exemplo: Obter dados WMI de um computador remoto.](example--getting-wmi-data-from-a-remote-computer.md)

    Para obter mais informações, consulte [Criando uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  De definir a segurança de proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Para obter mais informações, consulte [Definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

6.  Use o [**ponteiro IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações ao WMI. Este exemplo usa o [**método IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) para receber os dados de forma assíncrona. Sempre que receber dados de forma assíncrona, você deverá fornecer uma implementação [**de IWbemObjectSink.**](iwbemobjectsink.md) Este exemplo fornece a implementação na classe QuerySink. O código de implementação e o código de arquivo de header para essa classe são fornecidos seguindo o exemplo principal. O **método IWbemServices::ExecQueryAsync** chama o método QuerySink::Indicate sempre que os dados são recebidos.

    Para obter mais informações sobre como criar uma solicitação WMI, consulte [Manipulando](manipulating-class-and-instance-information.md) informações de classe e instância e [chamando um método](calling-a-method.md).

7.  Aguarde até que os dados sejam recuperados de forma assíncrona. Use o [**método IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para interromper manualmente a chamada assíncrona.

O exemplo de código a seguir obtém dados WMI do computador local de forma assíncrona.


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



O arquivo de header a seguir é usado para a classe QuerySink. A classe QuerySink é usada no exemplo de código anterior.


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



O exemplo de código a seguir é uma implementação da classe QuerySink.


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



 

 
