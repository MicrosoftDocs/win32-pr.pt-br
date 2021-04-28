---
description: Método CDynamicOutputPin. Disconnect – o método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
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
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099294"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Método CDynamicOutputPin. Disconnect

O `Disconnect` método quebra a conexão do PIN atual. Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN não foi conectado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Sucesso.<br/>                   |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin::D isconnect**](cbasepin-disconnect.md) para habilitar a desconexão enquanto o filtro está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




