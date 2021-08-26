---
description: Depois de definir os níveis de segurança para o ponteiro IWbemServices, você pode acessar os vários recursos do WMI. Depois de terminar de usar o WMI, você deve desligar seu aplicativo.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Limpando e desligando um aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120906"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Limpando e desligando um aplicativo WMI

Depois de definir os níveis de segurança para o [**ponteiro IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) você pode acessar os vários recursos do WMI. Depois de terminar de usar o WMI, você deve desligar seu aplicativo.

O procedimento a seguir descreve como limpar e desligar um aplicativo WMI.

**Para limpar e desligar um aplicativo WMI**

1.  Libere qualquer interface COM aberta.

    As duas interfaces principais que você deve lembrar de lançar [**são IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**e IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

2.  Chame [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Assim como com todos os aplicativos COM, você deve chamar [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) no final do aplicativo.

3.  Saia do aplicativo.

    O exemplo de código a seguir mostra como sair de um aplicativo cliente WMI.

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > A `pSvc` variável é do [**tipo IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* e a variável pLoc é do tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

Agora você inicializou com êxito o COM, acessou o WMI e saiu do aplicativo. Para obter mais informações, consulte [Exemplo: criando um aplicativo WMI](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
