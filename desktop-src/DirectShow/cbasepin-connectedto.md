---
description: O método ConnectedTo recupera um ponteiro para o pino conectado, se for o caso. Esse método implementa o método IPin::ConnectedTo.
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Método CBasePin.ConnectedTo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a37eafe9abf226be20cf5d573abc91bc52ee070e7667dbab3a8799f74022c92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916756"
---
# <a name="cbasepinconnectedto-method"></a>Método CBasePin.ConnectedTo

O `ConnectedTo` método recupera um ponteiro para o pino conectado, se for o caso. Esse método implementa o [**método IPin::ConnectedTo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppPin* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles na tabela a seguir.



| Código de retorno                                                                                           | Descrição                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/> |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino não está conectado.<br/>      |



 

## <a name="remarks"></a>Comentários

Se o método for bem-sucedido, a interface **IPin** retornada terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




