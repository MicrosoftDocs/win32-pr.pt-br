---
description: O objeto RealTimeStylus foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta eletrônica.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins e a classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810755"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-ins e a classe RealTimeStylus

O objeto [**RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta eletrônica. Plug-ins, objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , podem ser adicionados a um objeto **RealTimeStylus** . Plug-ins síncronos são geralmente chamados diretamente pelo objeto **RealTimeStylus** em um thread de alta prioridade, enquanto plug-ins assíncronos são geralmente chamados no thread da interface do usuário do aplicativo. Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real ao fluxo de dados e são de cálculo computacional, como a filtragem de pacotes. Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como a coleta de tinta.

Determinadas tarefas podem ser computacionalmente exigentes, mas exigem acesso em tempo real ao fluxo de dados, como o reconhecimento de gestos com vários traços. Para atender a essas necessidades, as APIs StylusInput fornecem um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus** , cada um em execução em seu próprio thread. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

As interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definem os mesmos métodos. Esses métodos permitem que o objeto [**RealTimeStylus**](realtimestylus-class.md) passe os dados da caneta para cada plug-in, independentemente de ser um plug-in assíncrono ou síncrono. As propriedades [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) permitem que cada plug-in assine dados específicos no fluxo de dados da caneta eletrônica. Um plug-in deve assinar apenas os dados necessários para executar sua tarefa, minimizando as demandas de desempenho. Para obter mais informações sobre Threading e a classe **RealTimeStylus** , consulte [considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) usa objetos no namespace [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para passar os dados da caneta para seus plug-ins. O **RealTimeStylus** também captura exceções geradas por plug-ins. Quando o **RealTimeStylus** captura exceções, ele notifica os plug-ins chamando o método [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) . Para obter mais informações sobre como usar dados de plug-in, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) . Para obter mais informações sobre o tratamento de erros, consulte [considerações de tratamento de erros para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e a seção dados de erro de dados de plug-in e a classe RealTimeStylus.

> [!Note]  
> Pelo menos um plug-in deve ser anexado ao objeto [**RealTimeStylus**](realtimestylus-class.md) antes que o objeto **RealTimeStylus** possa ser habilitado.

 

Os tópicos a seguir descrevem algumas categorias comuns de plug-ins.

-   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
-   [Plug-ins de processamento dinâmico](dynamic-renderer-plug-ins.md)
-   [Plug-ins do Recognizer](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Considerações especiais

Devido à natureza complexa do objeto [**RealTimeStylus**](realtimestylus-class.md) , você deve anotar o seguinte.

O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção se um plug-in modifica a coleção de plug-ins à qual está anexada. Isso ocorre apenas quando o plug-in faz isso enquanto está sendo chamado pelo objeto **RealTimeStylus** como um membro dessa coleção.

O exemplo C a seguir \# é um código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gere uma exceção.


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



O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção se um plug-in chama o método [Dispose](/previous-versions/ms825891(v=msdn.10)) do objeto **RealTimeStylus** . Isso ocorre apenas quando o plug-in faz isso enquanto está sendo chamado pelo objeto **RealTimeStylus** .

O exemplo C a seguir \# é um código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gere uma exceção.


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



As coleções de plug-ins podem ser modificadas enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; no entanto, isso pode tornar o comportamento do seu aplicativo mais difícil de prever. Quando um plug-in é adicionado enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) ou [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) do plug-in. Quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ou [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) do plug-in. Isso permite que o plug-in Mantenha seu estado adequado sem precisar verificar a propriedade [Enabled](/previous-versions/ms824832(v=msdn.10)) do objeto **RealTimeStylus** .

Quando um plug-in é adicionado enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, os dados de plug-in que o plug-in recebe podem não conter informações suficientes para estabelecer adequadamente o contexto dos dados iniciais. Por exemplo, o plug-in recém-adicionado pode começar a receber dados de pacote de uma caneta que está em um traço intermediário. Da mesma forma, quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, os dados de plug-in que o plug-in recebeu podem não ser suficientes para concluir o processamento dos dados.

> [!Note]  
> Para a estabilidade geral, redefina o estado interno de um plug-in quando o método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) for chamado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerações de tratamento de erro para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
