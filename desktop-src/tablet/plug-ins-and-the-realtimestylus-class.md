---
description: O objeto RealTimeStylus foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta do tablet.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins e a classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843376"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-ins e a classe RealTimeStylus

O [**objeto RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta do tablet. Plug-ins, objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) podem ser adicionados a um **objeto RealTimeStylus.** Plug-ins síncronos geralmente são chamados diretamente pelo objeto **RealTimeStylus** em um thread de alta prioridade, enquanto plug-ins assíncronos geralmente são chamados no thread da interface do usuário do aplicativo. Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real ao fluxo de dados e são computacionalmente indesejáveis, como filtragem de pacotes. Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como coleta de tinta.

Determinadas tarefas podem ser computacionalmente exigentes, mas exigem acesso em tempo real ao fluxo de dados, como o reconhecimento de gestos multivaluário. Para atender a essas necessidades, as APIs StylusInput fornecem um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus,** cada um em execução em seu próprio thread. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte O modelo [RealTimeStylus](the-cascaded-realtimestylus-model.md)em cascata .

As interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) [**e IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definem os mesmos métodos. Esses métodos permitem que o objeto [**RealTimeStylus**](realtimestylus-class.md) passe os dados da caneta para cada plug-in, independentemente de ser um plug-in assíncrono ou síncrono. As propriedades [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) permitem que cada plug-in assine dados específicos no fluxo de dados da caneta tablet. Um plug-in só deve assinar os dados necessários para executar sua tarefa, minimizando as demandas de desempenho. Para obter mais informações sobre threading e a **classe RealTimeStylus,** consulte Considerações de threading para as [APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).

O [**objeto RealTimeStylus**](realtimestylus-class.md) usa objetos no namespace [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) para passar os dados da caneta para seus plug-ins. A **RealTimeStylus** também captura exceções lançadas por plug-ins. Quando **a RealTimeStylus** captura exceções, ela notifica os plug-ins chamando o método [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) ou [IStylusAsyncPlugin.Error.](/previous-versions/ms824771(v=msdn.10)) Para obter mais informações sobre como usar dados de [plug-in, consulte Dados de plug-in e a classe RealTimeStylus.](plug-in-data-and-the-realtimestylus-class.md) Para obter mais informações sobre o tratamento de erros, consulte Considerações de tratamento de erros para as [APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e a seção Dados de Erro de Dados de Plug-in e a Classe RealTimeStylus.

> [!Note]  
> Pelo menos um plug-in deve ser anexado ao objeto [**RealTimeStylus**](realtimestylus-class.md) antes que o **objeto RealTimeStylus** possa ser habilitado.

 

Os tópicos a seguir descrevem algumas categorias comuns de plug-ins.

-   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
-   [Plug-ins de renderização dinâmica](dynamic-renderer-plug-ins.md)
-   [Plug-ins do Reconhecedor](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Considerações especiais

Devido à natureza complexa do objeto [**RealTimeStylus,**](realtimestylus-class.md) você deve anotar o seguinte.

O [**objeto RealTimeStylus**](realtimestylus-class.md) lançará uma exceção se um plug-in modificar a coleção de plug-ins à qual ele está anexado. Isso acontece somente quando o plug-in faz isso enquanto ele está sendo chamado pelo **objeto RealTimeStylus** como um membro dessa coleção.

O exemplo C \# a seguir é o código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



O [**objeto RealTimeStylus**](realtimestylus-class.md) lançará uma exceção se um plug-in chamar o método [Dispose](/previous-versions/ms825891(v=msdn.10)) do objeto **RealTimeStylus.** Isso acontece somente quando o plug-in faz isso enquanto ele está sendo chamado pelo **objeto RealTimeStylus.**

O exemplo C \# a seguir é o código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



Coleções de plug-in podem ser modificadas enquanto o [**objeto RealTimeStylus**](realtimestylus-class.md) está habilitado; no entanto, isso pode dificultar a previsão do comportamento do aplicativo. Quando um plug-in é adicionado enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) ou [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) do plug-in. Quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ou [IStylusSyncPlugin.RealTimeStylusDisabled do](/previous-versions/ms824757(v=msdn.10)) plug-in. Isso permite que o plug-in mantenha seu estado adequado sem precisar verificar a propriedade [Enabled](/previous-versions/ms824832(v=msdn.10)) do **objeto RealTimeStylus.**

Quando um plug-in é adicionado enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, os dados de plug-in recebidos pelo plug-in podem não conter informações suficientes para estabelecer adequadamente o contexto dos dados iniciais. Por exemplo, o plug-in recém-adicionado pode começar a receber dados de pacote de uma caneta com traço médio. Da mesma forma, quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, os dados de plug-in recebidos pelo plug-in podem ser insuficientes para concluir o processamento dos dados.

> [!Note]  
> Para estabilidade geral, redefina o estado interno de um plug-in quando seu [**método RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) for chamado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerações sobre tratamento de erros para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
