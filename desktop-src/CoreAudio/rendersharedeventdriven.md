---
description: Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: RenderSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826481"
---
# <a name="rendersharedeventdriven"></a><span data-ttu-id="b605e-103">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="b605e-103">RenderSharedEventDriven</span></span>

<span data-ttu-id="b605e-104">Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b605e-104">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="b605e-105">Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b605e-105">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="b605e-106">Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b605e-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="b605e-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b605e-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b605e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b605e-108">Description</span></span>](#description)
-   [<span data-ttu-id="b605e-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="b605e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b605e-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b605e-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b605e-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b605e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b605e-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b605e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b605e-114">Description</span></span>

<span data-ttu-id="b605e-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b605e-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="b605e-116">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="b605e-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="b605e-117">WASAPI para operações de gerenciamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b605e-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="b605e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b605e-118">Requirements</span></span>



| <span data-ttu-id="b605e-119">Produto</span><span class="sxs-lookup"><span data-stu-id="b605e-119">Product</span></span>                                                        | <span data-ttu-id="b605e-120">Versão</span><span class="sxs-lookup"><span data-stu-id="b605e-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b605e-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="b605e-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b605e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b605e-122">Windows 7</span></span> |
| <span data-ttu-id="b605e-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b605e-123">Visual Studio</span></span>                                                  | <span data-ttu-id="b605e-124">2008</span><span class="sxs-lookup"><span data-stu-id="b605e-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b605e-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-125">Downloading the Sample</span></span>

<span data-ttu-id="b605e-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="b605e-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b605e-127">Local</span><span class="sxs-lookup"><span data-stu-id="b605e-127">Location</span></span>    | <span data-ttu-id="b605e-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="b605e-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b605e-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="b605e-129">Windows SDK</span></span> | <span data-ttu-id="b605e-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ RenderSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="b605e-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b605e-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-131">Building the Sample</span></span>

<span data-ttu-id="b605e-132">Para criar o exemplo de RenderSharedEventDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b605e-132">To build the RenderSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="b605e-133">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo RenderSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="b605e-133">Open the CMD shell for the Windows SDK and change to the RenderSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="b605e-134">Execute o comando `start WASAPIRenderSharedEventDriven.sln` no diretório RenderSharedEventDriven para abrir o projeto WASAPIRenderSharedEventDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b605e-134">Run the command `start WASAPIRenderSharedEventDriven.sln` in the RenderSharedEventDriven directory to open the WASAPIRenderSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="b605e-135">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="b605e-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="b605e-136">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="b605e-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="b605e-137">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIRenderSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="b605e-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b605e-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b605e-138">Running the Sample</span></span>

<span data-ttu-id="b605e-139">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPIRenderSharedEventDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="b605e-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="b605e-140">Para executá-lo, digite `WASAPIRenderSharedEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="b605e-140">To run it, type `WASAPIRenderSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="b605e-141">O exemplo a seguir mostra como executar o exemplo especificando a duração da reprodução no dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="b605e-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="b605e-142">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="b605e-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="b605e-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="b605e-143">Argument</span></span>        | <span data-ttu-id="b605e-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="b605e-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="b605e-145">-?</span><span class="sxs-lookup"><span data-stu-id="b605e-145">-?</span></span>              | <span data-ttu-id="b605e-146">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="b605e-146">Shows help.</span></span>                                                |
| <span data-ttu-id="b605e-147">-H</span><span class="sxs-lookup"><span data-stu-id="b605e-147">-h</span></span>              | <span data-ttu-id="b605e-148">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="b605e-148">Shows help.</span></span>                                                |
| <span data-ttu-id="b605e-149">-f</span><span class="sxs-lookup"><span data-stu-id="b605e-149">-f</span></span>              | <span data-ttu-id="b605e-150">Frequência de onda do seno em Hz.</span><span class="sxs-lookup"><span data-stu-id="b605e-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="b605e-151">-l</span><span class="sxs-lookup"><span data-stu-id="b605e-151">-l</span></span>              | <span data-ttu-id="b605e-152">Latência de renderização de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b605e-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="b605e-153">-d</span><span class="sxs-lookup"><span data-stu-id="b605e-153">-d</span></span>              | <span data-ttu-id="b605e-154">Duração da onda do seno em segundos.</span><span class="sxs-lookup"><span data-stu-id="b605e-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="b605e-155">-M</span><span class="sxs-lookup"><span data-stu-id="b605e-155">-m</span></span>              | <span data-ttu-id="b605e-156">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="b605e-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="b605e-157">-console</span><span class="sxs-lookup"><span data-stu-id="b605e-157">-console</span></span>        | <span data-ttu-id="b605e-158">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="b605e-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="b605e-159">-comunicações</span><span class="sxs-lookup"><span data-stu-id="b605e-159">-communications</span></span> | <span data-ttu-id="b605e-160">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="b605e-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="b605e-161">-multimídia</span><span class="sxs-lookup"><span data-stu-id="b605e-161">-multimedia</span></span>     | <span data-ttu-id="b605e-162">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="b605e-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="b605e-163">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b605e-163">-endpoint</span></span>       | <span data-ttu-id="b605e-164">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="b605e-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="b605e-165">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de renderização.</span><span class="sxs-lookup"><span data-stu-id="b605e-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="b605e-166">Depois que o usuário especifica um dispositivo, o aplicativo renderiza uma onda de seno a 440 Hz por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="b605e-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="b605e-167">Esses valores podem ser modificados especificando-se os valores de opção-f e-d.</span><span class="sxs-lookup"><span data-stu-id="b605e-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="b605e-168">RenderSharedEventDriven demonstra o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="b605e-168">RenderSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="b605e-169">O exemplo mostra como:</span><span class="sxs-lookup"><span data-stu-id="b605e-169">The sample shows how to:</span></span>

-   <span data-ttu-id="b605e-170">Crie uma instância de um cliente de áudio, configure-o para ser executado em modo exclusivo e habilite o buffer controlado por evento definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="b605e-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="b605e-171">Associe o cliente com os exemplos que estão prontos para serem renderizados fornecendo um identificador de evento ao sistema chamando o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="b605e-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="b605e-172">Crie um thread de renderização para processar amostras do mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b605e-172">Create a render thread to proces samples from the audio engine.</span></span>
-   <span data-ttu-id="b605e-173">Verifique o formato de combinação do ponto de extremidade do dispositivo para determinar se os exemplos podem ser renderizados.</span><span class="sxs-lookup"><span data-stu-id="b605e-173">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="b605e-174">Se o dispositivo não oferecer suporte ao formato Mix, os dados serão convertidos em PCM.</span><span class="sxs-lookup"><span data-stu-id="b605e-174">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="b605e-175">Manipular a alternância de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b605e-175">Handle stream switching.</span></span>

<span data-ttu-id="b605e-176">Depois que a sessão de renderização começa e o fluxo é iniciado, o mecanismo de áudio sinaliza o identificador de evento fornecido para notificar o cliente sempre que um buffer se tornar pronto para o cliente processar.</span><span class="sxs-lookup"><span data-stu-id="b605e-176">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="b605e-177">Os dados de áudio também podem ser processados em um loop controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="b605e-177">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="b605e-178">Esse modo é demonstrado no exemplo de [RenderSharedTimerDriven](rendersharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="b605e-178">This mode is demonstrated in the [RenderSharedTimerDriven](rendersharedtimerdriven.md) sample.</span></span>

<span data-ttu-id="b605e-179">Para obter mais informações sobre como renderizar um fluxo, consulte [renderizando um fluxo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="b605e-179">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b605e-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b605e-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b605e-181">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="b605e-181">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



