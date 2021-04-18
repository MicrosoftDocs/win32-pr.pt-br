---
description: 'O método getTime recupera o tempo de referência atual. Esse método implementa o método IReferenceClock:: getTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock. getTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753348"
---
# <a name="cbasereferenceclockgettime-method"></a>Método CBaseReferenceClock. getTime

O `GetTime` método recupera o tempo de referência atual. Esse método implementa o método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora atual, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/>                       |
| <dl> <dt>**\_falso**</dt> </dl>   | A hora retornada é igual ao valor anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                                         |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CBaseReferenceClock:: Getparticulartime**](cbasereferenceclock-getprivatetime.md) para determinar o tempo real do relógio. Se a hora do relógio for estritamente maior que o valor anterior, o `GetTime` usará a hora do relógio e retornará S \_ OK. Caso contrário, `GetTime` o usará o valor anterior e retornará S \_ false. Portanto, o relógio interno pode ficar recuado por um curto período, sem fazer com que o tempo de referência seja executado retroativamente. Em vez disso, o tempo de referência será "paralisado" no mesmo valor até que o relógio interno seja atualizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




