---
description: O método Receive é chamado quando o objeto recebe um exemplo de mídia do pino de saída. A classe derivada deve implementar esse método.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Método CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759562"
---
# <a name="cpullpinreceive-method"></a>Método CPullPin. Receive

O `Receive` método é chamado quando o objeto recebe um exemplo de mídia do pino de saída. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Retornar um valor diferente de S \_ OK irá parar o thread de extração de dados.

## <a name="remarks"></a>Comentários

Esse método é chamado sempre que um novo exemplo chega do pino de saída. Escreva esse método da mesma maneira que o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

Os carimbos de data/hora no exemplo especificam os deslocamentos de byte, em relação à posição inicial original que foi especificada no método [**CPullPin:: Seek**](cpullpin-seek.md) .

A posição inicial é arredondada para baixo até o limite de alinhamento mais próximo e a posição de parada é arredondada para cima até o limite de alinhamento mais próximo. Além disso, se a posição de parada exceder a duração total, a duração será usada em vez disso.

Todos os carimbos de data/hora são fornecidos como um deslocamento de byte multiplicado por 10 milhões, definidos como as unidades de constante. Portanto, a noção de um segundo é um byte. Para localizar os deslocamentos de bytes reais, chame [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) e divida os resultados por unidades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




