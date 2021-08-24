---
description: Construtor CAMEvent.CAMEvent – método do construtor.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Construtor CAMEvent.CAMEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0fd5895ada4bbbd1bf4ad24710f7782fdfb9c932f2d9446ff0d992335437da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540547"
---
# <a name="cameventcamevent-constructor"></a>Construtor CAMEvent.CAMEvent

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valor booliana que especifica se o objeto é um evento de redefinição manual ou um evento de redefinição automática. Se **TRUE**, o objeto será um evento de redefinição manual. Caso contrário, será um evento de redefinição automática.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **valor HRESULT.** Se o construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

Para compatibilidade com versões anteriores do strmbase.lib, esse parâmetro assume null como **padrão.** No entanto, é preferível passar **um valor** não NULL para que o chamador possa verificar o status do objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento começa em um estado não sinal.

Com um evento de redefinição automática, o [**método CAMEvent::Wait**](camevent-wait.md) redefine o evento para não sinal quando o método retorna. Com um evento de redefinição manual, o evento permanece sinalizado até que você chame o [**método CAMEvent::Reset.**](camevent-reset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




