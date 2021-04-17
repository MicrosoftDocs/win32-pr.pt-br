---
description: O método StartUsingOutputPin obtém acesso ao PIN para uma operação de streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Método CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748811"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>Método CDynamicOutputPin. StartUsingOutputPin

O `StartUsingOutputPin` método obtém acesso ao PIN para uma operação de streaming.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                               |
| <dl> <dt>**E \_ inesperado**</dt> </dl>          | Erro inesperado.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ estado \_ alterado**</dt> </dl> | O filtro foi interrompido ou o PIN começou a ser liberado.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método antes de chamar quaisquer métodos que entreguem dados ao PIN de entrada conectado ou que alterem o tipo de mídia da conexão. Por exemplo, essa regra se aplica aos seguintes métodos:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: receber**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Depois, chame o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) para liberar o acesso ao PIN.

Se o PIN estiver bloqueado, o `StartUsingOutputPin` aguardará que o PIN se torne desbloqueado. Se o filtro for interrompido enquanto o método estiver aguardando, o método retornará imediatamente o \_ estado E VFW \_ \_ alterado. O PIN mantém uma contagem de quantas vezes `StartUsingOutputPin` foi chamado sem uma chamada correspondente para **StopUsingOutputPin**. Se outro thread tentar bloquear o PIN enquanto essa contagem for diferente de zero, o PIN definirá seu status de bloqueio como "pendente". O PIN fica bloqueado depois que todas as operações de streaming são concluídas, na chamada final para **StopUsingOutputPin**.

Não mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) ao chamar esse método. Caso contrário, se o PIN for bloqueado, ele nunca poderá ser desbloqueado, causando um deadlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




