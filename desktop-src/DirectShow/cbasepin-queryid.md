---
description: O método QueryId recupera o identificador de pino. Esse método implementa o método IPin::QueryId.
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Método CBasePin.QueryId (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac4f7448b27e1780e2d44a512693f3a59113055d66f1b46a85038f04f87f045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158138"
---
# <a name="cbasepinqueryid-method"></a>Método CBasePin.QueryId

O `QueryId` método recupera o identificador de pino. Esse método implementa o [**método IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Id* 
</dt> <dd>

Ponteiro para o identificador de pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>       |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Argumento de ponteiro **NULL.**<br/> |



 

## <a name="remarks"></a>Comentários

Esse método retorna uma cópia da variável de membro [**CBasePin::m \_ pName.**](cbasepin-m-pname.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




