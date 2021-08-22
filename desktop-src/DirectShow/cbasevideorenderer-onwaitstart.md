---
description: O método OnWaitStart atualiza os tempos gastos aguardando e não aguardando.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Método CBaseVideoRenderer.OnWaitStart (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bc3b895f27490377fd5de188b7cea8ccd429c55d36a5cdd0fea4ce025bac29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502596"
---
# <a name="cbasevideorendereronwaitstart-method"></a>Método CBaseVideoRenderer.OnWaitStart

O `OnWaitStart` método atualiza os tempos gastos aguardando e não aguardando.

## <a name="syntax"></a>Sintaxe


```C++
void OnWaitStart();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função membro é chamada ao começar a aguardar um evento de renderização. Ele é usado somente para medidas de desempenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




