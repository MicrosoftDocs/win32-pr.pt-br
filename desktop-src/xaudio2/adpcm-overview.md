---
description: O ADPCM (modulação diferencial de código de pulso) adaptável é um formato de compactação com perdas que é implementado para XAudio2 a fim de fornecer recursos adicionais para especificar o tamanho do bloco de amostra de compactação.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Visão geral de ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788704"
---
# <a name="adpcm-overview"></a><span data-ttu-id="bd2c6-103">Visão geral de ADPCM</span><span class="sxs-lookup"><span data-stu-id="bd2c6-103">ADPCM Overview</span></span>

<span data-ttu-id="bd2c6-104">O ADPCM (modulação diferencial de código de pulso) adaptável é um formato de compactação com perdas que é implementado para XAudio2 a fim de fornecer recursos adicionais para especificar o tamanho do bloco de amostra de compactação.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="bd2c6-105">Com um formato de compactação com perdas, alguns dados são alterados e perdidos durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="bd2c6-106">O ADPCM pode obter taxas de compactação de até 4:1.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="bd2c6-107">A implementação de ADPCM for XAudio2 fornece recursos adicionais para especificar o tamanho do bloco de amostra de compactação.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="bd2c6-108">O ADPCM permite que o designer de áudio escolha uma configuração que seja um comprometimento apropriado entre o tamanho, a qualidade e a resolução (para colocar pontos de loop).</span><span class="sxs-lookup"><span data-stu-id="bd2c6-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="bd2c6-109">O XAudio2 usa uma versão modificada do codec ADPCM da Microsoft que dá suporte à formatação de dados estendidos necessária para fornecer tamanhos de bloco de amostra personalizados.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="bd2c6-110">Por esse motivo, os dados de áudio XAudio2 não podem ser reproduzidos por mecanismos de áudio que não dão suporte a essa versão do codec ADPCM.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="bd2c6-111">Atualmente, a compactação ADPCM só está disponível para o Windows, incluindo o XNA Game Studio Express para implantações do Windows.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="bd2c6-112">Codificação ADPCM</span><span class="sxs-lookup"><span data-stu-id="bd2c6-112">ADPCM Encoding</span></span>

<span data-ttu-id="bd2c6-113">Os dados de áudio são codificados para ADPCM usando a ferramenta de linha de comando AdpcmEncode.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="bd2c6-114">AdpcmEncode</span><span class="sxs-lookup"><span data-stu-id="bd2c6-114">AdpcmEncode</span></span>

    <span data-ttu-id="bd2c6-115">Para codificar arquivos de áudio como ADPCM para uso com XAudio2, use a ferramenta de linha de comando **AdpcmEncode** .</span><span class="sxs-lookup"><span data-stu-id="bd2c6-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="bd2c6-116">Decodificação de ADPCM</span><span class="sxs-lookup"><span data-stu-id="bd2c6-116">ADPCM Decoding</span></span>

<span data-ttu-id="bd2c6-117">A decodificação de software de ADPCM tem suporte em XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="bd2c6-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="bd2c6-118">XAudio2</span></span>

    <span data-ttu-id="bd2c6-119">Para usar dados codificados em ADPCM no XAudio2, você precisa inicializar uma estrutura **ADPCMWAVEFORMAT** com valores específicos de ADPCM e passá-la como um argumento para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) ao criar uma voz de origem.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="bd2c6-120">Para obter um exemplo de como carregar e reproduzir um som no XAudio2, consulte [como: tocar um som com XAudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c6-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="bd2c6-121">SamplesPerBlock</span><span class="sxs-lookup"><span data-stu-id="bd2c6-121">SamplesPerBlock</span></span>

<span data-ttu-id="bd2c6-122">A compactação ADPCM funciona separando a forma de onda em blocos e prevendo a variação das amostras de forma de onda dentro de cada bloco.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="bd2c6-123">O tamanho dos blocos é medido em exemplos.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="bd2c6-124">O menor tamanho de bloco é de 32 amostras e os mais altos são os exemplos de 512.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="bd2c6-125">Blocos maiores permitem uma melhor compactação, o que resulta em tamanhos de arquivo menores, mas às custas da qualidade de som e da resolução para alinhar pontos de loop.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="bd2c6-126">Em geral, modificar o valor de SamplesPerBlock resulta nessas compensações:</span><span class="sxs-lookup"><span data-stu-id="bd2c6-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="bd2c6-127">Se SamplesPerBlock...</span><span class="sxs-lookup"><span data-stu-id="bd2c6-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="bd2c6-128">Compactação de arquivo</span><span class="sxs-lookup"><span data-stu-id="bd2c6-128">File Compression</span></span> | <span data-ttu-id="bd2c6-129">Qualidade do som</span><span class="sxs-lookup"><span data-stu-id="bd2c6-129">Sound Quality</span></span> | <span data-ttu-id="bd2c6-130">Resolução de ponto de loop</span><span class="sxs-lookup"><span data-stu-id="bd2c6-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="bd2c6-131">Aumenta (até o máximo 512)</span><span class="sxs-lookup"><span data-stu-id="bd2c6-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="bd2c6-132">Aumento</span><span class="sxs-lookup"><span data-stu-id="bd2c6-132">Increases</span></span>        | <span data-ttu-id="bd2c6-133">Diminui</span><span class="sxs-lookup"><span data-stu-id="bd2c6-133">Decreases</span></span>     | <span data-ttu-id="bd2c6-134">Diminui</span><span class="sxs-lookup"><span data-stu-id="bd2c6-134">Decreases</span></span>             |
| <span data-ttu-id="bd2c6-135">Diminui (até o mínimo 32)</span><span class="sxs-lookup"><span data-stu-id="bd2c6-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="bd2c6-136">Diminui</span><span class="sxs-lookup"><span data-stu-id="bd2c6-136">Decreases</span></span>        | <span data-ttu-id="bd2c6-137">Aumento</span><span class="sxs-lookup"><span data-stu-id="bd2c6-137">Increases</span></span>     | <span data-ttu-id="bd2c6-138">Aumento</span><span class="sxs-lookup"><span data-stu-id="bd2c6-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="bd2c6-139">Restrições</span><span class="sxs-lookup"><span data-stu-id="bd2c6-139">Restrictions</span></span>

<span data-ttu-id="bd2c6-140">Como o ADPCM usa blocos de exemplo alinhados um após o outro, uma onda compactada com ADPCM pode ter um bloco não concluído e parcial em seu final.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="bd2c6-141">O decodificador ADPCM gera silêncio para o restante deste bloco parcial, o que impede que a onda faça um loop contínuo.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="bd2c6-142">O valor do parâmetro *SamplesPerBlock* afeta a resolução com a qual você pode alinhar os dados de onda e os pontos de loop.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="bd2c6-143">Se você tentar aplicar a compactação a uma onda não alinhada, receberá um erro ou um aviso, dependendo se a onda é usada em qualquer evento de reprodução de looping.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="bd2c6-144">Não é possível compactar uma onda usada em qualquer evento de reprodução de looping.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="bd2c6-145">Remova-o dos eventos de reprodução de loop e aplique novamente a compactação.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="bd2c6-146">Se você usar a onda exclusivamente no modo sem looping, a restrição de alinhamento de bloco de exemplo não se aplicará.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="bd2c6-147">Estrutura de arquivo ADPCM</span><span class="sxs-lookup"><span data-stu-id="bd2c6-147">ADPCM File Structure</span></span>

<span data-ttu-id="bd2c6-148">Um arquivo ADPCM é um arquivo RIFF padrão com os seguintes tipos de bloco.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="bd2c6-149">Parte da FCC</span><span class="sxs-lookup"><span data-stu-id="bd2c6-149">Chunk FCC</span></span>     | <span data-ttu-id="bd2c6-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd2c6-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2c6-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="bd2c6-151">RIFF</span></span>          | <span data-ttu-id="bd2c6-152">A parte padrão do RIFF que contém um tipo de arquivo com o valor WAVE nos primeiros quatro bytes de sua seção de dados e as outras partes no arquivo no restante de sua seção de dados.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bd2c6-153">fmt</span><span class="sxs-lookup"><span data-stu-id="bd2c6-153">fmt</span></span>           | <span data-ttu-id="bd2c6-154">Contém o cabeçalho de formato do arquivo ADPCM.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="bd2c6-155">Os dados nessa parte correspondem a uma estrutura **ADPCMWAVEFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="bd2c6-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bd2c6-156">data</span><span class="sxs-lookup"><span data-stu-id="bd2c6-156">data</span></span>          | <span data-ttu-id="bd2c6-157">Contém os dados de áudio ADPCM codificados.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="bd2c6-158">Ao usar o ADPCM em XAudio2, você precisa ler o conteúdo da parte de dados em um buffer e passá-lo para uma voz de origem como o membro **pAudioData** de uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="bd2c6-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="bd2c6-159">Você não precisa trocar o conteúdo da parte de dados.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="bd2c6-160">smpl e wsmp</span><span class="sxs-lookup"><span data-stu-id="bd2c6-160">smpl and wsmp</span></span> | <span data-ttu-id="bd2c6-161">Tipos de bloco opcionais que contêm as informações de loop para o arquivo ADPCM.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="bd2c6-162">Quando você usa o ADPCM em XAudio2, os valores contidos nas partes smpl ou wsmp são usados para preencher os membros **LoopBeginLoopLength** e **LoopCount** da estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="bd2c6-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="bd2c6-163">No Xbox 360, você precisa trocar os dados carregados de uma parte smpl para considerar a diferença de endian entre o Windows e o Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="bd2c6-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bd2c6-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd2c6-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd2c6-165">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="bd2c6-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
