---
description: A classe CSourceSeeking é uma classe abstrata para implementar a busca em filtros de origem com um PIN de saída.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Classe CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767683"
---
# <a name="csourceseeking-class"></a>Classe CSourceSeeking

![hierarquia de classe CSourceSeeking](images/cutil15.png)

A classe **CSourceSeeking** é uma classe abstrata para implementar a busca em filtros de origem com um PIN de saída.

Essa classe dá suporte à interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Ele fornece implementações padrão para todos os métodos **IMediaSeeking** . As variáveis de membro protegidas armazenam a hora de início, a hora de parada e a taxa atual. Por padrão, o único formato de tempo com suporte da classe é o formato de tempo de **\_ \_ mídia \_** (unidades de 100 a nanossegundos). Consulte comentários para obter mais informações.



| Variáveis de membro protegido                                          | Descrição                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_rtDuration m**](csourceseeking-m-rtduration.md)                | Duração do fluxo.                                                                     |
| [**\_rtStart m**](csourceseeking-m-rtstart.md)                      | Hora de início.                                                                                 |
| [**\_rtStop m**](csourceseeking-m-rtstop.md)                        | Hora de parada.                                                                                  |
| [**\_dRateSeeking m**](csourceseeking-m-drateseeking.md)            | Taxa de reprodução.                                                                              |
| [**\_dwSeekingCaps m**](csourceseeking-m-dwseekingcaps.md)          | Buscando recursos.                                                                       |
| [**\_pLock m**](csourceseeking-m-plock.md)                          | Ponteiro para um objeto de seção crítica para bloqueio.                                           |
| Métodos Protegidos                                                   | Descrição                                                                                 |
| [**CSourceSeeking**](csourceseeking-csourceseeking.md)             | Método de construtor.                                                                         |
| Métodos virtuais puros                                                | Descrição                                                                                 |
| [**Trocador**](csourceseeking-changerate.md)                     | Chamado quando a taxa de reprodução é alterada.                                                      |
| [**Altere**](csourceseeking-changestart.md)                   | Chamado quando a posição inicial é alterada.                                                     |
| [**ChangeStop**](csourceseeking-changestop.md)                     | Chamado quando a posição de parada é alterada.                                                      |
| Métodos IMediaSeeking                                               | Descrição                                                                                 |
| [**IsFormatSupported**](csourceseeking-isformatsupported.md)       | Determina se há suporte para um formato de hora especificado.                                    |
| [**QueryPreferredFormat**](csourceseeking-querypreferredformat.md) | Recupera o formato de hora preferencial do objeto.                                               |
| [**SetTimeFormat**](csourceseeking-settimeformat.md)               | Define o formato de hora.                                                                       |
| [**IsUsingTimeFormat**](csourceseeking-isusingtimeformat.md)       | Determina se um formato de hora especificado é o formato em uso no momento.                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | Recupera o formato de hora atual.                                                          |
| [**GetDuration**](csourceseeking-getduration.md)                   | Recupera a duração do fluxo.                                                       |
| [**GetStopPosition**](csourceseeking-getstopposition.md)           | Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. |
| [**GetCurrentPosition**](csourceseeking-getcurrentposition.md)     | Recupera a posição atual, em relação à duração total do fluxo.               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | Recupera todos os recursos de busca do fluxo.                                       |
| [**CheckCapabilities**](csourceseeking-checkcapabilities.md)       | Consulta se o fluxo especificou recursos de busca.                              |
| [**ConvertTimeFormat**](csourceseeking-converttimeformat.md)       | Converte de um formato de tempo para outro.                                                   |
| [**Setpositiones**](csourceseeking-setpositions.md)                 | Define a posição atual e a posição de parada.                                            |
| [**Getpositiones**](csourceseeking-getpositions.md)                 | Recupera a posição atual e a posição de parada.                                       |
| [**GetAvailable**](csourceseeking-getavailable.md)                 | Recupera o intervalo de vezes em que a busca é eficiente.                                 |
| [**SetRate**](csourceseeking-setrate.md)                           | Define a taxa de reprodução.                                                                     |
| [**GetRate**](csourceseeking-getrate.md)                           | Recupera a taxa de reprodução.                                                                |
| [**GetPreroll**](csourceseeking-getpreroll.md)                     | Recupera o tempo de preversão.                                                                 |



 

## <a name="remarks"></a>Comentários

Sempre que a posição inicial, a posição de parada ou a taxa de reprodução é alterada, o objeto **CSourceSeeking** chama um método virtual puro correspondente:

-   Posição inicial: [ **CSourceSeeking:: altere**](csourceseeking-changestart.md)
-   Posição de parada: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)
-   Taxa de reprodução: [ **CSourceSeeking:: disqueteira**](csourceseeking-changerate.md)

A classe derivada deve implementar esses métodos. Após qualquer operação de busca, um filtro deve fazer o seguinte:

1.  Chame o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada downstream.
2.  Pare o thread de trabalho que está entregando dados.
3.  Chame o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.
4.  Reinicie o thread de trabalho.
5.  Chame o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) no pino de entrada.
6.  Defina a propriedade de descontinuidade no primeiro exemplo. Chame o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

A chamada para [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) liberará o thread de trabalho, se o thread estiver bloqueado aguardando para entregar um exemplo.

Na etapa 2, certifique-se de que o thread parou de enviar dados. Dependendo da implementação, talvez seja necessário aguardar a saída do thread ou para que o thread sinalize uma resposta de algum tipo. Se o filtro usar a classe [**CSourceStream**](csourcestream.md) , o método [**CSourceStream:: Stop**](csourcestream-stop.md) bloqueará até que o thread de trabalho responda.

O ideal é que o novo segmento (etapa 5) seja entregue do thread de trabalho. Ele também pode ser feito pelo objeto **CSourceSeeking** , desde que o filtro o Serialize com os exemplos.

O exemplo a seguir mostra uma implementação possível. Ele pressupõe que o pino de saída do filtro de origem é derivado de **CSourceSeeking** e [**CSourceStream**](csourcestream.md). Este exemplo define um método auxiliar, UpdateFromSeek, que executa as etapas 1 4. O método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) é substituído para enviar o novo segmento e para definir um sinalizador que indica a descontinuidade. O thread de trabalho pega esse sinalizador e chama o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a>Dando suporte a formatos de tempo adicionais

Por padrão, essa classe dá suporte à busca apenas em unidades de tempo de referência (tempo de mídia de formato de hora \_ \_ \_ ). Para dar suporte a formatos de tempo adicionais, substitua os métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que lidam com formatos de hora:

-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Além disso, substitua os métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes para executar as conversões necessárias entre os formatos de hora. Depois que o método [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) é chamado, todos os métodos **IMediaSeeking** devem tratar os parâmetros de hora de entrada e saída como estando no novo formato de hora. Por exemplo, se a variável *m \_ rtDuration* representar a duração em unidades de tempo de referência, mas o formato de hora atual for frames, o método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deverá retornar o valor *m \_ rtDuration* convertido em quadros. Por exemplo:


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



Além disso, certifique-se de verificar o \_ \_ sinalizador retornartime de busca no método [**IMediaSeeking:: setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) . Se esse sinalizador estiver presente, converta os valores de posição em tempos de referência quando retorná-los ao chamador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Dando suporte à busca em um filtro de origem](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




