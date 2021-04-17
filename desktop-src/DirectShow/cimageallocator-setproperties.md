---
description: 'O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método substitui o método CBaseAllocator:: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Método CImageAllocator. SetProperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747821"
---
# <a name="cimageallocatorsetproperties-method"></a>Método CImageAllocator. SetProperties

O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método substitui o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRequest* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Ponteiro para uma estrutura de **\_ Propriedades de alocador** que recebe as propriedades reais do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método chama [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) para validar o tamanho do buffer solicitado. Ele também chama a versão de classe base do `SetProperties` .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




