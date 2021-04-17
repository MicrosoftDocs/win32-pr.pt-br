---
description: O método Receive recebe um exemplo de mídia, processa-o e o entrega para o filtro downstream.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter. Receive (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748012"
---
# <a name="ctransinplacefilterreceive-method"></a>Método CTransInPlaceFilter. Receive

O `Receive` método recebe um exemplo de mídia, processa-o e o entrega para o filtro downstream.

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

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) no exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Sucesso<br/>          |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Erro inesperado<br/> |



 

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método quando recebe um exemplo. O filtro chama o método [**Transform**](ctransinplacefilter-transform.md) , que a classe derivada deve implementar. O método **Transform** processa os dados. Se o filtro estiver usando apenas um alocador, ele passará *pSample* diretamente para o método **Transform** . Caso contrário, ele copiará *pSample* e passará a cópia.

Se o método **Transform** retornar S \_ false, o `Receive` método descartará o exemplo. Na primeira amostra descartada, o filtro envia um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro. Caso contrário, se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo de saída. Para fazer isso, ele chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




