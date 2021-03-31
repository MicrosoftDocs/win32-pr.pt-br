---
description: O conjunto de todas as vozes, com seus efeitos contidos e suas interconexões, é conhecido como grafo de processamento de áudio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Grafo de áudio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172044"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="1df7e-103">Grafo de áudio XAudio2</span><span class="sxs-lookup"><span data-stu-id="1df7e-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="1df7e-104">O conjunto de todas as vozes, com seus efeitos contidos e suas interconexões, é conhecido como grafo de processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="1df7e-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="1df7e-105">O grafo usa um conjunto de fluxos de áudio do cliente como entrada, processa-os e entrega o resultado final a um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1df7e-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="1df7e-106">Todo o processamento de áudio ocorre em um thread separado com uma periodicidade definida pelo Quantum do grafo (atualmente, 10 milissegundos no Microsoft Windows e 5 1/3 milissegundos no Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="1df7e-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="1df7e-107">Todos os milissegundos do Quantum, o thread ativa e distribui milissegundos do quantum de dados de áudio por todo o grafo.</span><span class="sxs-lookup"><span data-stu-id="1df7e-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="1df7e-108">Para obter um exemplo de criação de um gráfico de áudio básico, consulte como [compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="1df7e-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="1df7e-109">Um grafo de áudio simples:</span><span class="sxs-lookup"><span data-stu-id="1df7e-109">A simple audio graph:</span></span>

![um grafo de áudio simples](images/xaudio2-audio-graph.png)

<span data-ttu-id="1df7e-111">O cliente pode controlar o estado do grafo dinamicamente enquanto ele está em execução.</span><span class="sxs-lookup"><span data-stu-id="1df7e-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="1df7e-112">As ações de controle podem incluir adição e remoção de entradas e saídas, alteração dos efeitos internos e interconexões, definição de parâmetros nos efeitos, habilitação e desabilitação de partes do grafo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1df7e-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="1df7e-113">Para obter um exemplo de alteração dinâmica de um gráfico de áudio, consulte [como: Adicionar ou remover vozes dinamicamente de um grafo de áudio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="1df7e-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="1df7e-114">Processando o grafo</span><span class="sxs-lookup"><span data-stu-id="1df7e-114">Processing the Graph</span></span>

<span data-ttu-id="1df7e-115">Qualquer chamada de método que afete qualquer objeto no grafo é considerada como efeito uma alteração de estado do grafo.</span><span class="sxs-lookup"><span data-stu-id="1df7e-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="1df7e-116">As alterações de estado do grafo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1df7e-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="1df7e-117">Criando e destruindo vozes</span><span class="sxs-lookup"><span data-stu-id="1df7e-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="1df7e-118">Iniciando ou parando vozes</span><span class="sxs-lookup"><span data-stu-id="1df7e-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="1df7e-119">Alterando os destinos de uma voz</span><span class="sxs-lookup"><span data-stu-id="1df7e-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="1df7e-120">Modificando cadeias de efeito</span><span class="sxs-lookup"><span data-stu-id="1df7e-120">Modifying effect chains</span></span>
-   <span data-ttu-id="1df7e-121">Habilitando ou desabilitando efeitos</span><span class="sxs-lookup"><span data-stu-id="1df7e-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="1df7e-122">Definindo parâmetros nos efeitos ou na SRCs interna, nos filtros, nos volumes e nos mixers</span><span class="sxs-lookup"><span data-stu-id="1df7e-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="1df7e-123">Qualquer conjunto de alterações de estado do grafo pode ser combinado e executado como uma transação atômica.</span><span class="sxs-lookup"><span data-stu-id="1df7e-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="1df7e-124">Essas operações atômicas são conhecidas como conjuntos de operações.</span><span class="sxs-lookup"><span data-stu-id="1df7e-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="1df7e-125">Eles são discutidos na visão geral dos [conjuntos de operações do XAudio2](xaudio2-operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="1df7e-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="1df7e-126">Representação de dados interna</span><span class="sxs-lookup"><span data-stu-id="1df7e-126">Internal Data Representation</span></span>

<span data-ttu-id="1df7e-127">Os dados de áudio no grafo XAudio2 são sempre armazenados e processados no formato PCM de ponto flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1df7e-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="1df7e-128">No entanto, a contagem de canais e a taxa de amostragem podem variar dentro do grafo.</span><span class="sxs-lookup"><span data-stu-id="1df7e-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="1df7e-129">O formato no qual uma determinada voz processa o áudio é determinado pelo tipo de voz e pelos parâmetros usados para criar a voz.</span><span class="sxs-lookup"><span data-stu-id="1df7e-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="1df7e-130">Tipo de voz</span><span class="sxs-lookup"><span data-stu-id="1df7e-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="1df7e-131">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1df7e-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1df7e-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="1df7e-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="1df7e-133">A contagem de canais e a taxa de amostra das vozes para as quais a voz de origem envia áudio.</span><span class="sxs-lookup"><span data-stu-id="1df7e-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="1df7e-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="1df7e-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="1df7e-135">Os argumentos *InputChannels* e *InputSampleRate* usados para criar a voz de submix/mestre.</span><span class="sxs-lookup"><span data-stu-id="1df7e-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="1df7e-136">Conversão de formato</span><span class="sxs-lookup"><span data-stu-id="1df7e-136">Format Conversion</span></span>

<span data-ttu-id="1df7e-137">XAudio2 lida com qualquer taxa de amostragem ou conversões de canal que são necessárias à medida que o áudio viaja de uma voz para outra, com as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="1df7e-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="1df7e-138">Todas as vozes de destino de uma determinada voz devem estar em execução com a mesma taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="1df7e-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="1df7e-139">Os efeitos em uma cadeia de efeito podem alterar a contagem de canais do áudio, mas não sua taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="1df7e-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="1df7e-140">A contagem de canais de saída de uma cadeia de efeitos deve corresponder à das vozes às quais ele envia</span><span class="sxs-lookup"><span data-stu-id="1df7e-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="1df7e-141">Nenhuma alteração dinâmica de grafo pode ser feita, o que quebraria as regras acima</span><span class="sxs-lookup"><span data-stu-id="1df7e-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="1df7e-142">No lado da entrada, as vozes de origem podem ler dados em qualquer formato PCM válido ou em qualquer um dos formatos compactados com suporte do XAudio2.</span><span class="sxs-lookup"><span data-stu-id="1df7e-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="1df7e-143">Se os dados de entrada forem compactados, eles serão decodificados para o PCM de ponto flutuante antes de qualquer processamento adicional ser feito.</span><span class="sxs-lookup"><span data-stu-id="1df7e-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="1df7e-144">No lado da saída, as vozes de dominar só podem produzir dados PCM.</span><span class="sxs-lookup"><span data-stu-id="1df7e-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="1df7e-145">Esses dados sempre atenderão às mesmas restrições descritas acima para dados de entrada PCM.</span><span class="sxs-lookup"><span data-stu-id="1df7e-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1df7e-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1df7e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df7e-147">Gráficos de áudio</span><span class="sxs-lookup"><span data-stu-id="1df7e-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="1df7e-148">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="1df7e-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="1df7e-149">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="1df7e-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="1df7e-150">Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio</span><span class="sxs-lookup"><span data-stu-id="1df7e-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="1df7e-151">Como: Usar vozes de submixagem</span><span class="sxs-lookup"><span data-stu-id="1df7e-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="1df7e-152">Como: Criar uma cadeia de efeitos</span><span class="sxs-lookup"><span data-stu-id="1df7e-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



