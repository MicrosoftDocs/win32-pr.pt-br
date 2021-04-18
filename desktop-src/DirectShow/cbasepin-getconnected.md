---
description: O método getconnecty recupera o PIN conectado a este pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Método CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752904"
---
# <a name="cbasepingetconnected-method"></a>Método CBasePin. GetConnected

O `GetConnected` método recupera o PIN conectado a esse PIN.

## <a name="syntax"></a>Sintaxe


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.

## <a name="remarks"></a>Comentários

Se o PIN não estiver conectado, esse método retornará **NULL**. Chame o método [**CBasePin:: IsConnected**](cbasepin-isconnected.md) para determinar se o PIN está conectado.

O método não chama **AddRef** na interface **IPin** , portanto, o chamador não deve liberar a interface.

## <a name="examples"></a>Exemplos

Como a contagem de referência não é incrementada no ponteiro retornado, você pode encadear chamadas de método em conjunto:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Esse padrão de codificação é muito conveniente; Mas como mostra o exemplo, você deve ter cuidado para não desreferenciar um ponteiro **nulo** quando o PIN não estiver conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




