---
description: 'O método Next recupera um número especificado de Pins na sequência de enumeração. Esse método implementa o método IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Método CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 683b8eb5beb9946db7f37d4db53a84c96d5bff7fc91fa4864020fffde5554824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567076"
---
# <a name="cenumpinsnext-method"></a>Método CEnumPins. Next

O método Next recupera um número especificado de Pins na sequência de enumeração. Esse método implementa o método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de Pins a serem recuperados.

</dd> <dt>

*ppPins* 
</dt> <dd>

Matriz de tamanho *cPins* que é preenchida com ponteiros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*pcFetched* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de Pins recuperados. Pode ser **NULL** se *cPins* for 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                    | Não foi possível recuperar quantos Pins forem solicitados.<br/>                                 |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento inválido.<br/>                                                           |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Argumento de ponteiro **nulo** .<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt> </dl> | O estado do filtro foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método recupera ponteiros para o número especificado de Pins, começando na posição atual na enumeração e os coloca na matriz especificada.

Esse método chama o método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) do filtro para recuperar os Pins.

Se o método tiver sucesso, os ponteiros **IPin** terão contagens de referência pendentes. Lembre-se de liberá-los quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




