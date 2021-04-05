---
description: Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646409"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="edf22-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="edf22-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="edf22-104">Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="edf22-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="edf22-105">Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="edf22-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="edf22-106">Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="edf22-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="edf22-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="edf22-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="edf22-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf22-108">Description</span></span>](#description)
-   [<span data-ttu-id="edf22-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="edf22-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="edf22-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="edf22-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="edf22-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="edf22-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edf22-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="edf22-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf22-114">Description</span></span>

<span data-ttu-id="edf22-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="edf22-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="edf22-116">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="edf22-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="edf22-117">WASAPI para operações de gerenciamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="edf22-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf22-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edf22-118">Requirements</span></span>



| <span data-ttu-id="edf22-119">Produto</span><span class="sxs-lookup"><span data-stu-id="edf22-119">Product</span></span>                                                        | <span data-ttu-id="edf22-120">Versão</span><span class="sxs-lookup"><span data-stu-id="edf22-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="edf22-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="edf22-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="edf22-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edf22-122">Windows 7</span></span> |
| <span data-ttu-id="edf22-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="edf22-123">Visual Studio</span></span>                                                  | <span data-ttu-id="edf22-124">2008</span><span class="sxs-lookup"><span data-stu-id="edf22-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="edf22-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-125">Downloading the Sample</span></span>

<span data-ttu-id="edf22-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="edf22-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="edf22-127">Local</span><span class="sxs-lookup"><span data-stu-id="edf22-127">Location</span></span>    | <span data-ttu-id="edf22-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="edf22-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf22-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="edf22-129">Windows SDK</span></span> | <span data-ttu-id="edf22-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="edf22-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="edf22-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-131">Building the Sample</span></span>

<span data-ttu-id="edf22-132">Para criar o exemplo de RenderSharedTimerDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="edf22-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="edf22-133">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="edf22-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="edf22-134">Execute o comando `start WASAPIRenderSharedTimerDriven.sln` no diretório RenderSharedTimerDriven para abrir o projeto WASAPIRenderSharedTimerDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="edf22-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="edf22-135">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="edf22-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="edf22-136">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="edf22-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="edf22-137">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="edf22-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="edf22-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="edf22-138">Running the Sample</span></span>

<span data-ttu-id="edf22-139">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderSharedTimerDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="edf22-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="edf22-140">Para executá-lo, digite `WASAPIRenderSharedTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="edf22-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="edf22-141">O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="edf22-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="edf22-142">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="edf22-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="edf22-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="edf22-143">Argument</span></span>        | <span data-ttu-id="edf22-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="edf22-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="edf22-145">-?</span><span class="sxs-lookup"><span data-stu-id="edf22-145">-?</span></span>              | <span data-ttu-id="edf22-146">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="edf22-146">Shows help.</span></span>                                                |
| <span data-ttu-id="edf22-147">-H</span><span class="sxs-lookup"><span data-stu-id="edf22-147">-h</span></span>              | <span data-ttu-id="edf22-148">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="edf22-148">Shows help.</span></span>                                                |
| <span data-ttu-id="edf22-149">-f</span><span class="sxs-lookup"><span data-stu-id="edf22-149">-f</span></span>              | <span data-ttu-id="edf22-150">Frequência de onda do seno em Hz.</span><span class="sxs-lookup"><span data-stu-id="edf22-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="edf22-151">-l</span><span class="sxs-lookup"><span data-stu-id="edf22-151">-l</span></span>              | <span data-ttu-id="edf22-152">Latência de renderização de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="edf22-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="edf22-153">-d</span><span class="sxs-lookup"><span data-stu-id="edf22-153">-d</span></span>              | <span data-ttu-id="edf22-154">Duração da onda do seno em segundos.</span><span class="sxs-lookup"><span data-stu-id="edf22-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="edf22-155">-M</span><span class="sxs-lookup"><span data-stu-id="edf22-155">-m</span></span>              | <span data-ttu-id="edf22-156">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="edf22-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="edf22-157">-console</span><span class="sxs-lookup"><span data-stu-id="edf22-157">-console</span></span>        | <span data-ttu-id="edf22-158">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="edf22-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="edf22-159">-comunicações</span><span class="sxs-lookup"><span data-stu-id="edf22-159">-communications</span></span> | <span data-ttu-id="edf22-160">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="edf22-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="edf22-161">-multimídia</span><span class="sxs-lookup"><span data-stu-id="edf22-161">-multimedia</span></span>     | <span data-ttu-id="edf22-162">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="edf22-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="edf22-163">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="edf22-163">-endpoint</span></span>       | <span data-ttu-id="edf22-164">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="edf22-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="edf22-165">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de renderização.</span><span class="sxs-lookup"><span data-stu-id="edf22-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="edf22-166">Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda de seno a 440 Hz por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="edf22-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="edf22-167">Esses valores podem ser modificados especificando-se os valores de opção-f e-d.</span><span class="sxs-lookup"><span data-stu-id="edf22-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="edf22-168">RenderSharedTimerDriven demonstra o buffer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="edf22-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="edf22-169">Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos).</span><span class="sxs-lookup"><span data-stu-id="edf22-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="edf22-170">Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="edf22-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="edf22-171">Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados a serem renderizados para que os dados não estourem o buffer.</span><span class="sxs-lookup"><span data-stu-id="edf22-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="edf22-172">Os dados de áudio a serem reproduzidos no dispositivo especificado podem ser processados habilitando o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="edf22-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="edf22-173">Esse modo é demonstrado no exemplo de [RenderSharedEventDriven](rendersharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="edf22-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="edf22-174">Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="edf22-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edf22-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edf22-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf22-176">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="edf22-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



