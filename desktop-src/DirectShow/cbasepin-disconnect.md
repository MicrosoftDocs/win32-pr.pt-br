---
description: O método Disconnect quebra a conexão do PIN atual. Esse método implementa o método IPin::D isconnect.
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
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750699"
---
# <a name="cbasepindisconnect-method"></a>Método CBasePin. Disconnect

O `Disconnect` método quebra a conexão do PIN atual. Esse método implementa o método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
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

A classe base delega a maior parte do trabalho para o método [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




