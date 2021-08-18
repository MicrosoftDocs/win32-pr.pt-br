---
description: O método Receive recebe um exemplo de mídia, processa-o e entrega-o ao filtro downstream.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter.Receive (Transip.h)
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
ms.openlocfilehash: 390d0243631e4ac31da779ca01197500f1d3df18127a3b86f0cf1ea834283f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053456"
---
# <a name="ctransinplacefilterreceive-method"></a>Método CTransInPlaceFilter.Receive

O `Receive` método recebe um exemplo de mídia, processa-o e entrega-o ao filtro downstream.

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

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito<br/>          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Erro inesperado<br/> |



 

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método quando recebe um exemplo. O filtro chama o [**método Transform,**](ctransinplacefilter-transform.md) que a classe derivada deve implementar. O **método Transform** processa os dados. Se o filtro estiver usando apenas um alocador, ele passará *pSample* diretamente para o **método Transform.** Caso contrário, ele copia *pSample* e passa a cópia.

Se o **método Transform** retornar S \_ FALSE, o método descarta o `Receive` exemplo. No primeiro exemplo descartado, o filtro envia um evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) para o gerenciador de grafo de filtro. Caso contrário, se o **método Transform** retornar S \_ OK, o filtro entregará o exemplo de saída. Para fazer isso, ele chama o [**método IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




