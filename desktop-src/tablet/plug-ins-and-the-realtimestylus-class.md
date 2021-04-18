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
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="71aa3-103">Plug-ins e a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="71aa3-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="71aa3-104">O objeto [**RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="71aa3-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="71aa3-105">Plug-ins, objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , podem ser adicionados a um objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="71aa3-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="71aa3-106">Plug-ins síncronos são geralmente chamados diretamente pelo objeto **RealTimeStylus** em um thread de alta prioridade, enquanto plug-ins assíncronos são geralmente chamados no thread da interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71aa3-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="71aa3-107">Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real ao fluxo de dados e são de cálculo computacional, como a filtragem de pacotes.</span><span class="sxs-lookup"><span data-stu-id="71aa3-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="71aa3-108">Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como a coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="71aa3-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="71aa3-109">Determinadas tarefas podem ser computacionalmente exigentes, mas exigem acesso em tempo real ao fluxo de dados, como o reconhecimento de gestos com vários traços.</span><span class="sxs-lookup"><span data-stu-id="71aa3-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="71aa3-110">Para atender a essas necessidades, as APIs StylusInput fornecem um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus** , cada um em execução em seu próprio thread.</span><span class="sxs-lookup"><span data-stu-id="71aa3-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="71aa3-111">Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="71aa3-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="71aa3-112">As interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definem os mesmos métodos.</span><span class="sxs-lookup"><span data-stu-id="71aa3-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="71aa3-113">Esses métodos permitem que o objeto [**RealTimeStylus**](realtimestylus-class.md) passe os dados da caneta para cada plug-in, independentemente de ser um plug-in assíncrono ou síncrono.</span><span class="sxs-lookup"><span data-stu-id="71aa3-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="71aa3-114">As propriedades [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) permitem que cada plug-in assine dados específicos no fluxo de dados da caneta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="71aa3-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="71aa3-115">Um plug-in deve assinar apenas os dados necessários para executar sua tarefa, minimizando as demandas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="71aa3-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="71aa3-116">Para obter mais informações sobre Threading e a classe **RealTimeStylus** , consulte [considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="71aa3-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="71aa3-117">O objeto [**RealTimeStylus**](realtimestylus-class.md) usa objetos no namespace [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para passar os dados da caneta para seus plug-ins. O **RealTimeStylus** também captura exceções geradas por plug-ins. Quando o **RealTimeStylus** captura exceções, ele notifica os plug-ins chamando o método [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="71aa3-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="71aa3-118">Para obter mais informações sobre como usar dados de plug-in, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="71aa3-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="71aa3-119">Para obter mais informações sobre o tratamento de erros, consulte [considerações de tratamento de erros para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e a seção dados de erro de dados de plug-in e a classe RealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="71aa3-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="71aa3-120">Pelo menos um plug-in deve ser anexado ao objeto [**RealTimeStylus**](realtimestylus-class.md) antes que o objeto **RealTimeStylus** possa ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="71aa3-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="71aa3-121">Os tópicos a seguir descrevem algumas categorias comuns de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="71aa3-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="71aa3-122">Plug-ins de coleta de tinta</span><span class="sxs-lookup"><span data-stu-id="71aa3-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="71aa3-123">Plug-ins de processamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="71aa3-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="71aa3-124">Plug-ins do Recognizer</span><span class="sxs-lookup"><span data-stu-id="71aa3-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="71aa3-125">Considerações especiais</span><span class="sxs-lookup"><span data-stu-id="71aa3-125">Special Considerations</span></span>

<span data-ttu-id="71aa3-126">Devido à natureza complexa do objeto [**RealTimeStylus**](realtimestylus-class.md) , você deve anotar o seguinte.</span><span class="sxs-lookup"><span data-stu-id="71aa3-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="71aa3-127">O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção se um plug-in modifica a coleção de plug-ins à qual está anexada.</span><span class="sxs-lookup"><span data-stu-id="71aa3-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="71aa3-128">Isso ocorre apenas quando o plug-in faz isso enquanto está sendo chamado pelo objeto **RealTimeStylus** como um membro dessa coleção.</span><span class="sxs-lookup"><span data-stu-id="71aa3-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="71aa3-129">O exemplo C a seguir \# é um código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gere uma exceção.</span><span class="sxs-lookup"><span data-stu-id="71aa3-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="71aa3-130">O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção se um plug-in chama o método [Dispose](/previous-versions/ms825891(v=msdn.10)) do objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="71aa3-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="71aa3-131">Isso ocorre apenas quando o plug-in faz isso enquanto está sendo chamado pelo objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="71aa3-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="71aa3-132">O exemplo C a seguir \# é um código que faz com que o objeto [**RealTimeStylus**](realtimestylus-class.md) gere uma exceção.</span><span class="sxs-lookup"><span data-stu-id="71aa3-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="71aa3-133">As coleções de plug-ins podem ser modificadas enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; no entanto, isso pode tornar o comportamento do seu aplicativo mais difícil de prever.</span><span class="sxs-lookup"><span data-stu-id="71aa3-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="71aa3-134">Quando um plug-in é adicionado enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) ou [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) do plug-in.</span><span class="sxs-lookup"><span data-stu-id="71aa3-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="71aa3-135">Quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ou [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) do plug-in.</span><span class="sxs-lookup"><span data-stu-id="71aa3-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="71aa3-136">Isso permite que o plug-in Mantenha seu estado adequado sem precisar verificar a propriedade [Enabled](/previous-versions/ms824832(v=msdn.10)) do objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="71aa3-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="71aa3-137">Quando um plug-in é adicionado enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, os dados de plug-in que o plug-in recebe podem não conter informações suficientes para estabelecer adequadamente o contexto dos dados iniciais.</span><span class="sxs-lookup"><span data-stu-id="71aa3-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="71aa3-138">Por exemplo, o plug-in recém-adicionado pode começar a receber dados de pacote de uma caneta que está em um traço intermediário.</span><span class="sxs-lookup"><span data-stu-id="71aa3-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="71aa3-139">Da mesma forma, quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, os dados de plug-in que o plug-in recebeu podem não ser suficientes para concluir o processamento dos dados.</span><span class="sxs-lookup"><span data-stu-id="71aa3-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="71aa3-140">Para a estabilidade geral, redefina o estado interno de um plug-in quando o método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) for chamado.</span><span class="sxs-lookup"><span data-stu-id="71aa3-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="71aa3-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71aa3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71aa3-142">O modelo RealTimeStylus em cascata</span><span class="sxs-lookup"><span data-stu-id="71aa3-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="71aa3-143">Considerações de tratamento de erro para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="71aa3-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="71aa3-144">Dados de plug-in e a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="71aa3-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="71aa3-145">Considerações de threading para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="71aa3-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
