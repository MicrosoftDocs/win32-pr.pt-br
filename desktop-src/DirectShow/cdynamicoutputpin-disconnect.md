---
description: Método CDynamicOutputPin.Disconnect – o método Disconnect interrompe a conexão de pino atual. Esse método implementa o método IPin::D isconnect.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Método CDynamicOutputPin.Disconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000bbdc0400a84f41cf370beca92b96d898b57ddb62ab7dc72319557fbe18a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983056"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Método CDynamicOutputPin.Disconnect

O `Disconnect` método interrompe a conexão de pino atual. Esse método implementa o [**método IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | O pino não estava conectado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                   |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBasePin::D sconnect**](cbasepin-disconnect.md) para habilitar a desconexão enquanto o filtro está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




