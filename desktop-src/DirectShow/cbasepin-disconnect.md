---
description: Método CBasePin. Disconnect – o método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0048624b79daa6948851fd9a56142b97c7e185caa9bbcbdeb6c2c1b19f591eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916626"
---
# <a name="cbasepindisconnect-method"></a>Método CBasePin. Disconnect

O `Disconnect` método quebra a conexão do PIN atual. Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                         | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>             | O PIN não foi conectado.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl> | O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.<br/> |



 

## <a name="remarks"></a>Comentários

A classe base delega a maior parte do trabalho para o método [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




