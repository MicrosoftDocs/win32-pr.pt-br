---
description: Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, recupera dados semisynchronously e, em seguida, limpa.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Exemplo: obtendo dados WMI do computador local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71036d95996926ce9e5a0200587a15abb8dc992c82999aa65c54be50d0e1691b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050904"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Exemplo: obtendo dados WMI do computador local

Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI no computador local, recupera dados semisynchronously e, em seguida, limpa. Este exemplo obtém o nome do sistema operacional no computador local e o exibe. Para recuperar dados de um computador remoto, consulte [exemplo: obtendo dados WMI de um computador remoto](example--getting-wmi-data-from-a-remote-computer.md). Para obter os dados de forma assíncrona, consulte [exemplo: obtendo dados do WMI do computador local de forma assíncrona](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

O procedimento a seguir é usado para executar o aplicativo WMI. As etapas de 1 a 5 contêm todas as etapas necessárias para configurar e conectar-se ao WMI, e as etapas 6 e 7 são onde os dados são consultados e recebidos.

1.  Inicialize parâmetros COM com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

2.  Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).

3.  Obtenha o localizador inicial para o WMI chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para o \\ namespace raiz cimv2 no computador local chamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Para se conectar a um computador remoto, consulte [exemplo: obtendo dados WMI de um computador remoto](example--getting-wmi-data-from-a-remote-computer.md).

    Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  Defina a segurança do proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

6.  Use o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações do WMI. Este exemplo executa uma consulta para o nome do sistema operacional chamando [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    A consulta WQL a seguir é um dos argumentos do método.

    `SELECT * FROM Win32_OperatingSystem`

    O resultado dessa consulta é armazenado em um ponteiro [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Isso permite que os objetos de dados da consulta sejam recuperados semisynchronously com a interface **IEnumWbemClassObject** . Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md). Para obter os dados de forma assíncrona, consulte [exemplo: obtendo dados do WMI do computador local de forma assíncrona](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

    Para obter mais informações sobre como fazer solicitações ao WMI, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [consultando o WMI](querying-wmi.md)e [chamando um método](calling-a-method.md).

7.  Obter e exibir os dados da consulta WQL. O ponteiro [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) é vinculado aos objetos de dados retornados pela consulta e os objetos de dados podem ser recuperados com o método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) . Esse método vincula os objetos de dados a um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que é passado para o método. Use o método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) para obter as informações desejadas dos objetos de dados.

    O exemplo de código a seguir é usado para obter a propriedade Name do objeto de dados, que fornece o nome do sistema operacional.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    Depois que o valor da propriedade Name é armazenado na variável [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp, ele pode ser exibido para o usuário.

    Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).

O exemplo de código a seguir recupera o WMI data semisynchronously de um computador local.


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
        -1,                          // COM authentication
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
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
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

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
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



 

 
