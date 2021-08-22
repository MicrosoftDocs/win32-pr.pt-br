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
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954825"
---
# <a name="cbaserenderernotready-method"></a>Método CBaseRenderer. não Ready

O `NotReady` método sinaliza que uma transição de estado ainda não foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
void NotReady();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método faz com que o método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) retorne o VFW \_ S \_ State \_ intermediário, que indica que o filtro ainda está em transição para seu estado atual. O filtro chama esse método sempre que uma transição de estado está pendente. (Isso ocorre quando o filtro é pausado, até receber um exemplo.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




