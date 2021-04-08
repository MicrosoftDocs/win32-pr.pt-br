---
description: Exemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Exemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087708"
---
# <a name="dvapp-sample"></a><span data-ttu-id="13f28-103">Exemplo de DVApp</span><span class="sxs-lookup"><span data-stu-id="13f28-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="13f28-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="13f28-104">Description</span></span>

<span data-ttu-id="13f28-105">Aplicativo de captura de vídeo digital (DV).</span><span class="sxs-lookup"><span data-stu-id="13f28-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="13f28-106">Este exemplo demonstra como criar vários tipos de grafos de filtro para controlar camcorders DV.</span><span class="sxs-lookup"><span data-stu-id="13f28-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="13f28-107">Ele também mostra como executar a captura, a visualização, a transmissão e o controle de dispositivo com uma camcorder DV.</span><span class="sxs-lookup"><span data-stu-id="13f28-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="13f28-108">Uso</span><span class="sxs-lookup"><span data-stu-id="13f28-108">Usage</span></span>

<span data-ttu-id="13f28-109">O aplicativo DVApp dá suporte aos seguintes modos:</span><span class="sxs-lookup"><span data-stu-id="13f28-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="13f28-110">Visualização: renderiza o DV da camcorder em uma janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="13f28-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="13f28-111">DV para o arquivo do tipo-1: captura dados de DV da camcorder para um arquivo DV de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="13f28-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="13f28-112">Tipo-1 arquivo para DV: transmite dados de um arquivo DV tipo-1 para a camcorder.</span><span class="sxs-lookup"><span data-stu-id="13f28-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="13f28-113">DV para o arquivo do tipo-2: captura dados de DV da camcorder para um arquivo de DV tipo 2.</span><span class="sxs-lookup"><span data-stu-id="13f28-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="13f28-114">Tipo-2 arquivo para DV: transmite dados de um arquivo DV tipo-2 para a camcorder.</span><span class="sxs-lookup"><span data-stu-id="13f28-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="13f28-115">Os modos de captura e transmissão também executam a visualização.</span><span class="sxs-lookup"><span data-stu-id="13f28-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="13f28-116">Cada um desses modos também tem uma opção **sem visualização** , que desabilita a visualização.</span><span class="sxs-lookup"><span data-stu-id="13f28-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="13f28-117">A captura sem visualização é mais eficiente e pode reduzir o número de quadros descartados.</span><span class="sxs-lookup"><span data-stu-id="13f28-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="13f28-118">O aplicativo é iniciado no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="13f28-118">The application starts in preview mode.</span></span> <span data-ttu-id="13f28-119">Para selecionar outro modo, escolha um modo no menu **modo de gráfico** .</span><span class="sxs-lookup"><span data-stu-id="13f28-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="13f28-120">Para cada modo, o DVApp cria um grafo de filtro que dá suporte à funcionalidade desse modo.</span><span class="sxs-lookup"><span data-stu-id="13f28-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="13f28-121">Para salvar o grafo como um arquivo GraphEdit (. GRF), selecione **salvar grafo em arquivo** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="13f28-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="13f28-122">Saia do DVApp antes de abrir o arquivo em GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="13f28-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="13f28-123">Para capturar para um arquivo:</span><span class="sxs-lookup"><span data-stu-id="13f28-123">To capture to a file:</span></span>

1.  <span data-ttu-id="13f28-124">No menu **arquivo** , escolha **definir arquivo de saída** e insira um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="13f28-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="13f28-125">No menu **modo de gráfico** , selecione um *DV para* o modo de arquivo (tipo 1 ou 2, com ou sem visualização).</span><span class="sxs-lookup"><span data-stu-id="13f28-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="13f28-126">Clique em **gravar**.</span><span class="sxs-lookup"><span data-stu-id="13f28-126">Click **Record**.</span></span>
4.  <span data-ttu-id="13f28-127">Se a camcorder estiver no modo VTR, clique em **reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="13f28-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="13f28-128">Para parar a captura, clique em **parar**.</span><span class="sxs-lookup"><span data-stu-id="13f28-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="13f28-129">Para transmitir de um arquivo para a camcorder:</span><span class="sxs-lookup"><span data-stu-id="13f28-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="13f28-130">No menu **arquivo** , clique em **definir arquivo de entrada** e selecione um arquivo DV.</span><span class="sxs-lookup"><span data-stu-id="13f28-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="13f28-131">O arquivo deve corresponder ao modo selecionado (tipo 1 ou tipo 2).</span><span class="sxs-lookup"><span data-stu-id="13f28-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="13f28-132">No menu **modo de gráfico** , selecione um *arquivo para* o modo DV (tipo 1 ou tipo 2, com ou sem visualização).</span><span class="sxs-lookup"><span data-stu-id="13f28-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="13f28-133">Clique em **Reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="13f28-133">Click **Play**.</span></span>
4.  <span data-ttu-id="13f28-134">Para registrar os dados em fita, clique em **gravar**.</span><span class="sxs-lookup"><span data-stu-id="13f28-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="13f28-135">Para interromper a transmissão, clique em **parar**.</span><span class="sxs-lookup"><span data-stu-id="13f28-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="13f28-136">Se a camcorder estiver no modo VTR, o usuário poderá controlar o mecanismo de transporte por meio dos botões de estilo VCR do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13f28-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="13f28-137">Para buscar a fita, insira o código de padirecionamento de destino e clique no botão buscar.</span><span class="sxs-lookup"><span data-stu-id="13f28-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="13f28-138">Para limitar a quantidade de dados capturados pelo aplicativo, escolha **capturar tamanho** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="13f28-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="13f28-139">Para verificar o formato de fita (NTSC ou PAL), escolha **verificar fita** no menu de **Opções** .</span><span class="sxs-lookup"><span data-stu-id="13f28-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="13f28-140">Para alterar o tamanho da janela de visualização, escolha **alterar tamanho de decodificação** no menu **Opções** .</span><span class="sxs-lookup"><span data-stu-id="13f28-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="13f28-141">Notas de programação</span><span class="sxs-lookup"><span data-stu-id="13f28-141">Programming Notes</span></span>

<span data-ttu-id="13f28-142">A principal finalidade desse aplicativo é mostrar como criar vários grafos de transmissão e captura de DV.</span><span class="sxs-lookup"><span data-stu-id="13f28-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="13f28-143">Chegada e remoção de dispositivo</span><span class="sxs-lookup"><span data-stu-id="13f28-143">Device Arrival and Removal</span></span>

<span data-ttu-id="13f28-144">O aplicativo lida com a chegada e remoção de dispositivos usando duas técnicas diferentes.</span><span class="sxs-lookup"><span data-stu-id="13f28-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="13f28-145">Para a chegada do dispositivo, o loop de mensagem do aplicativo responde às mensagens do WM \_ DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="13f28-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="13f28-146">Para a remoção do dispositivo, o aplicativo responde aos eventos [**\_ \_ perdidos do dispositivo EC**](ec-device-lost.md) do Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="13f28-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="13f28-147">Qualquer abordagem funciona, embora o \_ evento de perda do dispositivo EC \_ dependa da existência do dispositivo no grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="13f28-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="13f28-148">O aplicativo lida apenas com um dispositivo de cada vez.</span><span class="sxs-lookup"><span data-stu-id="13f28-148">The application only handles one device at a time.</span></span> <span data-ttu-id="13f28-149">Se o dispositivo atual for removido, o aplicativo procurará outro dispositivo de vídeo digital no sistema.</span><span class="sxs-lookup"><span data-stu-id="13f28-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="13f28-150">Em algumas filmadoras de vídeo digital, o usuário deve desligar o dispositivo ao alterá-lo entre o modo de câmera e o modo VTR, que dispara uma mensagem de perda de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f28-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="13f28-151">O aplicativo responde habilitando ou desabilitando os comandos de menu apropriados.</span><span class="sxs-lookup"><span data-stu-id="13f28-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="13f28-152">No entanto, se o usuário alternar rapidamente entre os modos, a camcorder poderá não gerar uma mensagem de perda de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f28-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="13f28-153">Você pode forçar os menus a serem atualizados escolhendo o **modo de atualização** no menu de **Opções** .</span><span class="sxs-lookup"><span data-stu-id="13f28-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="13f28-154">Algumas camcorders DV podem alternar modos sem desligamento, mas enviar uma mensagem de dispositivo perdido somente quando eles mudarem para o modo VTR.</span><span class="sxs-lookup"><span data-stu-id="13f28-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="13f28-155">Controle de dispositivo</span><span class="sxs-lookup"><span data-stu-id="13f28-155">Device Control</span></span>

<span data-ttu-id="13f28-156">A funcionalidade do botão **reproduzir** e **gravar** depende do modo atual:</span><span class="sxs-lookup"><span data-stu-id="13f28-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="13f28-157">Visualização: o grafo de filtro é executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="13f28-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="13f28-158">O botão **reproduzir** inicia o transporte.</span><span class="sxs-lookup"><span data-stu-id="13f28-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="13f28-159">Capturar para arquivo: o botão **gravar** executa o grafo e o botão **reproduzir** inicia o transporte.</span><span class="sxs-lookup"><span data-stu-id="13f28-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="13f28-160">Transmitir para o dispositivo: o botão **reproduzir** executa o grafo e o botão **gravar** inicia o transporte.</span><span class="sxs-lookup"><span data-stu-id="13f28-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="13f28-161">O aplicativo de exemplo não executa captura precisa de quadro.</span><span class="sxs-lookup"><span data-stu-id="13f28-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="13f28-162">Em vários pontos, o aplicativo chama a função de **suspensão** para aguardar que o dispositivo responda.</span><span class="sxs-lookup"><span data-stu-id="13f28-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="13f28-163">Camcorders DV mais recentes enviam uma notificação quando o estado do dispositivo é alterado.</span><span class="sxs-lookup"><span data-stu-id="13f28-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="13f28-164">Dispositivos mais antigos podem não dar suporte à notificação; para os fins de um exemplo, chamar **Sleep** é uma solução mais simples.</span><span class="sxs-lookup"><span data-stu-id="13f28-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="13f28-165">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13f28-165">Downloading the Sample</span></span>

<span data-ttu-id="13f28-166">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="13f28-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="13f28-167">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ \\ multimídia DirectShow de \\ \\ captura \\ DVApp.</span><span class="sxs-lookup"><span data-stu-id="13f28-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13f28-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13f28-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f28-169">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="13f28-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="13f28-170">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="13f28-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="13f28-171">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="13f28-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



