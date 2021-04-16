---
description: 'Há três tipos de objetos de voz XAudio2: origem, submix e vozes de mestre.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Vozes XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782608"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="97213-103">Vozes XAudio2</span><span class="sxs-lookup"><span data-stu-id="97213-103">XAudio2 Voices</span></span>

<span data-ttu-id="97213-104">Há três tipos de objetos de voz XAudio2: *origem*, *submix* e vozes de *mestre* .</span><span class="sxs-lookup"><span data-stu-id="97213-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="97213-105">As vozes de origem operam em dados de áudio fornecidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="97213-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="97213-106">As vozes de origem e submixagem enviam sua saída para uma ou mais vozes de submixagem ou masterização.</span><span class="sxs-lookup"><span data-stu-id="97213-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="97213-107">As vozes de submixagem e masterização combinam o áudio de todas as vozes que as alimentam e operam no resultado.</span><span class="sxs-lookup"><span data-stu-id="97213-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="97213-108">As vozes de masterização gravam dados de áudio em um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="97213-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="97213-109">Ações executadas por todas as vozes</span><span class="sxs-lookup"><span data-stu-id="97213-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="97213-110">Todas as vozes executam as seguintes ações na ordem no áudio que viaja por meio deles.</span><span class="sxs-lookup"><span data-stu-id="97213-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="97213-111">Ajuste de volume geral, afetando todos os canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="97213-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="97213-112">Consulte [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="97213-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="97213-113">Uma cadeia especificada pelo cliente opcional de um ou mais efeitos de DSP, como o verbo interno de reverberação ou um efeito de usuário definido pela interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) .</span><span class="sxs-lookup"><span data-stu-id="97213-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="97213-114">Consulte [efeitos de áudio XAudio2](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="97213-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="97213-115">Ajuste do volume de saída por canal.</span><span class="sxs-lookup"><span data-stu-id="97213-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="97213-116">Consulte [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="97213-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="97213-117">Combinação de matriz separada para cada uma das vozes de destino ou para o dispositivo de saída de áudio para dominar as vozes.</span><span class="sxs-lookup"><span data-stu-id="97213-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="97213-118">Essa combinação altera o número de canais no áudio, se necessário.</span><span class="sxs-lookup"><span data-stu-id="97213-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="97213-119">Vozes de origem</span><span class="sxs-lookup"><span data-stu-id="97213-119">Source Voices</span></span>

<span data-ttu-id="97213-120">Use as vozes de origem para enviar dados de áudio para o pipeline de processamento XAudio2.</span><span class="sxs-lookup"><span data-stu-id="97213-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="97213-121">Eles são os pontos de entrada no [grafo de áudio XAudio2](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="97213-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="97213-122">Você deve enviar dados de voz para uma voz de mestre para ser ouvido, seja diretamente ou por meio de vozes submixs intermediárias.</span><span class="sxs-lookup"><span data-stu-id="97213-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="97213-123">Além das ações executadas por todas as vozes, as vozes de origem executam as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="97213-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="97213-124">Se necessário, um decodificador é executado primeiro para converter dados de origem codificados em PCM (modulação de código de pulso).</span><span class="sxs-lookup"><span data-stu-id="97213-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="97213-125">Uma conversão de taxa de amostragem (SRC) de taxa variável converte os dados de áudio de origem da voz na taxa de amostra esperada por suas vozes de destino, se necessário, e também dá suporte a alterações de densidade dinâmica.</span><span class="sxs-lookup"><span data-stu-id="97213-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="97213-126">Um filtro de variável de estado opcional pode ser usado para colorir o som de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="97213-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="97213-127">Consulte [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="97213-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="97213-128">Um filtro opcional pode ser aplicado às saídas da voz.</span><span class="sxs-lookup"><span data-stu-id="97213-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="97213-129">Consulte [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="97213-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="97213-130">Submix vozes</span><span class="sxs-lookup"><span data-stu-id="97213-130">Submix Voices</span></span>

<span data-ttu-id="97213-131">Uma voz submix é usada principalmente para melhorias de desempenho e processamento de efeitos.</span><span class="sxs-lookup"><span data-stu-id="97213-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="97213-132">Você não pode enviar buffers de dados diretamente para vozes submix.</span><span class="sxs-lookup"><span data-stu-id="97213-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="97213-133">Não será audível, a menos que você o envie para uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="97213-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="97213-134">Você pode usar uma voz submix para garantir que um determinado conjunto de dados de voz seja convertido no mesmo formato e tenha uma cadeia de efeitos específica processada no resultado coletivo.</span><span class="sxs-lookup"><span data-stu-id="97213-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="97213-135">Além das ações executadas por todas as vozes, as vozes submix executam as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="97213-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="97213-136">Uma SRC de taxa fixa é executada na saída da voz, se necessário, para converter o áudio para a taxa de amostra esperada por suas vozes de destino.</span><span class="sxs-lookup"><span data-stu-id="97213-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="97213-137">Um filtro de variável de estado opcional pode ser usado para colorir o som de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="97213-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="97213-138">Consulte [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="97213-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="97213-139">Um filtro opcional pode ser aplicado às saídas da voz.</span><span class="sxs-lookup"><span data-stu-id="97213-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="97213-140">Consulte [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="97213-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="97213-141">Vozes de dominar</span><span class="sxs-lookup"><span data-stu-id="97213-141">Mastering Voices</span></span>

<span data-ttu-id="97213-142">Use uma voz de mestre para representar o dispositivo de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="97213-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="97213-143">Você não pode enviar buffers de dados diretamente para as vozes de dominar, mas os dados enviados para outros tipos de vozes devem ir para uma voz de mestre a ser ouvido.</span><span class="sxs-lookup"><span data-stu-id="97213-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="97213-144">Além das ações executadas por todas as vozes, as vozes de dominar executam as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="97213-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="97213-145">Se você criar a voz de mestre com um valor *InputSampleRate* explícito que não tenha suporte do dispositivo de áudio, uma src de taxa fixa será usada para converter a taxa de amostra mais próxima com suporte pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97213-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="97213-146">Recorte o áudio final de saída, se for exigido pelo dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="97213-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97213-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97213-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97213-148">Vozes</span><span class="sxs-lookup"><span data-stu-id="97213-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="97213-149">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="97213-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="97213-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="97213-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="97213-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="97213-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="97213-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="97213-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
