---
description: O método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Método CDynamicOutputPin. Disconnect (Amfilter. h)
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
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754989"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Método CDynamicOutputPin. Disconnect

O `Disconnect` método quebra a conexão do PIN atual. Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN não foi conectado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                   |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin::D isconnect**](cbasepin-disconnect.md) para habilitar a desconexão enquanto o filtro está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




