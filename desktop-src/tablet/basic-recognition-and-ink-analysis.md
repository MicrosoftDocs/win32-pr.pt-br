---
description: Este tópico apresenta as APIs de análise de tinta.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconhecimento básico e análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370511"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="73762-103">Reconhecimento básico e análise de tinta</span><span class="sxs-lookup"><span data-stu-id="73762-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="73762-104">Este tópico apresenta as APIs de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="73762-105">Reconhecimento simples</span><span class="sxs-lookup"><span data-stu-id="73762-105">Simple Recognition</span></span>

<span data-ttu-id="73762-106">A funcionalidade básica exposta pela API de análise de tinta é o acesso aos resultados de reconhecimento para uma determinada folha de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="73762-107">Isso é fácil e simples de fazer, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="73762-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="73762-108">Os resultados da operação de reconhecimento são simplesmente um valor de cadeia de caracteres que representa o valor reconhecido da tinta manuscrita.</span><span class="sxs-lookup"><span data-stu-id="73762-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="73762-109">A API de análise de tinta expõe muito mais funcionalidade de reconhecimento do que apenas a cadeia de caracteres reconhecida, mas essa é a operação mais comum.</span><span class="sxs-lookup"><span data-stu-id="73762-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="73762-110">Reconhecimento incremental</span><span class="sxs-lookup"><span data-stu-id="73762-110">Incremental Recognition</span></span>

<span data-ttu-id="73762-111">O processo de reconhecimento leva tempo para ser concluído, bloqueando o acesso ao aplicativo bloqueando o thread da interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73762-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="73762-112">Portanto, ele pode ser dispendioso e frustrante ao usuário final para aguardar de forma síncrona os resultados.</span><span class="sxs-lookup"><span data-stu-id="73762-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="73762-113">Muitos aplicativos de Tablet PC exigem o reconhecimento de mais de algumas linhas de tinta, e uma abordagem incremental para reconhecer traços em um thread em segundo plano é a estratégia ideal.</span><span class="sxs-lookup"><span data-stu-id="73762-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="73762-114">A vantagem de uma abordagem incremental em vez de uma operação em massa é que ela permite que o reconhecimento dos traços aconteça durante um período de tempo, distribuindo o trabalho no thread em segundo plano em vez de sincronicamente no thread em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="73762-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="73762-115">Para dar suporte à análise incremental, o objeto [**InkAnalyzer**](inkanalyzer.md) tem um método [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , que manipula a criação e o gerenciamento de um thread em segundo plano para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73762-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="73762-116">O **InkAnalyzer** também cuida automaticamente do gerenciamento do que precisa ser reconhecido e do que já foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="73762-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="73762-117">Portanto, há dois mecanismos para obter os resultados de reconhecimento:</span><span class="sxs-lookup"><span data-stu-id="73762-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="73762-118">O método [**Analyze**](iinkanalyzer-analyze.md) (análise síncrona), que funciona melhor para:</span><span class="sxs-lookup"><span data-stu-id="73762-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="73762-119">Pequenas quantidades de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="73762-120">Quando os resultados são necessários antes de prosseguir para a próxima operação no aplicativo, como ao exibir uma interface do usuário de correção.</span><span class="sxs-lookup"><span data-stu-id="73762-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="73762-121">O método [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (análise assíncrona), que funciona melhor para:</span><span class="sxs-lookup"><span data-stu-id="73762-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="73762-122">Qualquer quantidade de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="73762-123">Quando utilizado com um temporizador Pulsing aproximadamente a cada 600 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="73762-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="73762-124">600 milissegundos é a recomendação atual, mas esse tempo está sujeito a alterações de outros testes pendentes.</span><span class="sxs-lookup"><span data-stu-id="73762-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="73762-125">Para usar a operação [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , o objeto [**InkCollector**](inkcollector-class.md) (ou objetos semelhantes ou controles como o [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)ou [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) no Windows Presentation Foundation) gerencia a coleta e a renderização dos traços de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="73762-126">Se o **InkCollector** for emparelhado com as APIs de análise de tinta, os aplicativos poderão manter os resultados de reconhecimento atualizados ao informar o [**InkAnalyzer**](inkanalyzer.md) sobre cada novo traço adicionado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73762-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="73762-127">Isso permite que o **InkAnalyzer** reconheça os traços incrementalmente e em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="73762-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="73762-128">Para realizar uma análise de segundo plano incremental, os aplicativos precisam implementar três etapas (mostradas para código gerenciado):</span><span class="sxs-lookup"><span data-stu-id="73762-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="73762-129">Adicione o traço ao [**InkAnalyzer**](inkanalyzer.md) sempre que o evento de [**traço**](inkoverlay-stroke.md) do objeto [**InkOverlay**](inkoverlay-class.md) for gerado:</span><span class="sxs-lookup"><span data-stu-id="73762-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="73762-130">Invocar as operações [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) em um intervalo definido.</span><span class="sxs-lookup"><span data-stu-id="73762-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="73762-131">Observação os aplicativos não devem simplesmente invocar a operação de análise em segundo plano após cada novo traço.</span><span class="sxs-lookup"><span data-stu-id="73762-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="73762-132">Isso irá falhar (retornando um valor de **false**) se uma operação em segundo plano já estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="73762-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="73762-133">O motivo para esse comportamento é limitar o número de threads em segundo plano e as operações de reconciliação necessárias.</span><span class="sxs-lookup"><span data-stu-id="73762-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="73762-134">Ouça o evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (código gerenciado) ou o evento de [**resultados**](-ianalysisevents-results.md) (código C++) para determinar quando o processo em segundo plano foi concluído:</span><span class="sxs-lookup"><span data-stu-id="73762-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="73762-135">Agora que o processamento da tinta está sendo feito em um thread em segundo plano, o aplicativo tem a capacidade de aceitar alterações na tinta enquanto a operação em segundo plano está funcionando.</span><span class="sxs-lookup"><span data-stu-id="73762-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="73762-136">Se usarmos um thread síncrono, isso não é possível.</span><span class="sxs-lookup"><span data-stu-id="73762-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="73762-137">O trabalho é executado no thread da interface do usuário, bloqueando a capacidade de fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="73762-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="73762-138">As alterações incluem adicionar mais tinta ao documento, excluir tinta ou transformar o local ou a aparência da tinta existente.</span><span class="sxs-lookup"><span data-stu-id="73762-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="73762-139">As alterações que ocorrem durante a operação em segundo plano podem, de fato, invalidar os resultados.</span><span class="sxs-lookup"><span data-stu-id="73762-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="73762-140">Por exemplo, excluir um traço de uma palavra altera o valor de reconhecimento dessa palavra.</span><span class="sxs-lookup"><span data-stu-id="73762-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="73762-141">A API [**InkAnalyzer**](inkanalyzer.md) tem um processo de reconciliação interno que determina automaticamente quais partes da operação em segundo plano se tornam inválidas como resultado da alteração da tinta durante a análise.</span><span class="sxs-lookup"><span data-stu-id="73762-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="73762-142">O processo de reconciliação automática é realizado devido a três fatores:</span><span class="sxs-lookup"><span data-stu-id="73762-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="73762-143">A propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="73762-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="73762-144">Cada vez que o aplicativo adiciona (método [**addstroke**](iinkanalyzer-addstroke.md) ) ou Remove (método [**RemoveStroke**](iinkanalyzer-removestroke.md) ) um traço de ou para o [**InkAnalyzer**](inkanalyzer.md), o local físico do traço é capturado e na próxima vez que uma operação de análise é invocada, a **InkAnalyzer** garante que Stroke ou a área ocupada por esse traço seja analisada.</span><span class="sxs-lookup"><span data-stu-id="73762-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="73762-145">Sempre que o aplicativo modifica a tinta existente, altera o local ou altera outros atributos de desenho da tinta, o local da alteração (os limites da tinta) pode ser adicionado à propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) do [**InkAnalyzer**](inkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="73762-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="73762-146">Isso garante que, na próxima vez que o aplicativo iniciar a operação de análise, essas áreas serão verificadas quanto aos resultados corretos.</span><span class="sxs-lookup"><span data-stu-id="73762-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="73762-147">Assim, a propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) mantém o controle, entre as execuções de análise, de quais áreas do documento e, por sua vez, os traços precisam ser verificados quanto aos resultados corretos de análise e reconhecimento de tinta.</span><span class="sxs-lookup"><span data-stu-id="73762-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="73762-148">Análise limitada.</span><span class="sxs-lookup"><span data-stu-id="73762-148">Limited analysis.</span></span>

    -   <span data-ttu-id="73762-149">Cada vez que o aplicativo invoca a operação de análise, a propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica quais traços precisam ser analisados.</span><span class="sxs-lookup"><span data-stu-id="73762-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="73762-150">Isso permite que a operação de análise limite a operação somente às regiões sujas e ignore todas as outras regiões, otimizando a quantidade de tempo gasto na análise da tinta novamente.</span><span class="sxs-lookup"><span data-stu-id="73762-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="73762-151">O [**InkAnalyzer**](inkanalyzer.md) não ignora completamente todas as outras regiões na página, mas, em vez disso, pode examinar as áreas vizinhas para determinar se as alterações feitas na região suja afetam essas regiões vizinhas.</span><span class="sxs-lookup"><span data-stu-id="73762-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="73762-152">Por exemplo, o analisador classifica "is", no exemplo de tinta a seguir, como um único tipo de **InkWord** da classe [**ContextNode**](icontextnode.md) :</span><span class="sxs-lookup"><span data-stu-id="73762-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

![manuscrito "is"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="73762-154">A exclusão de "s" resulta em uma região suja (marcada com uma caixa vermelha).</span><span class="sxs-lookup"><span data-stu-id="73762-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

![manuscrito "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="73762-156">Após a análise, o analisador altera a classificação para "I" para um tipo **InkDrawing** , embora esteja fora da região suja, porque sem o traço "s" de suporte, o analisador de tinta tem uma chance de 50/50 da tinta sendo classificada como um desenho ou uma palavra.</span><span class="sxs-lookup"><span data-stu-id="73762-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="73762-157">Estado armazenado internamente em cache.</span><span class="sxs-lookup"><span data-stu-id="73762-157">Internally cached state.</span></span>

    -   <span data-ttu-id="73762-158">Quando um aplicativo invoca uma operação de análise em segundo plano, o [**InkAnalyzer**](inkanalyzer.md) armazena em cache um instantâneo dos dados removidos.</span><span class="sxs-lookup"><span data-stu-id="73762-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="73762-159">Ao fazer um instantâneo, o **InkAnalyzer** pode trabalhar na análise dos dados independentemente dos dados que estão sendo usados pelo aplicativo ou usar o instantâneo como ponto de comparação para determinar quais alterações foram feitas pelo aplicativo durante a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="73762-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="73762-160">Armazenar em cache o estado e comparar as alterações é melhor do que manter uma lista de todas as alterações ocorridas por um motivo principal: proxy de dados.</span><span class="sxs-lookup"><span data-stu-id="73762-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="73762-161">Este é um cenário avançado descrito mais adiante neste documento, mas ele envolve o aplicativo que atualiza o [**InkAnalyzer**](inkanalyzer.md) com apenas a tinta atual e os dados que não são de tinta antes da operação de análise invocada e antes do processamento dos resultados de uma operação de análise.</span><span class="sxs-lookup"><span data-stu-id="73762-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="73762-162">Análise de tinta simples</span><span class="sxs-lookup"><span data-stu-id="73762-162">Simple Ink Analysis</span></span>

<span data-ttu-id="73762-163">Os dois cenários anteriores (reconhecimento simples e reconhecimento incremental) descrevem como acessar os valores de reconhecimento, mas não mencionam como acessar os resultados da análise de tinta ou da classificação.</span><span class="sxs-lookup"><span data-stu-id="73762-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="73762-164">A configuração padrão do [**InkAnalyzer**](inkanalyzer.md), executa algoritmos de análise de tinta e algoritmos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="73762-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="73762-165">Essa configuração gera os resultados mais precisos, pois as duas tecnologias funcionam em conjunto para aumentar a precisão.</span><span class="sxs-lookup"><span data-stu-id="73762-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="73762-166">Ou seja, os mecanismos de análise de tinta ajudam a separar o desenho da gravação angular de escrita e de Normalize em um plano horizontal, que é o plano de entrada ideal para os mecanismos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="73762-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="73762-167">Para acessar os resultados da análise de tinta, seu aplicativo usa os métodos [**Analyze**](iinkanalyzer-analyze.md) ou [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exatamente conforme descrito nos dois cenários de reconhecimento anteriores.</span><span class="sxs-lookup"><span data-stu-id="73762-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="73762-168">Nada muda porque os algoritmos de reconhecimento e de análise de tinta já estão sendo executados quando esses métodos são chamados.</span><span class="sxs-lookup"><span data-stu-id="73762-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="73762-169">No entanto, o acesso aos resultados é mais complicado do que ler o valor de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="73762-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="73762-170">Por exemplo, o exemplo de código a seguir mostra o agrupamento e os locais de todos os segmentos **InkWord** e segmentos **InkDrawing** renderizando um retângulo ao lado do grupo de traços que compõem a classificação.</span><span class="sxs-lookup"><span data-stu-id="73762-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="73762-171">Este exemplo simplesmente usa o evento de **pintura** do formulário para renderizar retângulos coloridos em volta das palavras ou dos desenhos.</span><span class="sxs-lookup"><span data-stu-id="73762-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="73762-172">O método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) retornará uma coleção de objetos que existe somente se a operação de análise tiver sido executada e os resultados contiverem classificações com o tipo [**ContextNode**](icontextnode.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="73762-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="73762-173">Se nenhum **ContextNode** do tipo desejado existir no documento, as etapas para desenhar os retângulos serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="73762-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="73762-174">Cada objeto retornado do método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) terá propriedades relacionadas a esse tipo de classificação.</span><span class="sxs-lookup"><span data-stu-id="73762-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="73762-175">Por exemplo, o **InkWordNode** faz referência a todos os traços que compõem uma única palavra no documento e referenciam a cadeia de caracteres reconhecida para essa palavra.</span><span class="sxs-lookup"><span data-stu-id="73762-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="73762-176">O **InkDrawingNode** faz referência a todos os traços que compõem o desenho único no documento e referenciam o nome da forma para esse desenho.</span><span class="sxs-lookup"><span data-stu-id="73762-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="73762-177">O método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) é muito semelhante ao método [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) que retornou coleções de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de tipos de escrita ou desenho.</span><span class="sxs-lookup"><span data-stu-id="73762-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="73762-178">Para colocar o exemplo de código anterior em perspectiva, considere o seguinte exemplo de tinta:</span><span class="sxs-lookup"><span data-stu-id="73762-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![exemplo de tinta "esta é uma certa tinta".](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="73762-181">Se você chamar o método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e passar o campo estático para **InkWord**, o analisador retornará uma coleção de quatro objetos **InkWordNode** :</span><span class="sxs-lookup"><span data-stu-id="73762-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![saída do analisador, "esta é uma certa tinta"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="73762-183">Se você chamar o método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e passar o campo estático para **InkDrawing**, o analisador retornará uma coleção de um objeto **InkDrawingNode** :</span><span class="sxs-lookup"><span data-stu-id="73762-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![imagem mostrando "oval", o resultado do analisador de inkdrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="73762-185">Após o acionamento do evento de **pintura** , o código de exemplo renderiza retângulos em volta de cada um dos objetos:</span><span class="sxs-lookup"><span data-stu-id="73762-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![desenho original com retângulos renderizados em volta do objeto e das palavras](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="73762-187">Este exemplo só toca no método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , mas como os mecanismos de análise de tinta podem detectar um conjunto mais rico de tipos de tinta, o método também corresponde a todos os tipos de nós detectáveis pelos mecanismos de análise de tinta (como linhas, parágrafos e outras estruturas).</span><span class="sxs-lookup"><span data-stu-id="73762-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="73762-188">Usando a análise de tinta com o ponto de apagamento</span><span class="sxs-lookup"><span data-stu-id="73762-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="73762-189">Seu aplicativo precisa fazer ajustes no modo como atualiza os traços ao executar o apagamento de ponto para garantir um bom desempenho.</span><span class="sxs-lookup"><span data-stu-id="73762-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="73762-190">Em primeiro lugar, na camada de aplicativo, substitua o ponto da caneta do traço existente pelo ponto da caneta do novo traço e, em seguida, chame [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) nesse traço e atualize a região suja com os limites do traço.</span><span class="sxs-lookup"><span data-stu-id="73762-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="73762-191">Isso fará com que o [**InkAnalyzer**](inkanalyzer.md) busque os dados de traço atualizados quando a próxima rodada de análise em segundo plano for iniciada.</span><span class="sxs-lookup"><span data-stu-id="73762-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="73762-192">Essa técnica é demonstrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="73762-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="73762-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73762-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73762-194">Visão geral da análise de tinta</span><span class="sxs-lookup"><span data-stu-id="73762-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="73762-195">Uso da API de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="73762-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
