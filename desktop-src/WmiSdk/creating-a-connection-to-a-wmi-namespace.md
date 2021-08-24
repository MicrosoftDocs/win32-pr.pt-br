---
description: Depois de definir as chamadas padrão como COM, você deve se conectar ao WMI por meio de uma chamada para o método IWbemLocator::ConnectServer.
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Criando uma conexão com um namespace WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587024d7f581cd28a8fdaf339db9567b17c509599c01aca0599b701186fb786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412136"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Criando uma conexão com um namespace WMI

Depois de definir as chamadas padrão como COM, você deve se conectar ao WMI por meio de uma chamada para o [**método IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) O **método ConnectServer** retorna um proxy de uma interface [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Por **meio de IWbemServices,** você pode acessar os diferentes recursos do WMI.

Os exemplos de código neste tópico exigem as seguintes referências e \# instruções include para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir descreve como criar uma conexão com um namespace WMI.

**Para criar uma conexão com um namespace WMI**

-   Inicialize a interface [**IWbemLocator por**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) meio de uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    O WMI não exige que você execute nenhum procedimento adicional ao chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em [**IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

    O exemplo de código a seguir descreve como inicializar [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

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

    

    -   Conexão para WMI por meio de uma chamada para o [**método IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)

        O [**método ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) retorna um proxy para uma interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que usa para acessar o namespace WMI local ou remoto especificado em sua chamada para **ConnectServer**.

        O exemplo de código a seguir descreve como chamar [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

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

        

Depois de receber um ponteiro para o proxy [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) você deve definir a segurança no proxy para acessar o WMI. Para obter mais informações, consulte [Definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
