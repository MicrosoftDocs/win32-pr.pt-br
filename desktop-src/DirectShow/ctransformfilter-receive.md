---
description: O método Receive recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Método CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748618"
---
# <a name="ctransformfilterreceive-method"></a>Método CTransformFilter. Receive

O `Receive` método recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream.

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

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) no exemplo de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                             | Descrição                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O filtro upstream deve parar de enviar amostras.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                         |



 

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método quando recebe um exemplo. Esse método chama o método [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , que prepara um novo exemplo de saída. Em seguida, ele chama o método [**CTransformFilter:: Transform**](ctransformfilter-transform.md) , que a classe derivada deve implementar. O método **Transform** processa os dados de entrada e produz dados de saída.

Se o método **Transform** retornar S \_ false, o `Receive` método descartará esse exemplo. Na primeira amostra descartada, o filtro envia um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro. Caso contrário, se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo de saída. Para fazer isso, ele chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




