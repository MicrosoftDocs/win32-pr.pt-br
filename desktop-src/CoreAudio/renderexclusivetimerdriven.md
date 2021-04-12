---
description: Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário. Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457065"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="45aa8-104">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="45aa8-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="45aa8-105">Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="45aa8-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="45aa8-106">Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="45aa8-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="45aa8-107">Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="45aa8-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="45aa8-108">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="45aa8-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="45aa8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="45aa8-109">Description</span></span>](#description)
-   [<span data-ttu-id="45aa8-110">Requirements</span><span class="sxs-lookup"><span data-stu-id="45aa8-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="45aa8-111">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="45aa8-112">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="45aa8-113">Exibir os arquivos de exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="45aa8-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45aa8-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="45aa8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="45aa8-115">Description</span></span>

<span data-ttu-id="45aa8-116">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="45aa8-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="45aa8-117">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="45aa8-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="45aa8-118">WASAPI para operações de gerenciamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="45aa8-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="45aa8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45aa8-119">Requirements</span></span>



| <span data-ttu-id="45aa8-120">Produto</span><span class="sxs-lookup"><span data-stu-id="45aa8-120">Product</span></span>                                                        | <span data-ttu-id="45aa8-121">Versão</span><span class="sxs-lookup"><span data-stu-id="45aa8-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="45aa8-122">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="45aa8-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="45aa8-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45aa8-123">Windows 7</span></span> |
| <span data-ttu-id="45aa8-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45aa8-124">Visual Studio</span></span>                                                  | <span data-ttu-id="45aa8-125">2008</span><span class="sxs-lookup"><span data-stu-id="45aa8-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="45aa8-126">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-126">Downloading the Sample</span></span>

<span data-ttu-id="45aa8-127">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="45aa8-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="45aa8-128">Local</span><span class="sxs-lookup"><span data-stu-id="45aa8-128">Location</span></span>    | <span data-ttu-id="45aa8-129">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="45aa8-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45aa8-130">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="45aa8-130">Windows SDK</span></span> | <span data-ttu-id="45aa8-131">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderExclusiveTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="45aa8-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="45aa8-132">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-132">Building the Sample</span></span>

<span data-ttu-id="45aa8-133">Para criar o exemplo de RenderExclusiveTimerDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="45aa8-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="45aa8-134">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="45aa8-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="45aa8-135">Execute o comando `start WASAPIRenderExclusiveTimerDriven.sln` no diretório RenderExclusiveTimerDriven para abrir o projeto WASAPIRenderExclusiveTimerDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="45aa8-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="45aa8-136">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="45aa8-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="45aa8-137">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="45aa8-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="45aa8-138">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderExclusiveTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="45aa8-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="45aa8-139">Exibir os arquivos de exemplo</span><span class="sxs-lookup"><span data-stu-id="45aa8-139">View the Sample Files</span></span>

<span data-ttu-id="45aa8-140">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderExclusiveTimerDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="45aa8-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="45aa8-141">Para executá-lo, digite `WASAPIRenderExclusiveTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="45aa8-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="45aa8-142">O exemplo a seguir mostra como executar o exemplo por uma duração de reprodução especificando no dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="45aa8-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="45aa8-143">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="45aa8-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="45aa8-144">Argumento</span><span class="sxs-lookup"><span data-stu-id="45aa8-144">Argument</span></span>        | <span data-ttu-id="45aa8-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="45aa8-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="45aa8-146">-?</span><span class="sxs-lookup"><span data-stu-id="45aa8-146">-?</span></span>              | <span data-ttu-id="45aa8-147">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="45aa8-147">Shows help.</span></span>                                                |
| <span data-ttu-id="45aa8-148">-H</span><span class="sxs-lookup"><span data-stu-id="45aa8-148">-h</span></span>              | <span data-ttu-id="45aa8-149">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="45aa8-149">Shows help.</span></span>                                                |
| <span data-ttu-id="45aa8-150">-f</span><span class="sxs-lookup"><span data-stu-id="45aa8-150">-f</span></span>              | <span data-ttu-id="45aa8-151">Frequência de onda do seno em Hz.</span><span class="sxs-lookup"><span data-stu-id="45aa8-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="45aa8-152">-l</span><span class="sxs-lookup"><span data-stu-id="45aa8-152">-l</span></span>              | <span data-ttu-id="45aa8-153">Latência de renderização de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="45aa8-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="45aa8-154">-d</span><span class="sxs-lookup"><span data-stu-id="45aa8-154">-d</span></span>              | <span data-ttu-id="45aa8-155">Duração da onda do seno em segundos.</span><span class="sxs-lookup"><span data-stu-id="45aa8-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="45aa8-156">-M</span><span class="sxs-lookup"><span data-stu-id="45aa8-156">-m</span></span>              | <span data-ttu-id="45aa8-157">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="45aa8-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="45aa8-158">-console</span><span class="sxs-lookup"><span data-stu-id="45aa8-158">-console</span></span>        | <span data-ttu-id="45aa8-159">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="45aa8-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="45aa8-160">-comunicações</span><span class="sxs-lookup"><span data-stu-id="45aa8-160">-communications</span></span> | <span data-ttu-id="45aa8-161">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="45aa8-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="45aa8-162">-multimídia</span><span class="sxs-lookup"><span data-stu-id="45aa8-162">-multimedia</span></span>     | <span data-ttu-id="45aa8-163">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="45aa8-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="45aa8-164">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="45aa8-164">-endpoint</span></span>       | <span data-ttu-id="45aa8-165">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="45aa8-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="45aa8-166">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de renderização.</span><span class="sxs-lookup"><span data-stu-id="45aa8-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="45aa8-167">Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda de seno a 440 Hz por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="45aa8-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="45aa8-168">Esses valores podem ser modificados especificando-se os valores de opção-f e-d.</span><span class="sxs-lookup"><span data-stu-id="45aa8-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="45aa8-169">RenderExclusiveTimerDriven demonstra o buffer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="45aa8-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="45aa8-170">Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos).</span><span class="sxs-lookup"><span data-stu-id="45aa8-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="45aa8-171">Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="45aa8-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="45aa8-172">Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados a serem renderizados para que os dados não estourem o buffer.</span><span class="sxs-lookup"><span data-stu-id="45aa8-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="45aa8-173">Os dados de áudio a serem reproduzidos no dispositivo especificado podem ser processados habilitando o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="45aa8-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="45aa8-174">Esse modo é demonstrado no exemplo de RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="45aa8-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="45aa8-175">Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="45aa8-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45aa8-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45aa8-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45aa8-177">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="45aa8-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



