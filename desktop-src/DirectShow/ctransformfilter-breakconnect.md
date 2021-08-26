---
description: O método BreakConnect libera um PIN de uma conexão.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Método CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053806"
---
# <a name="ctransformfilterbreakconnect-method"></a>Método CTransformFilter. BreakConnect

O `BreakConnect` método libera um PIN de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dir* 
</dt> <dd>

Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual conexão de PIN foi quebrada (entrada ou saída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os métodos [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) e [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) chamam esse método quando uma conexão de PIN é quebrada. Esse método não faz nada na classe base. Se você substituir o método [**CheckConnect**](ctransformfilter-checkconnect.md) , substitua esse método para liberar todos os recursos obtidos no método **CheckConnect** , incluindo ponteiros de interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




