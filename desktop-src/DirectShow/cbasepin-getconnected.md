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
ms.openlocfilehash: 8bac5bc971f67c7678d2160cadb452995165638db4bb44d2ed1c89b3ab08f882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526836"
---
# <a name="cbasepingetconnected-method"></a>Método CBasePin. GetConnected

O `GetConnected` método recupera o PIN conectado a esse PIN.

## <a name="syntax"></a>Sintaxe


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




