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
# <a name="initializing-com-for-a-wmi-application"></a>Inicializando COM para um aplicativo WMI

A primeira etapa na conexão com o WMI é configurar as chamadas COM para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir descreve como inicializar COM de um aplicativo cliente.

**Para inicializar COM de um aplicativo cliente**

1.  Inicialize com com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) é um procedimento padrão para configurar uma interface com. Portanto, o WMI não exige que você observe quaisquer procedimentos adicionais ao chamar **CoInitializeEx**. Para obter mais informações, consulte [com](../com/component-object-model--com--portal.md).

    O exemplo de código a seguir descreve como chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Defina os níveis gerais de segurança com com uma chamada para a interface [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) é uma função padrão que você deve chamar ao configurar uma interface com para um processo. Chame **CoInitializeSecurity** se você quiser definir as configurações de segurança padrão para autenticação, representação ou serviço de autenticação para um processo inteiro. Para obter mais informações, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md). Se você quiser definir ou alterar a segurança de um proxy específico, deverá chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Use **CoSetProxyBlanket** sempre que for necessário definir ou alterar a segurança com ao executar dentro de outro processo em que você não possa controlar as configurações de segurança padrão para autenticação, representação ou serviço de autenticação. Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md) e [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

    O WMI tem vários problemas de segurança dos quais você deve estar atento ao programar um aplicativo cliente do WMI. Para obter mais informações, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).

    O exemplo de código a seguir descreve como chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança com no processo.

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

    

Depois de inicializar o COM, a próxima etapa é criar uma conexão com um namespace do WMI. Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
