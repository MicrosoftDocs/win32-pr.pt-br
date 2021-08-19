---
description: O WMI contém um conjunto de classes para solucionar problemas de aplicativos cliente que usam provedores WMI.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Solucionando problemas de aplicativos cliente WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050024"
---
# <a name="troubleshooting-wmi-client-applications"></a>Solucionando problemas de aplicativos cliente WMI

O WMI contém um conjunto de classes para [solucionar problemas](wmi-troubleshooting-classes.md) de aplicativos cliente que usam provedores WMI. As classes de evento de solução de problemas são associadas a classes de evento WMI, de modo que você pode acompanhar a execução do aplicativo usando um log de eventos de solução de problemas capturados.

A lista a seguir contém exemplos de classes de evento de solução de problemas:

-   [**MSFT \_ WmiProvider \_ ExecMethodAsyncEvent \_ pré**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Gerado antes que o WMI chame [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) no provedor.

-   [**MSFT \_ WmiProvider \_ ExecMethodAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Gerado depois que o WMI chama [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) no provedor.

O procedimento a seguir mostra como solucionar problemas de execução do aplicativo.

**Para configurar a solução de problemas do WMI**

1.  Crie e compile um arquivo MOF para usar o consumidor de evento de log WMI.
2.  Execute o aplicativo cliente.
3.  Exiba o arquivo de log de solução de problemas para todos os eventos de operação e falha do provedor e analise o log para diagnosticar os problemas do cliente que você está encontrando.

Outra abordagem de solução de problemas é exibir a lista de provedores atualmente no cache do computador, enumerando [**\_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) no namespace **raiz \\ cimv2** . Há métodos nessa classe que permitem carregar e descarregar provedores para fins de depuração ou instalação.

O exemplo de código a seguir usa o consumidor de evento de log WMI para capturar todos os eventos da classe de evento pai, capturando assim todos os eventos de operação do provedor.

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

Quando as mensagens de erro indicam falha de carregamento do provedor, use [**MSFT \_ WmiProvider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) para identificar qual provedor causou a falha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de solução de problemas do WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
