---
description: Usando GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Usando GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506017"
---
# <a name="using-graphedit"></a><span data-ttu-id="30e54-103">Usando GraphEdit</span><span class="sxs-lookup"><span data-stu-id="30e54-103">Using GraphEdit</span></span>

<span data-ttu-id="30e54-104">O GraphEdit está disponível no Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="30e54-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="30e54-105">O nome do aplicativo GraphEdit é "graphedt.exe".</span><span class="sxs-lookup"><span data-stu-id="30e54-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="30e54-106">Depois de instalar o SDK, "graphedt.exe" está localizado no seguinte diretório: \[ arquivos de programas \] \\ Microsoft SDKs \\ Windows \\ \[ versão \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="30e54-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="30e54-107">Antes de executar o GraphEdit, use o utilitário regsvr32 para registrar as seguintes DLLs, que estão localizadas no mesmo diretório:</span><span class="sxs-lookup"><span data-stu-id="30e54-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="30e54-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="30e54-108">proppage.dll</span></span>
-   <span data-ttu-id="30e54-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="30e54-109">evrprop.dll</span></span>

<span data-ttu-id="30e54-110">Essas DLLs permitem que o GraphEdit exiba páginas de propriedades para alguns dos filtros internos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="30e54-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="30e54-111">Criar um grafo de reprodução de arquivo</span><span class="sxs-lookup"><span data-stu-id="30e54-111">Build a File Playback Graph</span></span>

<span data-ttu-id="30e54-112">GraphEdit pode criar um grafo de filtro para reprodução de arquivos.</span><span class="sxs-lookup"><span data-stu-id="30e54-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="30e54-113">Esse recurso é equivalente a chamar o método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30e54-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="30e54-114">No menu **arquivo** , clique em **renderizar arquivo de mídia**.</span><span class="sxs-lookup"><span data-stu-id="30e54-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="30e54-115">GraphEdit exibe uma caixa de diálogo **Abrir arquivo** .</span><span class="sxs-lookup"><span data-stu-id="30e54-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="30e54-116">Selecione um arquivo multimídia e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="30e54-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="30e54-117">O GraphEdit cria um grafo de filtro para reproduzir o arquivo que você selecionou.</span><span class="sxs-lookup"><span data-stu-id="30e54-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="30e54-118">Você também pode renderizar um arquivo de mídia localizado em uma URL.</span><span class="sxs-lookup"><span data-stu-id="30e54-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="30e54-119">No menu **arquivo** , clique em **renderizar URL**.</span><span class="sxs-lookup"><span data-stu-id="30e54-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="30e54-120">GraphEdit exibe uma caixa de diálogo na qual digitar a URL.</span><span class="sxs-lookup"><span data-stu-id="30e54-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="30e54-121">Criar um gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="30e54-121">Build a Filter Graph</span></span>

<span data-ttu-id="30e54-122">O GraphEdit pode criar um grafo de filtro personalizado, usando qualquer um dos filtros registrados no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="30e54-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="30e54-123">No menu **gráfico** , clique em **Inserir filtros**.</span><span class="sxs-lookup"><span data-stu-id="30e54-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="30e54-124">Uma caixa de diálogo é exibida com uma lista dos filtros em seu sistema, organizadas por categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="30e54-125">GraphEdit compila essa lista a partir de informações no registro.</span><span class="sxs-lookup"><span data-stu-id="30e54-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="30e54-126">A ilustração a seguir mostra a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="30e54-126">The following illustration shows the dialog box.</span></span>

![quais filtros você deseja inserir?](images/gedit12.png)

<span data-ttu-id="30e54-128">Para adicionar um filtro ao grafo, selecione o nome do filtro, clique no botão **Inserir filtros** ou clique duas vezes no nome do filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="30e54-129">Depois de adicionar os filtros, você pode conectar dois filtros arrastando o mouse do pino de saída de um filtro para o PIN de entrada de outro filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="30e54-130">Se os Pins aceitarem a conexão, o GraphEdit desenhará uma seta conectando-as.</span><span class="sxs-lookup"><span data-stu-id="30e54-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![Conectando dois filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="30e54-132">Executar o grafo</span><span class="sxs-lookup"><span data-stu-id="30e54-132">Run the Graph</span></span>

<span data-ttu-id="30e54-133">Depois de criar um grafo de filtro na edição de grafo, você pode executar o grafo para ver se ele funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="30e54-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="30e54-134">O menu **gráfico** contém os comandos de menu **reproduzir**, **Pausar** e **parar**.</span><span class="sxs-lookup"><span data-stu-id="30e54-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="30e54-135">Esses comandos são invocados para os métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**executados**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pausar**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)e [**parar**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="30e54-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="30e54-136">A barra de ferramentas GraphEdit também tem botões para esses comandos:</span><span class="sxs-lookup"><span data-stu-id="30e54-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![botões pausar, reproduzir e parar](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="30e54-138">O comando GraphEdit **Stop** primeiro pausa o grafo e procura o tempo zero (supondo que o grafo seja pesquisável).</span><span class="sxs-lookup"><span data-stu-id="30e54-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="30e54-139">Para a reprodução de arquivo, essa ação redefine a janela de vídeo para o primeiro quadro.</span><span class="sxs-lookup"><span data-stu-id="30e54-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="30e54-140">Em seguida, GraphEdit chama [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="30e54-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="30e54-141">Se o grafo for pesquisável, você poderá Seek-lo arrastando a barra deslizante que aparece abaixo da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="30e54-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="30e54-142">Arrastar a barra deslizante invoca o método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="30e54-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="30e54-143">Exibir páginas de propriedades</span><span class="sxs-lookup"><span data-stu-id="30e54-143">View Property Pages</span></span>

<span data-ttu-id="30e54-144">Alguns filtros oferecem suporte a páginas de propriedades personalizadas, que fornecem uma interface do usuário para definir propriedades no filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="30e54-145">Para exibir a página de propriedades de um filtro no GraphEdit, clique com o botão direito do mouse no filtro e selecione **Propriedades** na janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="30e54-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="30e54-146">GraphEdit exibe uma página de propriedades que contém as folhas de propriedades definidas pelo filtro (se houver).</span><span class="sxs-lookup"><span data-stu-id="30e54-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="30e54-147">Além disso, o GraphEdit inclui uma folha de propriedades para cada Pin no filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="30e54-148">As folhas de propriedades do PIN são definidas por GraphEdit, não pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="30e54-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="30e54-149">Se o PIN estiver conectado, a folha de propriedades do PIN exibirá o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="30e54-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="30e54-150">Caso contrário, ele listará os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="30e54-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="30e54-151">Para usar as páginas de propriedades internas do GraphEdit, você deve registrar proppage.dll.</span><span class="sxs-lookup"><span data-stu-id="30e54-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="30e54-152">Essa DLL está disponível no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="30e54-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="30e54-153">A DLL também contém páginas de propriedades adicionais para alguns filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="30e54-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="30e54-154">Essas páginas de propriedades são fornecidas apenas para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="30e54-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="30e54-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30e54-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e54-156">Simulando a criação de gráficos com o GraphEdit</span><span class="sxs-lookup"><span data-stu-id="30e54-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



