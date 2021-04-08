---
description: Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por eventos.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089249"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="c89bc-104">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="c89bc-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="c89bc-105">Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="c89bc-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="c89bc-106">Este exemplo demonstra o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="c89bc-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c89bc-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c89bc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c89bc-108">Description</span></span>](#description)
-   [<span data-ttu-id="c89bc-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="c89bc-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c89bc-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c89bc-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c89bc-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c89bc-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c89bc-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c89bc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c89bc-114">Description</span></span>

<span data-ttu-id="c89bc-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c89bc-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="c89bc-116">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="c89bc-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="c89bc-117">[WASAPI](wasapi.md) para operações de gerenciamento de fluxo, como iniciar e interromper o fluxo e alternar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="c89bc-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="c89bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c89bc-118">Requirements</span></span>



| <span data-ttu-id="c89bc-119">Produto</span><span class="sxs-lookup"><span data-stu-id="c89bc-119">Product</span></span>                                                        | <span data-ttu-id="c89bc-120">Versão</span><span class="sxs-lookup"><span data-stu-id="c89bc-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c89bc-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="c89bc-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c89bc-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c89bc-122">Windows 7</span></span> |
| <span data-ttu-id="c89bc-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c89bc-123">Visual Studio</span></span>                                                  | <span data-ttu-id="c89bc-124">2008</span><span class="sxs-lookup"><span data-stu-id="c89bc-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c89bc-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-125">Downloading the Sample</span></span>

<span data-ttu-id="c89bc-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="c89bc-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c89bc-127">Local</span><span class="sxs-lookup"><span data-stu-id="c89bc-127">Location</span></span>    | <span data-ttu-id="c89bc-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="c89bc-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c89bc-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="c89bc-129">Windows SDK</span></span> | <span data-ttu-id="c89bc-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ CaptureSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="c89bc-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="c89bc-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-131">Building the Sample</span></span>

<span data-ttu-id="c89bc-132">Para criar o exemplo de CaptureSharedEventDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="c89bc-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="c89bc-133">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo CaptureSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="c89bc-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="c89bc-134">Execute o comando `start WASAPICaptureSharedEventDriven.sln` no diretório CaptureSharedEventDriven para abrir o projeto WASAPICaptureSharedEventDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c89bc-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="c89bc-135">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="c89bc-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="c89bc-136">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="c89bc-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="c89bc-137">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPICaptureSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="c89bc-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c89bc-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c89bc-138">Running the Sample</span></span>

<span data-ttu-id="c89bc-139">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPICaptureSharedEventDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="c89bc-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="c89bc-140">Para executá-lo, digite `WASAPICaptureSharedEventDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="c89bc-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="c89bc-141">O exemplo a seguir mostra como executar o exemplo especificando a duração da captura no dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="c89bc-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="c89bc-142">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="c89bc-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="c89bc-143">Argument</span></span>        | <span data-ttu-id="c89bc-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="c89bc-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="c89bc-145">-?</span><span class="sxs-lookup"><span data-stu-id="c89bc-145">-?</span></span>              | <span data-ttu-id="c89bc-146">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="c89bc-146">Shows help.</span></span>                                                |
| <span data-ttu-id="c89bc-147">-H</span><span class="sxs-lookup"><span data-stu-id="c89bc-147">-h</span></span>              | <span data-ttu-id="c89bc-148">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="c89bc-148">Shows help.</span></span>                                                |
| <span data-ttu-id="c89bc-149">-l</span><span class="sxs-lookup"><span data-stu-id="c89bc-149">-l</span></span>              | <span data-ttu-id="c89bc-150">Latência de captura de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="c89bc-151">-d</span><span class="sxs-lookup"><span data-stu-id="c89bc-151">-d</span></span>              | <span data-ttu-id="c89bc-152">Duração da captura de áudio em segundos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="c89bc-153">-M</span><span class="sxs-lookup"><span data-stu-id="c89bc-153">-m</span></span>              | <span data-ttu-id="c89bc-154">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="c89bc-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="c89bc-155">-console</span><span class="sxs-lookup"><span data-stu-id="c89bc-155">-console</span></span>        | <span data-ttu-id="c89bc-156">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="c89bc-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="c89bc-157">-comunicações</span><span class="sxs-lookup"><span data-stu-id="c89bc-157">-communications</span></span> | <span data-ttu-id="c89bc-158">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="c89bc-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="c89bc-159">-multimídia</span><span class="sxs-lookup"><span data-stu-id="c89bc-159">-multimedia</span></span>     | <span data-ttu-id="c89bc-160">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="c89bc-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="c89bc-161">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="c89bc-161">-endpoint</span></span>       | <span data-ttu-id="c89bc-162">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="c89bc-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="c89bc-163">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="c89bc-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="c89bc-164">Os dispositivos de console, comunicação e multimídia padrão são listados seguidos por dispositivos e os identificadores de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c89bc-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="c89bc-165">Se nenhuma duração for especificada, o fluxo de áudio do dispositivo especificado será capturado por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="c89bc-166">O aplicativo grava os dados capturados em um arquivo. wav nomeado exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c89bc-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="c89bc-167">CaptureSharedEventDriven demonstra o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="c89bc-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="c89bc-168">O cliente de áudio instanciado para este exemplo está configurado para ser executado no modo compartilhado e o processamento do cliente do buffer de áudio é feito com eventos definindo o sinalizador **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** na chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="c89bc-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="c89bc-169">O exemplo mostra como o cliente deve fornecer um identificador de evento ao sistema chamando o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="c89bc-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="c89bc-170">Depois que a sessão de captura começa e o fluxo é iniciado, o mecanismo de áudio sinaliza o identificador de evento fornecido para notificar o cliente sempre que um buffer se tornar pronto para o cliente processar.</span><span class="sxs-lookup"><span data-stu-id="c89bc-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="c89bc-171">Os dados de áudio também podem ser processados em um loop controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="c89bc-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="c89bc-172">Esse modo é demostrated no exemplo de [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="c89bc-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c89bc-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c89bc-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c89bc-174">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="c89bc-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



