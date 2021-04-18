---
description: O método EOS fornece uma chamada de fim de fluxo para o pino de entrada.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Método COutputQueue. EOS (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785359"
---
# <a name="coutputqueueeos-method"></a>Método COutputQueue. EOS

O `EOS` método fornece uma chamada de fim de fluxo para o pino de entrada.

## <a name="syntax"></a>Sintaxe


```C++
void EOS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o objeto estiver usando um thread, ele enfileira uma mensagem de \_ controle de pacote EOS. O thread entrega quaisquer exemplos pendentes e chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada.

Se o objeto não estiver usando um thread, ele chamará o método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para entregar quaisquer exemplos pendentes. Em seguida, ele chama **IPin:: EndOfStream** no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




