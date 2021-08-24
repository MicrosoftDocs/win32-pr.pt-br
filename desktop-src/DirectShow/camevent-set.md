---
description: O método Set sinaliza o evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Método CAMEvent. Set (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84059a66a77744b7ea570473474f6b773beae8005b7c4a68e73e59c76829f13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794276"
---
# <a name="cameventset-method"></a>Método CAMEvent. Set

O `Set` método sinaliza o evento.

## <a name="syntax"></a>Sintaxe


```C++
void Set();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O comportamento depende se o objeto é um evento de redefinição automática ou um evento de redefinição manual:

-   **Redefinição automática**: se algum thread estiver aguardando esse evento, um thread será liberado e o evento será redefinido. Se nenhum thread estiver aguardando esse evento, o evento permanecerá sinalizado.
-   **Redefinição manual**: todos os threads aguardando esse evento são liberados. O evento permanece sinalizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




