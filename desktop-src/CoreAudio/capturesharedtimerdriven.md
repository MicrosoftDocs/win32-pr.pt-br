---
description: Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual. Este exemplo demonstra o buffer controlado por temporizador.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010204"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="bbe4e-104">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="bbe4e-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="bbe4e-105">Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada especificado pelo usuário e grava-os em um arquivo. wav nomeado exclusivamente no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="bbe4e-106">Este exemplo demonstra o buffer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="bbe4e-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bbe4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbe4e-108">Description</span></span>](#description)
-   [<span data-ttu-id="bbe4e-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="bbe4e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bbe4e-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="bbe4e-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="bbe4e-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="bbe4e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbe4e-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="bbe4e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbe4e-114">Description</span></span>

<span data-ttu-id="bbe4e-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="bbe4e-116">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="bbe4e-117">[WASAPI](wasapi.md) para operações de gerenciamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe4e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbe4e-118">Requirements</span></span>



| <span data-ttu-id="bbe4e-119">Produto</span><span class="sxs-lookup"><span data-stu-id="bbe4e-119">Product</span></span>                                                        | <span data-ttu-id="bbe4e-120">Versão</span><span class="sxs-lookup"><span data-stu-id="bbe4e-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bbe4e-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="bbe4e-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bbe4e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbe4e-122">Windows 7</span></span> |
| <span data-ttu-id="bbe4e-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bbe4e-123">Visual Studio</span></span>                                                  | <span data-ttu-id="bbe4e-124">2008</span><span class="sxs-lookup"><span data-stu-id="bbe4e-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bbe4e-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-125">Downloading the Sample</span></span>

<span data-ttu-id="bbe4e-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="bbe4e-127">Local</span><span class="sxs-lookup"><span data-stu-id="bbe4e-127">Location</span></span>    | <span data-ttu-id="bbe4e-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="bbe4e-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe4e-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="bbe4e-129">Windows SDK</span></span> | <span data-ttu-id="bbe4e-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ CaptureSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="bbe4e-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="bbe4e-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-131">Building the Sample</span></span>

<span data-ttu-id="bbe4e-132">Para criar o exemplo de CaptureSharedTimerDriven, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="bbe4e-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="bbe4e-133">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo CaptureSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="bbe4e-134">Execute o comando `start WASAPICaptureSharedTimerDriven.sln` no diretório CaptureSharedTimerDriven para abrir o projeto WASAPICaptureSharedTimerDriven na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="bbe4e-135">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="bbe4e-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="bbe4e-136">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="bbe4e-137">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPICaptureSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="bbe4e-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe4e-138">Running the Sample</span></span>

<span data-ttu-id="bbe4e-139">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, WASAPICaptureSharedTimerDriven.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="bbe4e-140">Para executá-lo, digite `WASAPICaptureSharedTimerDriven` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="bbe4e-141">O exemplo a seguir mostra como executar o exemplo especificando a duração da captura no dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="bbe4e-142">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="bbe4e-143">Argumento</span><span class="sxs-lookup"><span data-stu-id="bbe4e-143">Argument</span></span>        | <span data-ttu-id="bbe4e-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbe4e-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="bbe4e-145">-?</span><span class="sxs-lookup"><span data-stu-id="bbe4e-145">-?</span></span>              | <span data-ttu-id="bbe4e-146">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-146">Shows help.</span></span>                                                |
| <span data-ttu-id="bbe4e-147">-H</span><span class="sxs-lookup"><span data-stu-id="bbe4e-147">-h</span></span>              | <span data-ttu-id="bbe4e-148">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-148">Shows help.</span></span>                                                |
| <span data-ttu-id="bbe4e-149">-l</span><span class="sxs-lookup"><span data-stu-id="bbe4e-149">-l</span></span>              | <span data-ttu-id="bbe4e-150">Latência de captura de áudio em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="bbe4e-151">-d</span><span class="sxs-lookup"><span data-stu-id="bbe4e-151">-d</span></span>              | <span data-ttu-id="bbe4e-152">Duração da captura de áudio em segundos.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="bbe4e-153">-M</span><span class="sxs-lookup"><span data-stu-id="bbe4e-153">-m</span></span>              | <span data-ttu-id="bbe4e-154">Desabilita o uso do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="bbe4e-155">-console</span><span class="sxs-lookup"><span data-stu-id="bbe4e-155">-console</span></span>        | <span data-ttu-id="bbe4e-156">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="bbe4e-157">-comunicações</span><span class="sxs-lookup"><span data-stu-id="bbe4e-157">-communications</span></span> | <span data-ttu-id="bbe4e-158">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="bbe4e-159">-multimídia</span><span class="sxs-lookup"><span data-stu-id="bbe4e-159">-multimedia</span></span>     | <span data-ttu-id="bbe4e-160">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="bbe4e-161">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="bbe4e-161">-endpoint</span></span>       | <span data-ttu-id="bbe4e-162">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="bbe4e-163">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo para a sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="bbe4e-164">Os dispositivos de console, comunicação e multimídia padrão são listados seguidos por dispositivos e os identificadores de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="bbe4e-165">Se nenhuma duração for especificada, o fluxo de áudio do dispositivo especificado será capturado por 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="bbe4e-166">O aplicativo grava os dados capturados em um arquivo. wav nomeado exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="bbe4e-167">CaptureSharedTimerDriven demonstra o buffer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="bbe4e-168">Nesse modo, o cliente deve aguardar por um período de tempo (metade da latência, especificado pelo valor da opção-d, em milissegundos).</span><span class="sxs-lookup"><span data-stu-id="bbe4e-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="bbe4e-169">Quando o cliente é ativado, metade do período de processamento, ele obtém o próximo conjunto de amostras do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="bbe4e-170">Antes de cada passagem de processamento no loop de buffer, o cliente deve descobrir a quantidade de dados de captura disponíveis para que os dados não estourem o buffer de captura.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="bbe4e-171">Os dados de áudio que são capturados do dispositivo especificado podem ser processados habilitando o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="bbe4e-172">Esse modo é demonstrado no exemplo de [CaptureSharedEventDriven](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe4e-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbe4e-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbe4e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe4e-174">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="bbe4e-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



