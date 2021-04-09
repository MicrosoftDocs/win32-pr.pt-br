---
description: Este exemplo usa as APIs de áudio principais para capturar um fluxo de voz de alta qualidade. O exemplo dá suporte a AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO, também chamado de DSP de captura de voz, fornecido pela Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089635"
---
# <a name="aecmicarray"></a><span data-ttu-id="0a455-104">AECMicArray</span><span class="sxs-lookup"><span data-stu-id="0a455-104">AECMicArray</span></span>

<span data-ttu-id="0a455-105">Este exemplo usa as APIs de áudio principais para capturar um fluxo de voz de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="0a455-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="0a455-106">O exemplo dá suporte a AEC (cancelamento de eco acústico) e ao processamento de matriz de microfone usando o AEC DMO, também chamado de DSP de captura de voz, fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a455-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="0a455-107">Este tópico contém as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a455-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="0a455-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a455-108">Description</span></span>](#description)
-   [<span data-ttu-id="0a455-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="0a455-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0a455-110">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0a455-111">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0a455-112">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0a455-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a455-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="0a455-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a455-114">Description</span></span>

<span data-ttu-id="0a455-115">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a455-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="0a455-116">[MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="0a455-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="0a455-117">[WASAPI](wasapi.md) para operações de gerenciamento de fluxo, como iniciar e interromper o fluxo, alternando o fluxo.</span><span class="sxs-lookup"><span data-stu-id="0a455-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="0a455-118">[DeviceTopology](devicetopology-api.md) para enumerar adaptadores de áudio.</span><span class="sxs-lookup"><span data-stu-id="0a455-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="0a455-119">[EndpointVolume](endpointvolume-api.md) controle os níveis de volume de [sessões de áudio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="0a455-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a455-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a455-120">Requirements</span></span>



| <span data-ttu-id="0a455-121">Produto</span><span class="sxs-lookup"><span data-stu-id="0a455-121">Product</span></span>                                                        | <span data-ttu-id="0a455-122">Versão</span><span class="sxs-lookup"><span data-stu-id="0a455-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="0a455-123">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="0a455-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0a455-124">Windows Vista ou posterior</span><span class="sxs-lookup"><span data-stu-id="0a455-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="0a455-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a455-125">Visual Studio</span></span>                                                  | <span data-ttu-id="0a455-126">2005 (edições não Express)</span><span class="sxs-lookup"><span data-stu-id="0a455-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0a455-127">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-127">Downloading the Sample</span></span>

<span data-ttu-id="0a455-128">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a455-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0a455-129">Local</span><span class="sxs-lookup"><span data-stu-id="0a455-129">Location</span></span>    | <span data-ttu-id="0a455-130">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="0a455-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a455-131">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="0a455-131">Windows SDK</span></span> | <span data-ttu-id="0a455-132">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ AECMicArray \\ ...</span><span class="sxs-lookup"><span data-stu-id="0a455-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="0a455-133">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-133">Building the Sample</span></span>

<span data-ttu-id="0a455-134">Para criar o exemplo de AecSDKDemo, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="0a455-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="0a455-135">Abra uma janela de comando do SDK.</span><span class="sxs-lookup"><span data-stu-id="0a455-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="0a455-136">Digite **CD% MSSDK% \\ Setup**.</span><span class="sxs-lookup"><span data-stu-id="0a455-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="0a455-137">Execute VCIntegrate.exe.</span><span class="sxs-lookup"><span data-stu-id="0a455-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="0a455-138">Deste ponto em diante, as janelas de comando terão as configurações de ambiente adequadas para criar um aplicativo que aproveita o SDK.</span><span class="sxs-lookup"><span data-stu-id="0a455-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="0a455-139">Compile o exemplo.</span><span class="sxs-lookup"><span data-stu-id="0a455-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0a455-140">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0a455-140">Running the Sample</span></span>

<span data-ttu-id="0a455-141">Se você criar o aplicativo de demonstração com êxito, um arquivo executável AecSDKDemo.exe será gerado.</span><span class="sxs-lookup"><span data-stu-id="0a455-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="0a455-142">Para executá-lo, digite `AecSDKDemo` uma janela de comando seguida por argumentos obrigatórios ou opcionais, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="0a455-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="0a455-143">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="0a455-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="0a455-144">Argumento</span><span class="sxs-lookup"><span data-stu-id="0a455-144">Argument</span></span>  | <span data-ttu-id="0a455-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a455-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a455-146">-out</span><span class="sxs-lookup"><span data-stu-id="0a455-146">-out</span></span>      | <span data-ttu-id="0a455-147">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0a455-147">Required.</span></span> <span data-ttu-id="0a455-148">Especifica o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="0a455-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="0a455-149">-mod</span><span class="sxs-lookup"><span data-stu-id="0a455-149">-mod</span></span>      | <span data-ttu-id="0a455-150">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0a455-150">Required.</span></span> <span data-ttu-id="0a455-151">Especifica o modo do sistema de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="0a455-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="0a455-152">Consulte a seção "Configurando a captura de voz DMO" no Leiame de exemplo para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0a455-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="0a455-153">-feito</span><span class="sxs-lookup"><span data-stu-id="0a455-153">-feat</span></span>     | <span data-ttu-id="0a455-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-154">Optional.</span></span> <span data-ttu-id="0a455-155">Ativa o modo de recurso em (1) ou desativado (0).</span><span class="sxs-lookup"><span data-stu-id="0a455-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="0a455-156">-NS</span><span class="sxs-lookup"><span data-stu-id="0a455-156">-ns</span></span>       | <span data-ttu-id="0a455-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-157">Optional.</span></span> <span data-ttu-id="0a455-158">Ativa a supressão de ruído em (1) ou off (0).</span><span class="sxs-lookup"><span data-stu-id="0a455-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="0a455-159">O modo de recurso deve estar ativado para especificar isso.</span><span class="sxs-lookup"><span data-stu-id="0a455-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="0a455-160">-agc</span><span class="sxs-lookup"><span data-stu-id="0a455-160">-agc</span></span>      | <span data-ttu-id="0a455-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-161">Optional.</span></span> <span data-ttu-id="0a455-162">Transforma AGC digital em (1) ou off (0).</span><span class="sxs-lookup"><span data-stu-id="0a455-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="0a455-163">O modo de recurso deve estar ativado para especificar isso.</span><span class="sxs-lookup"><span data-stu-id="0a455-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="0a455-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="0a455-164">-cntrclip</span></span> | <span data-ttu-id="0a455-165">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-165">Optional.</span></span> <span data-ttu-id="0a455-166">Desativa o recorte de centro em (1) ou desativado (0).</span><span class="sxs-lookup"><span data-stu-id="0a455-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="0a455-167">O modo de recurso deve estar ativado para especificar isso.</span><span class="sxs-lookup"><span data-stu-id="0a455-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="0a455-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="0a455-168">-spkdev</span></span>   | <span data-ttu-id="0a455-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-169">Optional.</span></span> <span data-ttu-id="0a455-170">Especifica o índice do dispositivo do orador.</span><span class="sxs-lookup"><span data-stu-id="0a455-170">Specifies speaker device index.</span></span> <span data-ttu-id="0a455-171">Se não for especificado, o usuário será solicitado a selecionar.</span><span class="sxs-lookup"><span data-stu-id="0a455-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="0a455-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="0a455-172">-micdev</span></span>   | <span data-ttu-id="0a455-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-173">Optional.</span></span> <span data-ttu-id="0a455-174">Especifica o índice do dispositivo de microfone.</span><span class="sxs-lookup"><span data-stu-id="0a455-174">Specifies microphone device index.</span></span> <span data-ttu-id="0a455-175">Se não for especificado, o usuário será solicitado a selecionar.</span><span class="sxs-lookup"><span data-stu-id="0a455-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="0a455-176">-duração</span><span class="sxs-lookup"><span data-stu-id="0a455-176">-duration</span></span> | <span data-ttu-id="0a455-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a455-177">Optional.</span></span> <span data-ttu-id="0a455-178">Especifica por quanto tempo o aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="0a455-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="0a455-179">Este aplicativo de exemplo não executa sinais.</span><span class="sxs-lookup"><span data-stu-id="0a455-179">This sample application does not play any signals.</span></span> <span data-ttu-id="0a455-180">Para executar a demonstração corretamente para os modos habilitados para AEC (modo 0 e 4), os usuários devem reproduzir alguns sinais de áudio por meio do mesmo dispositivo de alto-falante especificado para o DMO (ou seja, o dispositivo especificado pela opção "-spkdev"), que simula a voz de ponta em um cenário de bate-papo bidirecional.</span><span class="sxs-lookup"><span data-stu-id="0a455-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="0a455-181">Os usuários podem usar qualquer jogador para reproduzir sinais de áudio.</span><span class="sxs-lookup"><span data-stu-id="0a455-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="0a455-182">Se não houver nenhum fluxo de renderização ativo no dispositivo de alto-falante selecionado, o DMO falhará ao processar.</span><span class="sxs-lookup"><span data-stu-id="0a455-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a455-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a455-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a455-184">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="0a455-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



