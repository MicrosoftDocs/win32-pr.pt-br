---
description: 'A classe CTransInPlaceFilter é projetada para filtros de transformação in-loco, que são filtros que modificam os dados de entrada em vez de copiar os dados entre os buffers. Para usar essa classe, derive uma nova classe de CTransInPlaceFilter e implemente os seguintes métodos:'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: Classe CTransInPlaceFilter (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759086"
---
# <a name="ctransinplacefilter-class"></a>Classe CTransInPlaceFilter

![hierarquia de classe CTransInPlaceFilter](images/tsip03.png)

A `CTransInPlaceFilter` classe é projetada para filtros de transformação in-loco, que são filtros que modificam os dados de entrada em vez de copiar os dados entre os buffers. Para usar essa classe, derive uma nova classe de `CTransInPlaceFilter` e implemente os seguintes métodos:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter:: Transform**](ctransinplacefilter-transform.md)

Essa classe usa a classe [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) para seu pino de entrada e a classe [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) para seu pino de saída. Normalmente, você não precisa substituir essas classes de PIN. O filtro cria ambos os Pins no método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) . Se você substituir as classes de PIN, deverá substituir **GetPin** para criar seus PINs personalizados.

Essa classe é projetada para que o tipo de entrada sempre corresponda ao tipo de saída. Sempre que possível, o filtro usa um único alocador para ambas as conexões de PIN.

## <a name="preferred-media-types"></a>Tipos de mídia preferenciais

Se o pino de saída já estiver conectado, o PIN de entrada oferecerá os tipos preferenciais do filtro downstream. (Na verdade, ele simplesmente retorna o objeto enumerador do filtro downstream.) Caso contrário, ele não tem tipos preferenciais. O pino de saída tem o mesmo comportamento, mas na ordem inversa: se o PIN de entrada já estiver conectado, o pino de saída oferecerá os tipos preferenciais do filtro upstream. Caso contrário, ele não tem tipos preferenciais

## <a name="pin-connections"></a>Fixar conexões

Quando um PIN se conecta, o filtro geralmente reconecta o outro PIN para garantir que ambos os Pins usem o mesmo tipo de mídia e o mesmo alocador. (O mecanismo de reconexão de Pins é descrito em [reconectando Pins](reconnecting-pins.md).) Dois cenários são possíveis: o PIN de entrada se conecta primeiro ou o pino de saída se conecta primeiro.

Suponha que o PIN de entrada se conecte primeiro. Ocorrem as seguintes etapas:

1.  O pino de entrada chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia.
2.  O filtro upstream seleciona um alocador. Neste ponto, o pino de entrada não tem requisitos de alocador e aceita qualquer alocador para a conexão. Se o filtro upstream solicitar um alocador, o PIN criará um novo. Por motivos descritos em breve, esse alocador não será usado na conexão final. Ele é fornecido apenas para ajudar a concluir esse estágio do processo de conexão.

Posteriormente, quando o pino de saída se conectar:

1.  O pino de saída chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia. Ele também chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no filtro upstream. Isso garante que o PIN de entrada possa alterar seu tipo de mídia para corresponder.
2.  O pino de saída chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia. Ele também chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no filtro upstream. Isso garante que o PIN de entrada possa alterar seu tipo de mídia para corresponder.
3.  O pino de saída chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia. Ele também chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no filtro upstream. Isso garante que o PIN de entrada possa alterar seu tipo de mídia para corresponder.
4.  Desta vez, o método [**Getalocador**](ctransinplaceinputpin-getallocator.md) do pino de entrada retorna o alocador downstream e [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) retorna os requisitos de alocador do filtro downstream. O PIN de entrada aceita qualquer alocador escolhido pelo filtro upstream.
5.  Desta vez, o método [**Getalocador**](ctransinplaceinputpin-getallocator.md) do pino de entrada retorna o alocador downstream e [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) retorna os requisitos de alocador do filtro downstream. O PIN de entrada aceita qualquer alocador escolhido pelo filtro upstream.

Agora, considere o cenário oposto, em que o pino de saída é o primeiro PIN a ser conectado.

1.  O pino de saída chama o método [**CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia.
2.  Ele seleciona um alocador, preferindo-se a usar o alocador do filtro downstream.

Em seguida, quando o PIN de entrada se conecta:

1.  O PIN de entrada verifica o tipo de mídia chamando [**CheckInputType**](ctransformfilter-checkinputtype.md) no filtro e chamando [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída do filtro downstream.
2.  Se o tipo de entrada não corresponder ao tipo de saída, o filtro reconectará o pino de saída.
3.  O filtro upstream seleciona um alocador. O método [**Getalocador**](ctransinplaceinputpin-getallocator.md) do pino de entrada retorna o alocador downstream, e o PIN de entrada aceita qualquer alocador que o filtro upstream selecionar.
4.  O filtro usa o mesmo alocador para a conexão downstream, possivelmente substituindo o alocador downstream original.

Essa sequência de eventos muda ligeiramente se qualquer um dos alocadores envolvidos for somente leitura, pois o alocador downstream deve ser gravável. Nesse caso, o filtro pode usar dois alocadores separados.

Para obter mais informações sobre como usar essa classe, consulte [Writing Transform Filters](writing-transform-filters.md).



| Variáveis de membro protegido                                                        | Descrição                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**\_bModifiesData m**](ctransinplacefilter-m-bmodifiesdata.md)                   | Indica se o filtro modifica os dados de exemplo.                           |
| Métodos Protegidos                                                                 | Descrição                                                                      |
| [**CopiarObjeto**](ctransinplacefilter-copy.md)                                          | Copia um exemplo de mídia.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Recupera um ponteiro para o PIN de entrada do filtro.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Recupera um ponteiro para o pino de saída do filtro.                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | Determina se o tipo de mídia de entrada corresponde ao tipo de mídia de saída.           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | Determina se os Pins de entrada e de saída estão usando alocadores diferentes.     |
| Métodos públicos                                                                    | Descrição                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | Método de construtor.                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | Recupera um PIN.                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | Recupera um tipo de mídia preferencial para o pino de saída.                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | Define os requisitos de buffer do pino de saída.                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | Verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | Conclui uma conexão de PIN.                                                      |
| [**Recebe**](ctransinplacefilter-receive.md)                                    | Recebe um exemplo de mídia, processa-o e o entrega para o filtro downstream. |
| Métodos virtuais puros                                                              | Descrição                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Transforma um exemplo no local.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




