---
description: 'Método CBaseInputPin. Receive – o método Receive recebe o próximo exemplo de mídia no fluxo. Esse método implementa o método IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Método CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099684"
---
# <a name="cbaseinputpinreceive-method"></a>Método CBaseInputPin. Receive

O `Receive` método recebe o próximo exemplo de mídia no fluxo. Esse método implementa o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Sucesso.<br/>                                        |
| <dl> <dt>**\_falso**</dt> </dl>                 | O PIN está sendo liberado no momento; o exemplo foi rejeitado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ erro de tempo de execução \_**</dt> </dl>   | Ocorreu um erro em tempo de execução.<br/>                      |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>     | O PIN foi interrompido.<br/>                             |



 

## <a name="remarks"></a>Comentários

O pino de saída upstream chama esse método para entregar um exemplo ao pino de entrada. O PIN de entrada deve seguir um destes procedimentos:

-   Processe o exemplo antes de retornar.
-   Retorne e processe o exemplo em um thread de trabalho.
-   Rejeite o exemplo.

Se o PIN usar um thread de trabalho para processar o exemplo, adicione uma contagem de referência ao exemplo dentro desse método. Depois que o método retorna, o pino upstream libera o exemplo. Quando a contagem de referência do exemplo chega a zero, o exemplo retorna ao alocador para reutilização.

Esse método é síncrono e pode ser bloqueado. Se o método puder ser bloqueado, o método [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) do PIN deverá retornar s \_ OK.

Na classe base, esse método executa as seguintes etapas:

1.  Chama o método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) para verificar se o PIN pode processar amostras agora. Se não puder, por exemplo, se o PIN for interrompido, o método falhará.
2.  Recupera as propriedades de exemplo e verifica se o formato foi alterado (veja abaixo).
3.  Se o formato for alterado, o método chamará o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar se o novo formato é aceitável.
4.  Se o novo formato não for aceitável, o método chamará o método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , lançará um \_ evento ERRORABORT do EC e retornará um código de erro.
5.  Supondo que não houvesse erros, o método retorna S \_ OK.

Teste para uma alteração de formato da seguinte maneira:

-   Se o exemplo der suporte à interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , verifique o membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) . Se o \_ \_ sinalizador tipochanged de exemplo am estiver presente, o formato será alterado.
-   Caso contrário, se o exemplo não oferecer suporte a **IMediaSample2**, chame o método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) . Se o método retornar um valor não **nulo** , o formato terá mudado.

Na classe base, esse método não processa o exemplo. A classe derivada deve substituir esse método para executar o processamento. (O que isso envolve depende inteiramente do filtro.) A classe derivada deve chamar o método de classe base, para verificar os erros descritos anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




