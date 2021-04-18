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
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Definindo os níveis de segurança em uma conexão WMI

Depois de recuperar um ponteiro para um proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você deve definir a segurança no proxy para acessar o WMI por meio do proxy. Você deve definir a segurança porque o proxy de **IWbemServices** concede acesso a um objeto fora do processo. Em geral, a segurança COM não permite que um processo acesse outro processo se você não definir as propriedades de segurança adequadas. Para obter mais informações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md). As conexões com diferentes sistemas operacionais exigem níveis variados de autenticação e representação. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir descreve como definir os níveis de segurança em uma conexão WMI.

**Para definir os níveis de segurança em uma conexão WMI**

-   Defina os níveis de segurança no proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com uma chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

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

    

Depois de definir os níveis de segurança para o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você pode acessar os vários recursos do WMI. Depois de terminar de usar o WMI, você deve desligar o aplicativo. Para obter mais informações, consulte [limpando e desligando um aplicativo WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
