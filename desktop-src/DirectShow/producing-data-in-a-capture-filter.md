---
description: Este tópico descreve como um filtro de captura personalizado do DirectShow deve gerar dados de saída.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Produzindo dados em um filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919950"
---
# <a name="producing-data-in-a-capture-filter"></a>Produzindo dados em um filtro de captura

Este tópico descreve como um filtro de captura personalizado do DirectShow deve gerar dados de saída.

## <a name="filter-state-changes"></a>Filtrar alterações de estado

Um filtro de captura deve produzir dados somente quando o filtro está em execução. Não envie dados de seus PINs quando o filtro for pausado. Além disso, retornar **VFW \_ S não consegue se \_ \_ Marcar** do método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) quando o filtro é pausado. Esse valor de retorno informa ao Gerenciador do grafo de filtro que ele não deve esperar por nenhum dado do filtro enquanto o filtro está em pausa. Para obter mais informações, consulte [Filtrar Estados](filter-states.md).

O código a seguir mostra como implementar o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>Controlando fluxos individuais

Os Pins de saída de um filtro de captura devem dar suporte à interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , para que um aplicativo possa ativar ou desativar cada PIN individualmente. Por exemplo, um aplicativo pode ser visualizado sem capturar e, em seguida, alternar para o modo de captura sem recriar o grafo de filtro. Você pode usar a classe [**CBaseStreamControl**](cbasestreamcontrol.md) para implementar essa interface.

## <a name="time-stamps"></a>Carimbos de Data/Hora

Quando o filtro captura um exemplo, o carimbo de data/hora é o exemplo com a hora atual do fluxo. A hora de término é a hora de início mais a duração. Por exemplo, se o filtro estiver capturando em dez amostras por segundo, e a hora do fluxo for de 200 milhões unidades quando o filtro capturar o exemplo, os carimbos de data/hora deverão ser 200 milhões e 201 milhões. (Há 10 milhões unidades por segundo.)

Para calcular a hora do fluxo, chame o método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obter o tempo de referência atual e, em seguida, substract a hora de início original. Como alternativa, chame o método [**CBaseFilter:: streamtime**](cbasefilter-streamtime.md) , que executa o mesmo cálculo. Para definir o carimbo de data/hora em um exemplo, chame o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

No entanto, se o filtro tiver um PIN de visualização, os exemplos do pino de visualização não deverão ter carimbos de data/hora. O motivo é que os exemplos sempre alcançarão um pouco o processador após o momento da captura. Se os exemplos estiverem com carimbo de data/hora, o renderizador os tratará como atrasado e poderá tentar se acumular descartando amostras. (Para obter mais informações, consulte [filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md).) Observe que a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) exige que o PIN acompanhe os tempos de amostragem. Para um PIN de visualização, talvez seja necessário modificar a implementação para que ela não dependa de carimbos de data/hora.

Os carimbos de data/hora sempre devem aumentar de um exemplo para o próximo. Isso é verdadeiro mesmo quando o filtro é pausado. Se o filtro for executado, pausar e executar novamente, o primeiro exemplo após a pausa deverá ter um carimbo de data/hora maior do que o último exemplo antes da pausa.

Dependendo dos dados que você está capturando, pode ser apropriado definir o tempo de mídia nos exemplos.

Para obter mais informações, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Gravando filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



