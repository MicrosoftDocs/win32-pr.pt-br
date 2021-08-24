---
description: O método SendAnyway entrega quaisquer exemplos pendentes.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Método COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4aed3cdd37c50f20b48922c8c711266a111680506813ab4572800abbca971343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831756"
---
# <a name="coutputqueuesendanyway-method"></a>Método COutputQueue. SendAnyway

O `SendAnyway` método entrega quaisquer exemplos pendentes.

## <a name="syntax"></a>Sintaxe


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a variável de membro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) for **true**, o objeto preencherá a matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de fornecer um lote de amostras. Chame esse método para entregar um lote parcial. Por exemplo, o método [**COutputQueue:: EOS**](coutputqueue-eos.md) chama `SendAnyway` para serializar mensagens de fim de fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




