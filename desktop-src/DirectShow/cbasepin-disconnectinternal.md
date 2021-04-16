---
description: O método DisconnectInternal quebra a conexão do PIN atual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin. DisconnectInternal (Amfilter. h)
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
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752512"
---
# <a name="cbasepindisconnectinternal-method"></a>Método CBasePin. DisconnectInternal

O `DisconnectInternal` método quebra a conexão do PIN atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                         | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>             | O PIN não foi conectado.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl> | O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.<br/> |



 

## <a name="remarks"></a>Comentários

O método [**CBasePin::D isconnect**](cbasepin-disconnect.md) delega o processo de desconexão para esse método. Esse método chama o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Ele também libera a contagem de referência no outro PIN, que é mantido pela variável de membro [**\_ conectado CBasePin:: m**](cbasepin-m-connected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




