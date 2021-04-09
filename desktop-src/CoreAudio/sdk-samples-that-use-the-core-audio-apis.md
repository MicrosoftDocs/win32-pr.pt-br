---
description: Exemplos de SDK que usam as APIs de áudio principal
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemplos de SDK que usam as APIs de áudio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920407"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="61393-103">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="61393-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="61393-104">O SDK do Windows inclui os exemplos de código a seguir que demonstram o uso das APIs de áudio principais.</span><span class="sxs-lookup"><span data-stu-id="61393-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="61393-105">Os exemplos a seguir estão localizados no diretório% MSSdk% \\ Sample \\ \\ áudio multimídia, em que% MSSdk% é o diretório raiz da instalação do SDK do Windows no seu computador.</span><span class="sxs-lookup"><span data-stu-id="61393-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61393-106">Amostra</span><span class="sxs-lookup"><span data-stu-id="61393-106">Sample</span></span></th>
<th><span data-ttu-id="61393-107">Deascription</span><span class="sxs-lookup"><span data-stu-id="61393-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61393-108"><a href="aecmicarray.md">AECMicArray</a></span><span class="sxs-lookup"><span data-stu-id="61393-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="61393-109">Este exemplo usa as APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume para capturar um fluxo de voz de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="61393-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="61393-110">O exemplo de Tnão dá suporte a um AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO também chamado de DSP de captura de voz fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61393-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61393-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="61393-112">Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificado pelo usuário e grava-os em um nome exclusivo. Arquivo WAV no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="61393-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="61393-113">Este exemplo demonstra o buffer controlado por eventos.</span><span class="sxs-lookup"><span data-stu-id="61393-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61393-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="61393-115">Este aplicativo de exemplo usa as APIs de áudio principais para capturar dados de áudio de um dispositivo de entrada, especificado pelo usuário e grava-os em um nome exclusivo. Arquivo WAV no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="61393-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="61393-116">Este exemplo demonstra o buffer controlado por temporizador.</span><span class="sxs-lookup"><span data-stu-id="61393-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61393-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span><span class="sxs-lookup"><span data-stu-id="61393-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="61393-118">Este aplicativo de exemplo demonstra como abrir e fechar fluxos de comunicação e causar eventos de pato que um aplicativo pode obter para implementar a atenuação de fluxo.</span><span class="sxs-lookup"><span data-stu-id="61393-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="61393-119">Esse aplicativo implementa um cliente de chat que usa APIs de áudio de núcleo para ler dados de áudio de um dispositivo de comunicação e reproduzi-lo no dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="61393-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61393-120"><a href="endpointvolume.md">EndpointVolume</a></span><span class="sxs-lookup"><span data-stu-id="61393-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="61393-121">Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61393-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61393-122"><a href="osd.md">OSD Feature</a></span><span class="sxs-lookup"><span data-stu-id="61393-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="61393-123">Este exemplo usa as APIs MMDevice e EndpointVolume para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="61393-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="61393-124">A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume do Windows, Sndvol.exe e desaparece depois que o nível do volume permanece inalterado por um curto período de tempo.</span><span class="sxs-lookup"><span data-stu-id="61393-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61393-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="61393-126">Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61393-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="61393-127">Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="61393-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="61393-128">Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61393-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61393-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="61393-130">Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61393-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="61393-131">Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="61393-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="61393-132">Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61393-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61393-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="61393-134">Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61393-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="61393-135">Este exemplo demonstra o buffer controlado por eventos para um cliente de renderização no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="61393-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="61393-136">Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61393-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61393-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="61393-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="61393-138">Este aplicativo de exemplo usa as APIs de áudio principais para processar dados de áudio para um dispositivo de saída, especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61393-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="61393-139">Este exemplo demonstra o buffer controlado por temporizador para um cliente de renderização no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="61393-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="61393-140">Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61393-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61393-141">WinAudio</span><span class="sxs-lookup"><span data-stu-id="61393-141">WinAudio</span></span></td>
<td><span data-ttu-id="61393-142">Este exemplo usa a API MMDevice e o WASAPI para reproduzir e capturar fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="61393-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="61393-143">A interface do usuário deste aplicativo de exemplo permite que os usuários selecionem dispositivos de ponto de extremidade de áudio, alterem o nível de volume da sessão de áudio local e reproduza arquivos. wav e entrada de microfone.</span><span class="sxs-lookup"><span data-stu-id="61393-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61393-144">Este exemplo foi preterido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61393-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61393-145">Você pode baixar o SDK do Windows no site do [centro de download do SDK do Microsoft Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/) .</span><span class="sxs-lookup"><span data-stu-id="61393-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61393-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61393-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61393-147">Sobre as APIs de áudio do Windows Core</span><span class="sxs-lookup"><span data-stu-id="61393-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




