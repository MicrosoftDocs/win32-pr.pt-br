---
description: O método GetTime recupera a hora de referência atual. Esse método implementa o método IReferenceClock::GetTime.
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock.GetTime (Refclock.h)
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
ms.openlocfilehash: 5a1ffd021ac917a7aa1e12f3d3dc9c4a62ea1f883f126bca1d9c1300d335bdae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954975"
---
# <a name="cbasereferenceclockgettime-method"></a>Método CBaseReferenceClock.GetTime

O `GetTime` método recupera a hora de referência atual. Esse método implementa o [**método IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

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

Ponteiro para uma variável que recebe a hora atual, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | Argumento de ponteiro **NULL.**<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | A hora retornada é igual ao valor anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                                         |



 

## <a name="remarks"></a>Comentários

Esse método chama o [**método CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) para determinar a hora do relógio real. Se a hora do relógio for estritamente maior que o valor anterior, `GetTime` usará a hora do relógio e retornará S \_ OK. Caso contrário, `GetTime` usa o valor anterior e retorna S \_ FALSE. Portanto, o relógio interno pode ser executado para trás por um curto período, sem fazer com que o tempo de referência seja executado para trás. Em vez disso, o tempo de referência será "parado" com o mesmo valor até que o relógio interno seja atualizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




