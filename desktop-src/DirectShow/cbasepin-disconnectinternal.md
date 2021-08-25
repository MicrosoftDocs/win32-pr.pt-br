---
description: O método DisconnectInternal interrompe a conexão de pino atual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin.DisconnectInternal (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916526"
---
# <a name="cbasepindisconnectinternal-method"></a>Método CBasePin.DisconnectInternal

O `DisconnectInternal` método interrompe a conexão de pino atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles na tabela a seguir.



| Código de retorno                                                                                         | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | O pino não estava conectado.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NÃO INTERROMPIDO \_**</dt> </dl> | O filtro está ativo e o pino não dá suporte à reconexão dinâmica.<br/> |



 

## <a name="remarks"></a>Comentários

O [**método CBasePin::D isconnect**](cbasepin-disconnect.md) delega o processo de desconexão a esse método. Esse método chama o [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Ele também libera a contagem de referência no outro pino, que é mantido pela variável de membro [**conectada CBasePin::m. \_**](cbasepin-m-connected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




