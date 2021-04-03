---
description: Este tópico descreve como implementar a busca em um filtro de origem do Microsoft DirectShow. Ele usa o exemplo de filtro de bola como o ponto de partida e descreve o código adicional necessário para dar suporte à busca nesse filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Dando suporte à busca em um filtro de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837140"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="7a7b0-104">Dando suporte à busca em um filtro de origem</span><span class="sxs-lookup"><span data-stu-id="7a7b0-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="7a7b0-105">Este tópico descreve como implementar a busca em um filtro de origem do Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="7a7b0-106">Ele usa o exemplo de [filtro de bola](ball-filter-sample.md) como o ponto de partida e descreve o código adicional necessário para dar suporte à busca nesse filtro.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="7a7b0-107">O exemplo de [filtro de bola](ball-filter-sample.md) é um filtro de origem que cria uma bola de saltação animada.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="7a7b0-108">Este artigo descreve como adicionar a funcionalidade de busca a esse filtro.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="7a7b0-109">Depois de adicionar essa funcionalidade, você pode renderizar o filtro em GraphEdit e controlar a bola arrastando o controle deslizante GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="7a7b0-110">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="7a7b0-111">Visão geral de busca no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a7b0-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="7a7b0-112">Visão geral rápida do filtro de bola</span><span class="sxs-lookup"><span data-stu-id="7a7b0-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="7a7b0-113">Modificando o filtro de bola para busca</span><span class="sxs-lookup"><span data-stu-id="7a7b0-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="7a7b0-114">Limitações da classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="7a7b0-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="7a7b0-115">Visão geral de busca no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a7b0-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="7a7b0-116">Um aplicativo busca o grafo de filtro chamando um método [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="7a7b0-117">Em seguida, o Gerenciador do grafo de filtro distribui a chamada para todos os renderizadores no grafo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="7a7b0-118">Cada renderizador envia o upstream de chamada por meio do pino de saída do próximo filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="7a7b0-119">A chamada viaja para upstream até atingir um filtro que possa executar o comando Seek, normalmente um filtro de origem ou um filtro do analisador.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="7a7b0-120">Em geral, o filtro que origina os carimbos de data/hora também lida com a busca.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="7a7b0-121">Um filtro responde a um comando de busca da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="7a7b0-122">O filtro libera o grafo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-122">The filter flushes the graph.</span></span> <span data-ttu-id="7a7b0-123">Isso limpa os dados obsoletos do grafo, o que melhora a capacidade de resposta.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="7a7b0-124">Caso contrário, os exemplos que foram armazenados em buffer antes do comando de busca podem ser entregues.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="7a7b0-125">O filtro chama [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) para informar os filtros de downstream da nova hora de parada, hora de início e taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="7a7b0-126">Em seguida, o filtro define o sinalizador de descontinuidade no primeiro exemplo após o comando Seek.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="7a7b0-127">Os carimbos de data/hora começam do zero após qualquer comando de busca (incluindo alterações de taxa).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="7a7b0-128">Visão geral rápida do filtro de bola</span><span class="sxs-lookup"><span data-stu-id="7a7b0-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="7a7b0-129">O filtro de bola é uma fonte Push, o que significa que ele usa um thread de trabalho para entregar amostras downstream, em vez de uma fonte pull, que espera passivamente um filtro downstream para solicitar amostras.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="7a7b0-130">O filtro de bola é criado a partir da classe [**CSource**](csource.md) e seu pino de saída é criado a partir da classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7b0-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="7a7b0-131">A classe **CSourceStream** cria o thread de trabalho que orienta o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="7a7b0-132">Esse thread entra em um loop que obtém exemplos do alocador, preenche-os com os dados e os entrega por downstream.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="7a7b0-133">A maior parte da ação em [**CSourceStream**](csourcestream.md) acontece no método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que a classe derivada implementa.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="7a7b0-134">O argumento para esse método é um ponteiro para o exemplo a ser entregue.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="7a7b0-135">A implementação do filtro de bolas do **FillBuffer** recupera o endereço do buffer de exemplo e desenha diretamente para o buffer, definindo valores de pixel individuais.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="7a7b0-136">(O desenho é feito por uma classe auxiliar, CBall, para que você possa ignorar os detalhes em relação a profundidades de bits, paletas e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="7a7b0-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="7a7b0-137">Modificando o filtro de bola para busca</span><span class="sxs-lookup"><span data-stu-id="7a7b0-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="7a7b0-138">Para tornar o filtro de bola pesquisável, use a classe [**CSourceSeeking**](csourceseeking.md) , que foi projetada para implementar a busca em filtros com um PIN de saída.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="7a7b0-139">Adicione a classe **CSourceSeeking** à lista de herança para a classe CBallStream:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="7a7b0-140">Além disso, será necessário adicionar um inicializador para [**CSourceSeeking**](csourceseeking.md) ao Construtor CBallStream:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="7a7b0-141">Essa instrução chama o construtor base para [**CSourceSeeking**](csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="7a7b0-142">Os parâmetros são um nome, um ponteiro para o PIN proprietário, um valor **HRESULT** e o endereço de um objeto de seção crítica.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="7a7b0-143">O nome é usado somente para depuração e a macro de [**nome**](name.md) compila para uma cadeia de caracteres vazia em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="7a7b0-144">O PIN herda diretamente **CSourceSeeking**, portanto, o segundo parâmetro é um ponteiro para si mesmo, convertê-lo em um ponteiro [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="7a7b0-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="7a7b0-145">O valor **HRESULT** é ignorado na versão atual das classes base; Ele permanece para compatibilidade com as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="7a7b0-146">A seção crítica protege dados compartilhados, como a hora de início, a hora de parada e a taxa de reprodução atuais.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="7a7b0-147">Adicione a seguinte instrução dentro do construtor [**CSourceSeeking**](csourceseeking.md) :</span><span class="sxs-lookup"><span data-stu-id="7a7b0-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="7a7b0-148">A variável *m \_ rtStop* especifica a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="7a7b0-149">Por padrão, o valor é \_ i64 \_ Max/2, que é de aproximadamente 14.600 anos.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="7a7b0-150">A instrução anterior a define como um número mais conservador de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="7a7b0-151">Duas variáveis de membro adicionais devem ser adicionadas a CBallStream:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="7a7b0-152">Após cada comando Seek, o filtro deve definir o sinalizador de discontinuidade no próximo exemplo chamando [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="7a7b0-153">A variável *m \_ bDiscontinuity* manterá o controle disso.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="7a7b0-154">A variável *m \_ rtBallPosition* especificará a posição da bola dentro do quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="7a7b0-155">O filtro de bola original calcula a posição a partir do tempo do fluxo, mas o tempo de fluxo é redefinido para zero após cada comando de busca.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="7a7b0-156">Em um fluxo pesquisável, a posição absoluta é independente do tempo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="7a7b0-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="7a7b0-157">QueryInterface</span></span>

<span data-ttu-id="7a7b0-158">A classe [**CSourceSeeking**](csourceseeking.md) implementa a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="7a7b0-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="7a7b0-159">Para expor essa interface aos clientes, substitua o método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :</span><span class="sxs-lookup"><span data-stu-id="7a7b0-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="7a7b0-160">O método é chamado de "nondelegating" devido à maneira como as classes base do DirectShow dão suporte à agregação de Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="7a7b0-161">Para obter mais informações, consulte o tópico "How to implement IUnknown" no SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="7a7b0-162">Métodos de busca</span><span class="sxs-lookup"><span data-stu-id="7a7b0-162">Seeking Methods</span></span>

<span data-ttu-id="7a7b0-163">A classe [**CSourceSeeking**](csourceseeking.md) mantém várias variáveis de membro relacionadas à busca.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="7a7b0-164">Variável</span><span class="sxs-lookup"><span data-stu-id="7a7b0-164">Variable</span></span>          | <span data-ttu-id="7a7b0-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a7b0-165">Description</span></span>   | <span data-ttu-id="7a7b0-166">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7a7b0-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="7a7b0-167">*\_rtStart m*</span><span class="sxs-lookup"><span data-stu-id="7a7b0-167">*m\_rtStart*</span></span>      | <span data-ttu-id="7a7b0-168">Hora de início</span><span class="sxs-lookup"><span data-stu-id="7a7b0-168">Start time</span></span>    | <span data-ttu-id="7a7b0-169">Zero</span><span class="sxs-lookup"><span data-stu-id="7a7b0-169">Zero</span></span>           |
| <span data-ttu-id="7a7b0-170">*\_rtStop m*</span><span class="sxs-lookup"><span data-stu-id="7a7b0-170">*m\_rtStop*</span></span>       | <span data-ttu-id="7a7b0-171">Hora de parada</span><span class="sxs-lookup"><span data-stu-id="7a7b0-171">Stop time</span></span>     | <span data-ttu-id="7a7b0-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="7a7b0-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="7a7b0-173">*\_dRateSeeking m*</span><span class="sxs-lookup"><span data-stu-id="7a7b0-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="7a7b0-174">Taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="7a7b0-174">Playback rate</span></span> | <span data-ttu-id="7a7b0-175">1.0</span><span class="sxs-lookup"><span data-stu-id="7a7b0-175">1.0</span></span>            |



 

<span data-ttu-id="7a7b0-176">A implementação de [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) atualiza os horários de início e de parada e, em seguida, chama dois métodos virtuais puros na classe derivada, [**CSourceSeeking:: altere**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="7a7b0-177">A implementação de [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) é semelhante: atualiza a taxa de reprodução e, em seguida, chama o método virtual puro [**CSourceSeeking:: disqueteira**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="7a7b0-178">Em cada um desses métodos virtuais, o PIN deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="7a7b0-179">Chame [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) para iniciar a liberação de dados.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="7a7b0-180">Pare o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="7a7b0-181">Chamar [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="7a7b0-182">Reinicie o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="7a7b0-183">Chame [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="7a7b0-184">Defina o sinalizador de descontinuidade no próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="7a7b0-185">A ordem dessas etapas é crucial, pois o thread de streaming pode ser bloqueado enquanto aguarda para entregar um exemplo ou obter um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="7a7b0-186">O método [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garante que o thread de streaming não seja bloqueado e, portanto, não causará deadlock na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="7a7b0-187">A chamada [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa os filtros downstream para esperar novos exemplos e, portanto, eles não os rejeitam quando o thread é iniciado novamente na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="7a7b0-188">O método particular a seguir executa as etapas 1 a 4:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="7a7b0-189">Quando o thread de streaming inicia novamente, ele chama o método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7b0-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="7a7b0-190">Substitua esse método para executar as etapas 5 e 6:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="7a7b0-191">No método [**altere**](csourceseeking-changestart.md) , defina o tempo de fluxo como zero e a posição da bola para a nova hora de início.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="7a7b0-192">Em seguida, chame CBallStream:: UpdateFromSeek:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="7a7b0-193">No método [**ChangeStop**](csourceseeking-changestop.md) , chame CBallStream:: UpdateFromSeek se a nova hora de parada for menor que a posição atual.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="7a7b0-194">Caso contrário, o tempo de parada ainda estará no futuro, portanto, não há necessidade de liberar o grafo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="7a7b0-195">Para alterações de taxa, o método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) define *m \_ dRateSeeking* como a nova taxa (descartando o valor antigo) antes de chamar o [**alterador**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="7a7b0-196">Infelizmente, se o chamador forneceu uma taxa inválida — por exemplo, menor que zero, é muito tarde que o **Peralterador** de tempo é chamado.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="7a7b0-197">Uma solução é substituir **SetRate** e verificar se há taxas válidas:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="7a7b0-198">Desenho no buffer</span><span class="sxs-lookup"><span data-stu-id="7a7b0-198">Drawing in the Buffer</span></span>

<span data-ttu-id="7a7b0-199">Aqui está a versão modificada de [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md), a rotina que desenha a bola em cada quadro:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="7a7b0-200">As principais diferenças entre essa versão e a original são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="7a7b0-201">Como mencionado anteriormente, a variável *m \_ rtBallPosition* é usada para definir a posição da bola, em vez da hora do fluxo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="7a7b0-202">Depois de conter a seção crítica, o método verifica se a posição atual excede a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="7a7b0-203">Nesse caso, ele retorna **S \_ false**, que sinaliza a classe base para parar de enviar dados e fornecer uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="7a7b0-204">Os carimbos de data/hora são divididos pela taxa atual.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="7a7b0-205">Se *m \_ BDiscontinuity* for **true**, o método definirá o sinalizador de descontinuidade no exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="7a7b0-206">Há outra diferença secundária.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-206">There is another minor difference.</span></span> <span data-ttu-id="7a7b0-207">Como a versão original depende de ter exatamente um buffer, ela preenche todo o buffer com zeros uma vez, quando o streaming começa.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="7a7b0-208">Depois disso, ele apenas apaga a bola de sua posição anterior.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="7a7b0-209">No entanto, essa otimização revela um pequeno bug no filtro de bola.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="7a7b0-210">Quando o método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), ele define o sinalizador somente leitura como **falso**.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="7a7b0-211">Como resultado, o filtro downstream é livre para gravar no buffer.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="7a7b0-212">Uma solução é substituir **DecideAllocator** para que ele defina o sinalizador somente leitura como **true**.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="7a7b0-213">Para simplificar, no entanto, a nova versão simplesmente remove totalmente a otimização.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="7a7b0-214">Em vez disso, essa versão preenche o buffer com zeros a cada vez.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="7a7b0-215">Alterações diversas</span><span class="sxs-lookup"><span data-stu-id="7a7b0-215">Miscellaneous Changes</span></span>

<span data-ttu-id="7a7b0-216">Na nova versão, essas duas linhas são removidas do Construtor CBall:</span><span class="sxs-lookup"><span data-stu-id="7a7b0-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="7a7b0-217">O filtro de bola original usa esses valores para adicionar uma aleatoriedade à posição inicial da bola.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="7a7b0-218">Para nossos objetivos, queremos que a bola seja determinística.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="7a7b0-219">Além disso, algumas variáveis foram alteradas de objetos [**CRefTime**](creftime.md) para variáveis de [**\_ tempo de referência**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="7a7b0-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="7a7b0-220">(A classe **CRefTime** é um wrapper fino para um valor de **\_ tempo de referência** .) Por fim, a implementação de [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) foi modificada ligeiramente; Você pode consultar o código-fonte para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="7a7b0-221">Limitações da classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="7a7b0-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="7a7b0-222">A classe [**CSourceSeeking**](csourceseeking.md) não é destinada a filtros com vários Pins de saída, devido a problemas com comunicação entre pinos.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="7a7b0-223">Por exemplo, imagine um filtro do analisador que recebe um fluxo de vídeo de áudio Intercalado, divide o fluxo em seus componentes de áudio e vídeo e entrega vídeo de um PIN de saída e áudio de outro.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="7a7b0-224">Ambos os Pins de saída receberão todos os comandos de busca, mas o filtro deverá procurar apenas uma vez por comando de busca.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="7a7b0-225">A solução é designar um dos Pins para controlar a busca e ignorar os comandos de busca recebidos pelo outro PIN.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="7a7b0-226">Depois do comando Seek, no entanto, ambos os Pins devem liberar dados.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="7a7b0-227">Para complicar ainda mais as coisas, o comando Seek ocorre no thread do aplicativo, não no thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="7a7b0-228">Portanto, você deve certificar-se de que nenhum PIN está bloqueado e aguardando uma chamada [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) para Return ou pode causar um deadlock.</span><span class="sxs-lookup"><span data-stu-id="7a7b0-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="7a7b0-229">Para obter mais informações sobre liberação thread-safe em Pins, consulte [threads e seções críticas](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="7a7b0-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a7b0-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a7b0-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a7b0-231">Gravando filtros de origem</span><span class="sxs-lookup"><span data-stu-id="7a7b0-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



