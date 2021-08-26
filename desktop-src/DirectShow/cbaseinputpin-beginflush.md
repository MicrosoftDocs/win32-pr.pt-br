---
description: 'O método CBaseInputPin inicia uma operação de liberação. Esse método implementa o método IPin:: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Método CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103206"
---
# <a name="cbaseinputpinbeginflush-method"></a>Método CBaseInputPin. BeginFlush

O `CBaseInputPin` método inicia uma operação de liberação. Esse método implementa o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define o sinalizador [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) como **true**, o que faz com que o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rejeite mais exemplos.

A classe derivada deve substituir esse método e executar as seguintes etapas:

1.  Chame o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) nos Pins de entrada downstream. Se o PIN ainda não tiver entregue nenhuma amostra de mídia downstream, você poderá ignorar esta etapa. Se os Pins de saída derivarem da classe [**CBaseOutputPin**](cbaseoutputpin.md) , você poderá chamar o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .
2.  Chame o método da classe base.
3.  Iniciar descartar dados na fila.
4.  Retornar de todas as chamadas bloqueadas para o método **Receive** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




