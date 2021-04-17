---
description: Este aplicativo de exemplo demonstra a atenuação de fluxo implementando um player de mídia que mostra o comportamento de atenuação padrão fornecido pelo sistema, opta de eventos de pato e implementa manipulação personalizada quando eventos de pato são recebidos.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105754799"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="3e6d5-103">DuckingMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3e6d5-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="3e6d5-104">Este aplicativo de exemplo demonstra a atenuação de fluxo implementando um player de mídia que mostra o comportamento de atenuação padrão fornecido pelo sistema, opta de eventos de pato e implementa manipulação personalizada quando eventos de pato são recebidos.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="3e6d5-105">Este exemplo deve ser usado em juntamente com [DuckingCaptureSample](duckingcapturesample.md).</span><span class="sxs-lookup"><span data-stu-id="3e6d5-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="3e6d5-106">Para obter mais informações sobre o pato ou atenuação de fluxo, consulte [experiência de pato padrão](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="3e6d5-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="3e6d5-107">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e6d5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e6d5-108">Description</span></span>](#description)
-   [<span data-ttu-id="3e6d5-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="3e6d5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3e6d5-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3e6d5-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3e6d5-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3e6d5-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e6d5-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="3e6d5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e6d5-114">Description</span></span>

<span data-ttu-id="3e6d5-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="3e6d5-116">DirectShow para reproduzir um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="3e6d5-117">[WASAPI](wasapi.md) para gerenciamento de fluxo e manipulação de eventos de pato.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6d5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e6d5-118">Requirements</span></span>



| <span data-ttu-id="3e6d5-119">Produto</span><span class="sxs-lookup"><span data-stu-id="3e6d5-119">Product</span></span>                                                        | <span data-ttu-id="3e6d5-120">Versão</span><span class="sxs-lookup"><span data-stu-id="3e6d5-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3e6d5-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="3e6d5-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3e6d5-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e6d5-122">Windows 7</span></span> |
| <span data-ttu-id="3e6d5-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3e6d5-123">Visual Studio</span></span>                                                  | <span data-ttu-id="3e6d5-124">2008</span><span class="sxs-lookup"><span data-stu-id="3e6d5-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3e6d5-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-125">Downloading the Sample</span></span>

<span data-ttu-id="3e6d5-126">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="3e6d5-127">Local</span><span class="sxs-lookup"><span data-stu-id="3e6d5-127">Location</span></span>    | <span data-ttu-id="3e6d5-128">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="3e6d5-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6d5-129">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="3e6d5-129">Windows SDK</span></span> | <span data-ttu-id="3e6d5-130">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ DuckingMediaPlayer \\ ...</span><span class="sxs-lookup"><span data-stu-id="3e6d5-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="3e6d5-131">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-131">Building the Sample</span></span>

<span data-ttu-id="3e6d5-132">Para criar o exemplo de DuckingMediaPlayer, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3e6d5-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="3e6d5-133">Abra o DuckingMediaPlayer. sln no Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="3e6d5-134">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="3e6d5-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="3e6d5-135">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="3e6d5-136">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, DuckingMediaPlayer. vcproj.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3e6d5-137">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3e6d5-137">Running the Sample</span></span>

<span data-ttu-id="3e6d5-138">Se você compilar o aplicativo com êxito, um arquivo executável, DuckingMediaPlayer.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="3e6d5-139">Para executá-lo, selecione **Iniciar Depuração** ou **Iniciar sem Depurar** no menu **depurar** ou digite `DuckingMediaPlayer` uma janela de comando.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="3e6d5-140">Para exibir uma demonstração do patoing, você deve executar DuckingMediaPlayer e DuckingCaptureSample simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="3e6d5-141">DuckingCaptureSample abre um fluxo de comunicação e sinaliza o sistema para gerar um evento de patoing.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="3e6d5-142">O DuckingMediaPlayer é notificado pelo sistema quando ocorre um evento de patoing e o player de mídia executa a ação solicitada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="3e6d5-143">Para desabilitar o comportamento de pato:</span><span class="sxs-lookup"><span data-stu-id="3e6d5-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="3e6d5-144">Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="3e6d5-145">No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido e especifique a opção de pato como **recusar o pato**.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="3e6d5-146">Observe que o arquivo de mídia é reproduzido sem nenhuma interrupção.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="3e6d5-147">Os eventos gerados pelo sistema quando o fluxo de comunicação aberto são ignorados.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="3e6d5-148">Para demonstrar o comportamento padrão de pato fornecido pelo sistema, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3e6d5-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="3e6d5-149">Selecione a opção **sons** no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="3e6d5-150">Na guia **comunicações** , selecione **reduzir o volume de outros sons em 80%**.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="3e6d5-151">Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="3e6d5-152">No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido, sem escolher nenhuma das opções de pato.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="3e6d5-153">Na janela DuckingCaptureSample, clique em **parar** para interromper o fluxo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="3e6d5-154">Observe que quando o DuckingCaptureSample abre o fluxo de comunicação, o arquivo de mídia jogado por DuckingMediaPlayer é reproduzido sem interrupção, mas o nível de volume é reduzido.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="3e6d5-155">Quando a sessão de comunicação é interrompida, o volume é redefinido para a configuração original.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="3e6d5-156">Esse comportamento de atenuação de fluxo é o comportamento padrão de pato implementado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="3e6d5-157">Para exibir um comportamento de pato personalizado implementado pelo Player de mídia:</span><span class="sxs-lookup"><span data-stu-id="3e6d5-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="3e6d5-158">Na janela DuckingCaptureSample, selecione **usar dispositivo de entrada padrão** e clique em **Iniciar** para iniciar uma sessão de captura do dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="3e6d5-159">No DuckingMediaPlayer, selecione um arquivo de mídia a ser reproduzido e especifique a opção de pato como **pausa no pato**.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="3e6d5-160">Na janela DuckingCaptureSample, clique em **parar** para interromper o fluxo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="3e6d5-161">Observe que quando o DuckingCaptureSample abre o fluxo de comunicação, o arquivo de mídia jogado por DuckingMediaPlayer é pausado.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="3e6d5-162">A reprodução é retomada quando a sessão de comunicação é interrompida.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="3e6d5-163">Esse comportamento de atenuação de fluxo é o comportamento de pato implementado pelo Player de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="3e6d5-164">DuckingMediaPlayer também demonstra como integrar o controle de volume para cada aplicativo com o mixer de volume.</span><span class="sxs-lookup"><span data-stu-id="3e6d5-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="3e6d5-165">Para obter mais informações sobre o recurso de atenuação de fluxo, consulte [experiência de pato padrão](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="3e6d5-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e6d5-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e6d5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6d5-167">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="3e6d5-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



