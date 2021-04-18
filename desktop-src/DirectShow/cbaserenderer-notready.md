---
description: O método não Ready sinaliza que uma transição de estado ainda não foi concluída.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Método CBaseRenderer. não Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778629"
---
# <a name="cbaserenderernotready-method"></a>Método CBaseRenderer. não Ready

O `NotReady` método sinaliza que uma transição de estado ainda não foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
void NotReady();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método faz com que o método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) retorne o VFW \_ S \_ State \_ intermediário, que indica que o filtro ainda está em transição para seu estado atual. O filtro chama esse método sempre que uma transição de estado está pendente. (Isso ocorre quando o filtro é pausado, até receber um exemplo.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




