---
description: Você pode usar o procedimento e o exemplo de código neste tópico para concluir o aplicativo cliente WMI que executa a inicialização COM, conecta-se ao WMI no computador local, recebe uma notificação de evento e, em seguida, limpa.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: 'Exemplo: recebendo notificações de eventos por meio do WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759ed91ed1f7892b622089fa64fe8e8421a8b3bd73bf77ba2f60fa4199d25434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411876"
---
# <a name="example-receiving-event-notifications-through-wmi"></a>Exemplo: recebendo notificações de eventos por meio do WMI

Você pode usar o procedimento e o exemplo de código neste tópico para concluir o aplicativo cliente WMI que executa a inicialização COM, conecta-se ao WMI no computador local, recebe uma notificação de evento e, em seguida, limpa. O exemplo notifica o usuário de um evento quando um novo processo é criado. Os eventos são recebidos de forma assíncrona.

O procedimento a seguir é usado para executar o aplicativo WMI. As etapas 1 a 5 contêm todas as etapas necessárias para configurar e se conectar ao WMI e a etapa 6 é onde as notificações de evento são recebidas.

**Para receber uma notificação de evento por meio do WMI**

1.  Inicialize parâmetros COM com uma chamada para [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Para obter mais informações, consulte [Inicializando COM para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

2.  Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Para obter mais informações, consulte [Definindo o nível de segurança do processo padrão usando C++.](setting-the-default-process-security-level-using-c-.md)

3.  Obtenha o localizador inicial para o WMI chamando [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Para obter mais informações, consulte [Criando uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para o namespace raiz cimv2 no computador local chamando \\ [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Para se conectar a um computador remoto, consulte [Exemplo: Obter dados WMI de um computador remoto.](example--getting-wmi-data-from-a-remote-computer.md)

    Para obter mais informações, consulte [Criando uma conexão com um namespace WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  De definir a segurança de proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Para obter mais informações, consulte [Definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

6.  Use o [**ponteiro IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações ao WMI. Este exemplo usa o [**método IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para receber eventos assíncronos. Ao receber eventos assíncronos, você deve fornecer uma implementação [**de IWbemObjectSink.**](iwbemobjectsink.md) Este exemplo fornece a implementação na classe EventSink. O código de implementação e o código de arquivo de header para essa classe são fornecidos abaixo do exemplo principal. O **método IWbemServices::ExecNotificationQueryAsync** chama o **método EventSink::Indicate** sempre que um evento é recebido. Para este exemplo, **o método EventSink::Indicate** é chamado sempre que um processo é criado. Para testar este exemplo, execute o código e inicie um processo como Notepad.exe. Isso dispara uma notificação de evento.

    Para obter mais informações sobre como fazer solicitações de WMI, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e chamando um [método](calling-a-method.md).

O código de exemplo a seguir recebe notificações de eventos por meio do WMI.


```C++
#include "eventsink.h"

int main(int iArgCnt, char ** argv)
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

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
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
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
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


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
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

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



O arquivo de header a seguir é usado para a classe EventSink. A classe EventSink é usada no exemplo de código anterior.


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

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
};

#endif    // end of EventSink.h
```



O código de exemplo a seguir é uma implementação da classe EventSink.


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
