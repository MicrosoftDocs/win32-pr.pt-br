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
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170604"
---
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="d812e-103">Solucionando problemas de aplicativos cliente WMI</span><span class="sxs-lookup"><span data-stu-id="d812e-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="d812e-104">O WMI contém um conjunto de classes para [solucionar problemas](wmi-troubleshooting-classes.md) de aplicativos cliente que usam provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="d812e-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="d812e-105">As classes de evento de solução de problemas são associadas a classes de evento WMI, de modo que você pode acompanhar a execução do aplicativo usando um log de eventos de solução de problemas capturados.</span><span class="sxs-lookup"><span data-stu-id="d812e-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="d812e-106">A lista a seguir contém exemplos de classes de evento de solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="d812e-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="d812e-107">**MSFT \_ WmiProvider \_ ExecMethodAsyncEvent \_ pré**</span><span class="sxs-lookup"><span data-stu-id="d812e-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="d812e-108">Gerado antes que o WMI chame [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) no provedor.</span><span class="sxs-lookup"><span data-stu-id="d812e-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="d812e-109">**MSFT \_ WmiProvider \_ ExecMethodAsyncEvent \_ post**</span><span class="sxs-lookup"><span data-stu-id="d812e-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="d812e-110">Gerado depois que o WMI chama [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) no provedor.</span><span class="sxs-lookup"><span data-stu-id="d812e-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="d812e-111">O procedimento a seguir mostra como solucionar problemas de execução do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d812e-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="d812e-112">**Para configurar a solução de problemas do WMI**</span><span class="sxs-lookup"><span data-stu-id="d812e-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="d812e-113">Crie e compile um arquivo MOF para usar o consumidor de evento de log WMI.</span><span class="sxs-lookup"><span data-stu-id="d812e-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="d812e-114">Execute o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="d812e-114">Run your client application.</span></span>
3.  <span data-ttu-id="d812e-115">Exiba o arquivo de log de solução de problemas para todos os eventos de operação e falha do provedor e analise o log para diagnosticar os problemas do cliente que você está encontrando.</span><span class="sxs-lookup"><span data-stu-id="d812e-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="d812e-116">Outra abordagem de solução de problemas é exibir a lista de provedores atualmente no cache do computador, enumerando [**\_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) no namespace **raiz \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="d812e-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="d812e-117">Há métodos nessa classe que permitem carregar e descarregar provedores para fins de depuração ou instalação.</span><span class="sxs-lookup"><span data-stu-id="d812e-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="d812e-118">O exemplo de código a seguir usa o consumidor de evento de log WMI para capturar todos os eventos da classe de evento pai, capturando assim todos os eventos de operação do provedor.</span><span class="sxs-lookup"><span data-stu-id="d812e-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

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

<span data-ttu-id="d812e-119">Quando as mensagens de erro indicam falha de carregamento do provedor, use [**MSFT \_ WmiProvider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) para identificar qual provedor causou a falha.</span><span class="sxs-lookup"><span data-stu-id="d812e-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d812e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d812e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d812e-121">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="d812e-121">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="d812e-122">Classes de solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="d812e-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
