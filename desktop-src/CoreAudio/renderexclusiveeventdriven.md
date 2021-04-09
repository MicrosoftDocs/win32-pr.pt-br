---
description: Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010214"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="fefc5-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="fefc5-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="fefc5-104">Este aplicativo de exemplo usa as APIs de áudio principais para renderizar dados de áudio para um dispositivo de saída especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fefc5-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="fefc5-105">Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fefc5-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="fefc5-106">Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="fefc5-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="fefc5-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="fefc5-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fefc5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fefc5-108">Description</span></span>](#description)
-   [<span data-ttu-id="fefc5-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="fefc5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="fefc5-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="fefc5-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="fefc5-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="fefc5-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fefc5-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="fefc5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fefc5-114">Description</span></span>

<span data-ttu-id="fefc5-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="fefc5-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="fefc5-116">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="fefc5-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="fefc5-117">WASAPI para operações de gerenciamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fefc5-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="fefc5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fefc5-118">Requirements</span></span>



| <span data-ttu-id="fefc5-119">Produto</span><span class="sxs-lookup"><span data-stu-id="fefc5-119">Product</span></span>                                                        | <span data-ttu-id="fefc5-120">Versão</span><span class="sxs-lookup"><span data-stu-id="fefc5-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="fefc5-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="fefc5-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="fefc5-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fefc5-122">Windows 7</span></span> |
| <span data-ttu-id="fefc5-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fefc5-123">Visual Studio</span></span>                                                  | <span data-ttu-id="fefc5-124">2008</span><span class="sxs-lookup"><span data-stu-id="fefc5-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="fefc5-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-125">Downloading the Sample</span></span>

<span data-ttu-id="fefc5-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="fefc5-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="fefc5-127">Local</span><span class="sxs-lookup"><span data-stu-id="fefc5-127">Location</span></span>    | <span data-ttu-id="fefc5-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="fefc5-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fefc5-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="fefc5-129">Windows SDK</span></span> | <span data-ttu-id="fefc5-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderExclusiveEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="fefc5-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="fefc5-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-131">Building the Sample</span></span>

<span data-ttu-id="fefc5-132">Para criar o exemplo de RenderExclusiveEventDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fefc5-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="fefc5-133">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderExclusiveEventDriven.</span><span class="sxs-lookup"><span data-stu-id="fefc5-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="fefc5-134">Execute o comando `start WASAPIRenderExclusiveEventDriven.sln` no diretório RenderExclusiveEventDriven para abrir o projeto WASAPIRenderExclusiveEventDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fefc5-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="fefc5-135">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="fefc5-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="fefc5-136">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="fefc5-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="fefc5-137">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderExclusiveEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="fefc5-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="fefc5-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fefc5-138">Running the Sample</span></span>

<span data-ttu-id="fefc5-139">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderExclusiveEventDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="fefc5-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="fefc5-140">Para executá-lo, digite `WASAPIRenderExclusiveEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="fefc5-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="fefc5-141">O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="fefc5-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="fefc5-142">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="fefc5-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="fefc5-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="fefc5-143">Argument</span></span>        | <span data-ttu-id="fefc5-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="fefc5-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="fefc5-145">-?</span><span class="sxs-lookup"><span data-stu-id="fefc5-145">-?</span></span>              | <span data-ttu-id="fefc5-146">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="fefc5-146">Shows help.</span></span>                                                |
| <span data-ttu-id="fefc5-147">-H</span><span class="sxs-lookup"><span data-stu-id="fefc5-147">-h</span></span>              | <span data-ttu-id="fefc5-148">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="fefc5-148">Shows help.</span></span>                                                |
| <span data-ttu-id="fefc5-149">-f</span><span class="sxs-lookup"><span data-stu-id="fefc5-149">-f</span></span>              | <span data-ttu-id="fefc5-150">Frequência de onda do seno em Hz.</span><span class="sxs-lookup"><span data-stu-id="fefc5-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="fefc5-151">-l</span><span class="sxs-lookup"><span data-stu-id="fefc5-151">-l</span></span>              | <span data-ttu-id="fefc5-152">Latência de renderização de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="fefc5-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="fefc5-153">-d</span><span class="sxs-lookup"><span data-stu-id="fefc5-153">-d</span></span>              | <span data-ttu-id="fefc5-154">Duração da onda do seno em segundos.</span><span class="sxs-lookup"><span data-stu-id="fefc5-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="fefc5-155">-M</span><span class="sxs-lookup"><span data-stu-id="fefc5-155">-m</span></span>              | <span data-ttu-id="fefc5-156">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="fefc5-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="fefc5-157">-console</span><span class="sxs-lookup"><span data-stu-id="fefc5-157">-console</span></span>        | <span data-ttu-id="fefc5-158">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="fefc5-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="fefc5-159">-comunicações</span><span class="sxs-lookup"><span data-stu-id="fefc5-159">-communications</span></span> | <span data-ttu-id="fefc5-160">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="fefc5-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="fefc5-161">-multimídia</span><span class="sxs-lookup"><span data-stu-id="fefc5-161">-multimedia</span></span>     | <span data-ttu-id="fefc5-162">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="fefc5-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="fefc5-163">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="fefc5-163">-endpoint</span></span>       | <span data-ttu-id="fefc5-164">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="fefc5-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="fefc5-165">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de renderização.</span><span class="sxs-lookup"><span data-stu-id="fefc5-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="fefc5-166">Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda de seno a 440 Hz por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="fefc5-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="fefc5-167">Esses valores podem ser modificados especificando-se os valores de opção-f e-d.</span><span class="sxs-lookup"><span data-stu-id="fefc5-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="fefc5-168">O exemplo RenderExclusiveEventDriven demonstra o buffer controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="fefc5-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="fefc5-169">O exemplo mostra como:</span><span class="sxs-lookup"><span data-stu-id="fefc5-169">The sample shows how to:</span></span>

-   <span data-ttu-id="fefc5-170">Crie uma instância de um cliente de áudio, configure-o para ser executado em modo exclusivo e habilite o buffer controlado por evento definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="fefc5-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="fefc5-171">Associe o cliente com os exemplos que estão prontos para serem renderizados fornecendo um identificador de evento ao sistema chamando o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="fefc5-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="fefc5-172">Crie um thread de renderização para processar exemplos do mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="fefc5-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="fefc5-173">Alinhe os buffers corretamente em um limite de 128 bytes antes de enviá-los para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fefc5-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="fefc5-174">Isso é feito ajustando a periodicidade do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="fefc5-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="fefc5-175">Verifique o formato de combinação do ponto de extremidade do dispositivo para determinar se os exemplos podem ser renderizados.</span><span class="sxs-lookup"><span data-stu-id="fefc5-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="fefc5-176">Se o dispositivo não oferecer suporte ao formato Mix, os dados serão convertidos em PCM.</span><span class="sxs-lookup"><span data-stu-id="fefc5-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="fefc5-177">Manipular a alternância de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fefc5-177">Handle stream switching.</span></span>

<span data-ttu-id="fefc5-178">Depois que a sessão de renderização começa e o fluxo é iniciado, o mecanismo de áudio sinaliza o identificador de evento fornecido para notificar o cliente sempre que um buffer se tornar pronto para o cliente processar.</span><span class="sxs-lookup"><span data-stu-id="fefc5-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="fefc5-179">Os dados de áudio também podem ser processados em um loop controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="fefc5-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="fefc5-180">Esse modo é demonstrado no exemplo de [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="fefc5-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="fefc5-181">Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="fefc5-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fefc5-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fefc5-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fefc5-183">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="fefc5-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



