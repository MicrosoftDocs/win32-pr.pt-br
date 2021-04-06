---
description: Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826675"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="04f9b-103">DuckingCaptureSample</span><span class="sxs-lookup"><span data-stu-id="04f9b-103">DuckingCaptureSample</span></span>

<span data-ttu-id="04f9b-104">Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo.</span><span class="sxs-lookup"><span data-stu-id="04f9b-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="04f9b-105">Esse aplicativo implementa um cliente de chat que usa APIs de áudio de núcleo para ler dados de áudio de um dispositivo de comunicação e reproduzi-lo no dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="04f9b-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="04f9b-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="04f9b-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="04f9b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="04f9b-107">Description</span></span>](#description)
-   [<span data-ttu-id="04f9b-108">Requirements</span><span class="sxs-lookup"><span data-stu-id="04f9b-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="04f9b-109">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="04f9b-110">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="04f9b-111">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="04f9b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04f9b-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="04f9b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="04f9b-113">Description</span></span>

<span data-ttu-id="04f9b-114">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="04f9b-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="04f9b-115">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="04f9b-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="04f9b-116">[WASAPI](wasapi.md) para acessar o dispositivo de captura e processamento de comunicações, operações de gerenciamento de fluxo e manipulação de eventos de pato.</span><span class="sxs-lookup"><span data-stu-id="04f9b-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="04f9b-117">[APIs de onda](/previous-versions//ms713499(v=vs.85)) para acessar o dispositivo de comunicações e capturar a entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="04f9b-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f9b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04f9b-118">Requirements</span></span>



| <span data-ttu-id="04f9b-119">Produto</span><span class="sxs-lookup"><span data-stu-id="04f9b-119">Product</span></span>                                                        | <span data-ttu-id="04f9b-120">Versão</span><span class="sxs-lookup"><span data-stu-id="04f9b-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="04f9b-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="04f9b-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="04f9b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04f9b-122">Windows 7</span></span> |
| <span data-ttu-id="04f9b-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="04f9b-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="04f9b-124">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-124">Downloading the Sample</span></span>

<span data-ttu-id="04f9b-125">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="04f9b-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="04f9b-126">Local</span><span class="sxs-lookup"><span data-stu-id="04f9b-126">Location</span></span>    | <span data-ttu-id="04f9b-127">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="04f9b-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f9b-128">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="04f9b-128">Windows SDK</span></span> | <span data-ttu-id="04f9b-129">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ DuckingCaptureSample \\ ...</span><span class="sxs-lookup"><span data-stu-id="04f9b-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="04f9b-130">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-130">Building the Sample</span></span>

<span data-ttu-id="04f9b-131">Para criar o exemplo de DuckingCaptureSample, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="04f9b-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="04f9b-132">Abra o DuckingCaptureSample. sln no Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="04f9b-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="04f9b-133">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="04f9b-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="04f9b-134">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="04f9b-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="04f9b-135">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, DuckingCaptureSample. vcproj.</span><span class="sxs-lookup"><span data-stu-id="04f9b-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="04f9b-136">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04f9b-136">Running the Sample</span></span>

<span data-ttu-id="04f9b-137">Se você compilar o aplicativo com êxito, um arquivo executável, DuckingCaptureSample.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="04f9b-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="04f9b-138">Para executá-lo, selecione **Iniciar Depuração** ou **Iniciar sem Depurar** no menu **depurar** ou digite `DuckingCaptureSample` uma janela de comando.</span><span class="sxs-lookup"><span data-stu-id="04f9b-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="04f9b-139">O DuckingCaptureSample fornece ao usuário duas implementações para capturar áudio do dispositivo de console padrão: WASAPI e APIs de onda.</span><span class="sxs-lookup"><span data-stu-id="04f9b-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="04f9b-140">Para iniciar uma sessão de captura, selecione um modo e clique em **Iniciar** na interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04f9b-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="04f9b-141">Para encerrar a sessão, clique em **parar**.</span><span class="sxs-lookup"><span data-stu-id="04f9b-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="04f9b-142">Dependendo do dispositivo especificado pelo usuário (entrada ou saída), o aplicativo usa a API MMDevice para obter uma referência ao dispositivo de comunicação de captura ou de renderização padrão.</span><span class="sxs-lookup"><span data-stu-id="04f9b-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="04f9b-143">Depois que o usuário inicia uma sessão de bate-papo, o aplicativo executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="04f9b-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="04f9b-144">Cria e inicializa um cliente de áudio no modo controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="04f9b-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="04f9b-145">Associa o cliente ao identificador de evento que sinaliza que as amostras estão prontas para captura ou renderização.</span><span class="sxs-lookup"><span data-stu-id="04f9b-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="04f9b-146">Configura um cliente de captura e um cliente de renderização para o transporte.</span><span class="sxs-lookup"><span data-stu-id="04f9b-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="04f9b-147">Cria o thread de chat e inicia o mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="04f9b-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="04f9b-148">Para capturar dados de áudio, com cada passagem de processamento, o exemplo usa o cliente de captura para obter a quantidade total de dados capturados que estão disponíveis no buffer, ler dados do dispositivo de entrada padrão e liberar o pacote e disponibilizar o buffer para ler o próximo conjunto de dados capturados.</span><span class="sxs-lookup"><span data-stu-id="04f9b-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="04f9b-149">Para renderização, o aplicativo determina a quantidade de dados que são enfileirados para reprodução no buffer de ponto de extremidade de captura.</span><span class="sxs-lookup"><span data-stu-id="04f9b-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="04f9b-150">Portanto, ele grava no buffer e libera o buffer na preparação para o próximo passo de processamento até que todos os dados tenham sido gravados.</span><span class="sxs-lookup"><span data-stu-id="04f9b-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="04f9b-151">Para renderização, os quadros silenciosos são inscritos para impedir que o mecanismo de áudio seja reparado na inicialização.</span><span class="sxs-lookup"><span data-stu-id="04f9b-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="04f9b-152">DuckingCaptureSample também mostra como ocultar o fluxo de renderização do mixer de volume.</span><span class="sxs-lookup"><span data-stu-id="04f9b-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="04f9b-153">Para obter mais informações sobre o recurso de atenuação de fluxo, consulte [usando um dispositivo de comunicação](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="04f9b-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04f9b-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04f9b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04f9b-155">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="04f9b-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
