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
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747412"
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

## <a name="return-value"></a>Retornar valor

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Quando um pino de saída Inicializa um alocador de memória, ele pode chamar esse método para determinar se o PIN de entrada tem requisitos de buffer. Para obter mais informações, consulte [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

A implementação desse método é opcional. Se o filtro tiver requisitos específicos de alinhamento ou prefixo, substitua esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




