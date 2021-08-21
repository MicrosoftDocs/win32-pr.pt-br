---
description: Este tópico descreve como implementar a busca em um filtro de origem DirectShow Microsoft. Ele usa o exemplo de Filtro de Bola como o ponto de partida e descreve o código adicional necessário para dar suporte à busca nesse filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Suporte à busca em um filtro de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c52ff4bde3ea75b156e5521af9825b0902df38f0d0c6bc23cc7be99c37a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072350"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Suporte à busca em um filtro de origem

Este tópico descreve como implementar a busca em um filtro de origem DirectShow Microsoft. Ele usa o [exemplo de Filtro de](ball-filter-sample.md) Bola como o ponto de partida e descreve o código adicional necessário para dar suporte à busca nesse filtro.

O [exemplo de Filtro de](ball-filter-sample.md) Bola é um filtro de origem que cria uma bola animada. Este artigo descreve como adicionar funcionalidades de busca a esse filtro. Depois de adicionar essa funcionalidade, você pode renderizar o filtro em GraphEdit e controlar a bola arrastando o controle deslizante GraphEdit.

Este tópico contém as seguintes seções:

-   [Visão geral da busca em DirectShow](#overview-of-seeking-in-directshow)
-   [Visão geral rápida do filtro de bola](#quick-overview-of-the-ball-filter)
-   [Modificando o filtro de bola para busca](#modifying-the-ball-filter-for-seeking)
-   [Limitações da classe CSourceSeeking](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Visão geral da busca em DirectShow

Um aplicativo busca o grafo de filtro chamando um [**método IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) no Gerenciador Graph Filtro. O Gerenciador Graph Filtro distribui a chamada a todos os renderdores no grafo. Cada renderdor envia a chamada upstream, por meio do pino de saída do próximo filtro upstream. A chamada percorre o upstream até atingir um filtro que pode executar o comando seek, normalmente um filtro de origem ou um filtro de analisador. Em geral, o filtro que origina os carimbos de data/hora também lida com a busca.

Um filtro responde a um comando seek da seguinte forma:

1.  O filtro libera o grafo. Isso limpa todos os dados desleistidos do grafo, o que melhora a capacidade de resposta. Caso contrário, exemplos que foram armazenados em buffer antes do comando seek podem ser entregues.
2.  O filtro chama [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) para informar filtros downstream da nova hora de parada, hora de início e taxa de reprodução.
3.  Em seguida, o filtro define o sinalizador de descontinuidade no primeiro exemplo após o comando seek.

Os carimbos de data/hora começam de zero após qualquer comando de busca (incluindo alterações de taxa).

## <a name="quick-overview-of-the-ball-filter"></a>Visão geral rápida do filtro de bola

O filtro Bola é uma fonte de push, o que significa que ele usa um thread de trabalho para entregar amostras downstream, em vez de uma fonte de pull, que aguarda passivamente um filtro downstream para solicitar exemplos. O filtro Ball é criado com base na [**classe CSource**](csource.md) e seu pino de saída é criado com base na [**classe CSourceStream.**](csourcestream.md) A **classe CSourceStream** cria o thread de trabalho que orienta o fluxo de dados. Esse thread entra em um loop que obtém exemplos do alocador, preenche-os com dados e os entrega downstream.

A maior parte da ação [**em CSourceStream**](csourcestream.md) ocorre no [**método CSourceStream::FillBuffer,**](csourcestream-fillbuffer.md) que a classe derivada implementa. O argumento para esse método é um ponteiro para o exemplo a ser entregue. A implementação do filtro Ball de **FillBuffer** recupera o endereço do buffer de exemplo e desenha diretamente para o buffer definindo valores de pixel individuais. (O desenho é feito por uma classe auxiliar, CBall, para que você possa ignorar os detalhes sobre profundidades de bits, paletas e assim por diante.)

## <a name="modifying-the-ball-filter-for-seeking"></a>Modificando o filtro de bola para busca

Para tornar o filtro De bola acessível, use a [**classe CSourceSeeking,**](csourceseeking.md) que foi projetada para implementar a busca em filtros com um pino de saída. Adicione a **classe CSourceSeeking** à lista de herança da classe CBallStream:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Além disso, você precisará adicionar um inicializador para [**CSourceSeeking**](csourceseeking.md) ao construtor CBallStream:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Essa instrução chama o construtor base para [**CSourceSeeking.**](csourceseeking.md) Os parâmetros são um nome, um ponteiro para o pin de propriedade, um valor **HRESULT** e o endereço de um objeto de seção crítico. O nome é usado apenas para depuração e a macro [**NAME**](name.md) é compilada em uma cadeia de caracteres vazia em builds de varejo. O pino herda diretamente **CSourceSeeking,** portanto, o segundo parâmetro é um ponteiro para si mesmo, sendo definido como [**um ponteiro IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) O **valor HRESULT** é ignorado na versão atual das classes base; ele permanece para compatibilidade com versões anteriores. A seção crítica protege dados compartilhados, como a hora de início atual, a hora de parada e a taxa de reprodução.

Adicione a seguinte instrução dentro do construtor [**CSourceSeeking:**](csourceseeking.md)


```C++
m_rtStop = 60 * UNITS;
```



A *\_ variável m rtStop* especifica a hora de parada. Por padrão, o valor \_ é I64 MAX/2, que é de aproximadamente \_ 14.600 anos. A instrução anterior o define como um 60 segundos mais conservadora.

Duas variáveis de membro adicionais devem ser adicionadas ao CBallStream:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Após cada comando de busca, o filtro deve definir o sinalizador de descontinuidade no próximo exemplo chamando [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity). A *\_ variável m bDiscontinuity* acompanhará isso. A *\_ variável m rtBallPosition* especificará a posição da bola dentro do quadro de vídeo. O filtro De bola original calcula a posição do tempo de fluxo, mas o tempo de fluxo é redefinido como zero após cada comando de busca. Em um fluxo que pode ser buscado, a posição absoluta é independente do tempo de fluxo.

### <a name="queryinterface"></a>QueryInterface

A [**classe CSourceSeeking**](csourceseeking.md) implementa a interface [**IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Para expor essa interface aos clientes, substitua o [**método NonDeltingQueryInterface:**](cunknown-nondelegatingqueryinterface.md)


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



O método é chamado de "NonDelting" devido à maneira como as classes base DirectShow suportam Component Object Model agregação (COM). Para obter mais informações, consulte o tópico "Como implementar IUnknown" no SDK do DirectShow.

### <a name="seeking-methods"></a>Métodos de busca

A [**classe CSourceSeeking**](csourceseeking.md) mantém várias variáveis de membro relacionadas à busca.



| Variável          | Descrição   | Valor padrão  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | Hora de início    | Zero           |
| *m \_ rtStop*       | Hora de parada     | \_I64 \_ MAX /2 |
| *m \_ dRateSeeking* | Taxa de reprodução | 1.0            |



 

A implementação [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) atualiza os horários de início e de parada e, em seguida, chama dois métodos virtuais puros na classe derivada, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) e [**CSourceSeeking::ChangeStop.**](csourceseeking-changestop.md) A implementação de [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) é semelhante: ele atualiza a taxa de reprodução e, em seguida, chama o método virtual puro [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md). Em cada um desses métodos virtuais, o pino deve fazer o seguinte:

1.  Chame [**IPin::BeginFlush para**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) iniciar a liberação de dados.
2.  Interromper o thread de streaming.
3.  Chame [**IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)
4.  Reinicie o thread de streaming.
5.  Chame [**IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
6.  Definir o sinalizador de descontinuidade no próximo exemplo.

A ordem dessas etapas é crucial, porque o thread de streaming pode ser bloqueado enquanto aguarda para entregar um exemplo ou obter um novo exemplo. O [**método BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garante que o thread de streaming não seja bloqueado e, portanto, não fará deadlock na etapa 2. A [**chamada EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa os filtros downstream para esperar novos exemplos, portanto, eles não os rejeitam quando o thread é iniciado novamente na etapa 4.

O seguinte método privado executa as etapas 1 a 4:


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



Quando o thread de streaming é iniciado novamente, ele chama o [**método CSourceStream::OnThreadStartPlay.**](csourcestream-onthreadstartplay.md) Substitua esse método para executar as etapas 5 e 6:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



No método [**ChangeStart,**](csourceseeking-changestart.md) de definido o tempo de fluxo como zero e a posição da bola para a nova hora de início. Em seguida, chame CBallStream::UpdateFromSeek:


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



No método [**ChangeStop,**](csourceseeking-changestop.md) chame CBallStream::UpdateFromSeek se o novo tempo de parada for menor que a posição atual. Caso contrário, o tempo de parada ainda está no futuro, portanto, não há necessidade de liberar o grafo.


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



Para alterações de taxa, o método [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) define *m \_ dRateSeeking* para a nova taxa (descartando o valor antigo) antes de chamar [**ChangeRate**](csourceseeking-changerate.md). Infelizmente, se o chamador tiver dado uma taxa inválida , por exemplo, menor que zero, será muito tarde quando **ChangeRate** for chamado. Uma solução é substituir **SetRate e** verificar se há taxas válidas:


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



### <a name="drawing-in-the-buffer"></a>Desenhando no buffer

Aqui está a versão modificada [**de CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), a rotina que desenha a bola em cada quadro:


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



As principais diferenças entre essa versão e a original são as seguintes:

-   Conforme mencionado anteriormente, a *variável m \_ rtBallPosition* é usada para definir a posição da bola, em vez da hora do fluxo.
-   Depois de manter a seção crítica, o método verifica se a posição atual excede o tempo de parada. Em caso afirmatório, ele retorna **S \_ FALSE,** que sinaliza a classe base para parar de enviar dados e entregar uma notificação de fim de fluxo.
-   Os carimbos de data/hora são divididos pela taxa atual.
-   Se *m \_ bDiscontinuity* for **TRUE,** o método define o sinalizador de descontinuidade no exemplo.

Há outra diferença secundária. Como a versão original depende de ter exatamente um buffer, ela preenche todo o buffer com zeros uma vez, quando o streaming começa. Depois disso, ele apenas apaga a bola de sua posição anterior. No entanto, essa otimização revela um pequeno bug no filtro Bola. Quando o [**método CBaseOutputPin::D eputaçãoAllocator**](cbaseoutputpin-decideallocator.md) chama [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), ele define o sinalizador somente leitura como **FALSE.** Como resultado, o filtro downstream é livre para gravação no buffer. Uma solução é substituir **DecideAllocator** para definir o sinalizador somente leitura como **TRUE.** Para simplificar, no entanto, a nova versão simplesmente remove completamente a otimização. Em vez disso, essa versão preenche o buffer com zeros a cada vez.

### <a name="miscellaneous-changes"></a>Alterações diversas

Na nova versão, essas duas linhas são removidas do construtor CBall:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



O filtro Bola original usa esses valores para adicionar alguma aleatoriedade à posição inicial da bola. Para nossos objetivos, queremos que a bola seja determinística. Além disso, algumas variáveis foram alteradas de [**objetos CRefTime**](creftime.md) para [**variáveis REFERENCE \_ TIME.**](reference-time.md) (A **classe CRefTime** é um wrapper fino para um **valor REFERENCE \_ TIME.)** Por fim, a implementação de [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) foi ligeiramente modificada; você pode consultar o código-fonte para obter detalhes.

## <a name="limitations-of-the-csourceseeking-class"></a>Limitações da classe CSourceSeeking

A [**classe CSourceSeeking**](csourceseeking.md) não se trata de filtros com vários pinos de saída, devido a problemas com comunicação entre pinos. Por exemplo, imagine um filtro de analisador que recebe um fluxo intercalado de áudio e vídeo, divide o fluxo em seus componentes de áudio e vídeo e entrega vídeo de um pino de saída e áudio de outro. Ambos os pinos de saída receberão cada comando de busca, mas o filtro deve buscar apenas uma vez por comando de busca. A solução é designar um dos pinos para controlar a busca e ignorar os comandos de busca recebidos pelo outro pin.

No entanto, após o comando seek, ambos os pinos devem liberar dados. Para complicar ainda mais, o comando seek acontece no thread do aplicativo, não no thread de streaming. Portanto, você deve certificar-se de que nenhum pin está bloqueado e aguardando uma chamada [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) retornar ou isso pode causar um deadlock. Para obter mais informações sobre a liberação thread-safe em pinos, consulte [Threads e seções críticas](threads-and-critical-sections.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 



