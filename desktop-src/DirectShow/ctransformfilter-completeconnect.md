---
description: Método CTransformFilter.CompleteConnect – o método CompleteConnect conclui uma conexão de pino.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e708745231f320d143c55403a75178e78432a162c3c89fc2c5fe8fd62cdd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687306"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Método CTransformFilter.CompleteConnect

O `CompleteConnect` método conclui uma conexão de pino.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*direction* 
</dt> <dd>

Membro do tipo [**enumerado PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando qual pino no filtro está fazendo a conexão.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino nesta tentativa de conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os [**métodos CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) chamam esse método durante o processo de conexão de pino. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




