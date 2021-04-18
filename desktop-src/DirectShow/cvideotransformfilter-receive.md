---
description: 'O método Receive recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. Esse método substitui o método CTransformFilter:: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Método CVideoTransformFilter. Receive (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759082"
---
# <a name="cvideotransformfilterreceive-method"></a>Método CVideoTransformFilter. Receive

O `Receive` método recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. Esse método substitui o método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .

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

Esse método chama [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) para determinar se ele deve entregar esse exemplo ou simplesmente descartá-lo. Se **ShouldSkipFrame** retornar **false** (indicando que o exemplo deve ser entregue), o método fará o seguinte:

1.  Chama [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) para preparar o exemplo de saída
2.  Chama [**CTransformFilter:: Transform**](ctransformfilter-transform.md) para processar o exemplo de entrada. Esse método é virtual puro e deve ser implementado na classe derivada.
3.  Chama [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) para entregar o exemplo de saída.

Além disso, esse método verifica as alterações de formato no exemplo de entrada ou saída, chamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se houver uma alteração de formato, o método definirá o tipo de conexão no PIN correspondente. Antes de definir o novo tipo, ele chama **StopStreaming**. Depois de definir o novo tipo, ele chama **StartStreaming**. A classe derivada pode usar esses métodos para atualizar seu estado interno. A classe derivada também pode precisar verificar o novo formato em seu método de **transformação** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




