---
description: O método GetAllocatorRequirements recupera as propriedades de alocador solicitadas pelo PIN de entrada.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Método CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586366"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Método CBaseInputPin. GetAllocatorRequirements

O `GetAllocatorRequirements` método recupera as propriedades de alocador solicitadas pelo pino de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProps* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que é preenchida com os requisitos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Quando um pino de saída Inicializa um alocador de memória, ele pode chamar esse método para determinar se o PIN de entrada tem requisitos de buffer. Para obter mais informações, consulte [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

A implementação desse método é opcional. Se o filtro tiver requisitos específicos de alinhamento ou prefixo, substitua esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




