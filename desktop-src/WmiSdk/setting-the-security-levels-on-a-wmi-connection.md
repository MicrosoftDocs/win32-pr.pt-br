---
description: Depois de recuperar um ponteiro para um proxy IWbemServices, você deve definir a segurança no proxy para acessar o WMI por meio do proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Definindo os níveis de segurança em uma conexão WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315320"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Definindo os níveis de segurança em uma conexão WMI

Depois de recuperar um ponteiro para um proxy [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) você deve definir a segurança no proxy para acessar o WMI por meio do proxy. Você deve definir a segurança porque o proxy **IWbemServices** concede acesso a um objeto fora do processo. Em geral, a segurança COM não permitirá que um processo acesse outro processo se você não definir as propriedades de segurança apropriadas. Para obter mais informações, [consulte Definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md). As conexões com diferentes sistemas operacionais exigem níveis variados de autenticação e representação. Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)

Os exemplos de código neste tópico exigem as seguintes referências e \# instruções include para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir descreve como definir os níveis de segurança em uma conexão WMI.

**Para definir os níveis de segurança em uma conexão WMI**

-   Definir os níveis de segurança no proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com uma chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    O exemplo de código a seguir descreve uma maneira comum de chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

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

    

Depois de definir os níveis de segurança para o [**ponteiro IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) você pode acessar os vários recursos do WMI. Depois de terminar de usar o WMI, você deve desligar seu aplicativo. Para obter mais informações, [consulte Limpando e desligando um aplicativo WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
