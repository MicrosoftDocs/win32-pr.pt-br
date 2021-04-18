---
description: A classe CPosPassThru manipula comandos de busca para filtros de transformação, passando-os upstream para o próximo filtro.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Classe CPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780862"
---
# <a name="cpospassthru-class"></a>Classe CPosPassThru

![hierarquia de classe base CPosPassThru](images/cutil14.png)

A `CPosPassThru` classe manipula comandos de busca para filtros de transformação, passando-os upstream para o próximo filtro.

Quando um aplicativo busca o grafo de filtro, o Gerenciador de grafo de filtro fornece o comando de busca aos filtros de processador. O comando é passado para upstream, por meio do pino de saída de cada filtro, até atingir um filtro que possa executar o comando (se houver). Para obter detalhes, consulte [buscando](seeking.md). A `CPosPassThru` classe passa todos os comandos de busca para o pino de saída no filtro upstream, conforme mostrado no diagrama a seguir.

![a classe CPosPassThru envia comandos de busca upstream.](images/cpospassthru.png)

Embora essa classe seja fornecida na biblioteca de classes base, o DirectShow também fornece a mesma classe em Quartz.dll. O uso da versão Quartz.dll pode reduzir um pouco o tamanho do código em seu filtro, pois a classe é carregada em tempo de execução da DLL. Para usar essa versão, chame a função [**CreatePosPassThru**](createpospassthru.md) .

No método **NonDelegatingQueryInterface** do pino de saída, delegue ao objeto **CPosPassThru** sempre que a interface solicitada for [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), conforme mostrado no código a seguir:


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



Exceto quando indicado, todos os métodos [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) nessa classe chamam o método correspondente no PIN conectado e retornam o resultado.



| Métodos públicos                                                    | Descrição                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | Método de construtor.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Obsoleto.                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | Recupera os carimbos de data/hora no exemplo atual. VirtuaisLUNs.                                           |
| Métodos IMediaPosition                                            | Descrição                                                                                         |
| [**obter \_ duração**](cpospassthru-get-duration.md)                | Recupera a duração do fluxo.                                                               |
| [**colocar \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | Define a posição atual, em relação à duração total do fluxo.                            |
| [**obter \_ StopTime**](cpospassthru-get-stoptime.md)                | Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.         |
| [**colocar \_ StopTime**](cpospassthru-put-stoptime.md)                | Define a hora em que a reprodução será interrompida, em relação à duração do fluxo.              |
| [**obter \_ preverttime**](cpospassthru-get-prerolltime.md)          | Recupera a quantidade de dados que serão enfileirados antes da posição inicial.                         |
| [**colocar \_ preverttime**](cpospassthru-put-prerolltime.md)          | Define a quantidade de dados que serão enfileirados antes da posição inicial.                              |
| [**taxa de obtenção \_**](cpospassthru-get-rate.md)                        | Recupera a taxa de reprodução.                                                                        |
| [**taxa de Put \_**](cpospassthru-put-rate.md)                        | Define a taxa de reprodução.                                                                             |
| [**obter \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | Recupera a posição atual, em relação à duração total do fluxo.                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | Determina se o fluxo pode ser buscado retroativamente.                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | Determina se o fluxo pode ser buscado em frente.                                                |
| Métodos IMediaSeeking                                             | Descrição                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | Consulta se um fluxo especificou recursos de busca.                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | Converte de um formato de tempo para outro.                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | Recupera o intervalo de vezes em que a busca é eficiente.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Recupera todos os recursos de busca do fluxo.                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | Recupera a posição atual, em relação à duração total do fluxo.                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | Recupera a duração do fluxo.                                                               |
| [**Getpositiones**](cpospassthru-getpositions.md)                 | Recupera a posição atual e a posição de parada, em relação à duração total do fluxo. |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | Recupera a quantidade de dados que serão enfileirados antes da posição inicial.                         |
| [**GetRate**](cpospassthru-getrate.md)                           | Recupera a taxa de reprodução.                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Recupera o formato de hora atual.                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | Determina se há suporte para um formato de hora especificado.                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | Determina se um formato de hora especificado é o formato em uso no momento.                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | Recupera o formato de hora preferencial para o fluxo.                                                 |
| [**Setpositiones**](cpospassthru-setpositions.md)                 | Define a posição atual e a posição de parada.                                                    |
| [**SetRate**](cpospassthru-setrate.md)                           | Define a taxa de reprodução.                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | Define o formato de hora.                                                                               |
| Funções auxiliares                                                  | Descrição                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | Cria um `CPosPassThru` objeto ou [**CRendererPosPassThru**](crendererpospassthru.md) .            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




