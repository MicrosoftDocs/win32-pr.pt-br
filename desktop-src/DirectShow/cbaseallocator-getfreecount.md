---
description: O método GetFreeCount recupera o número de amostras de mídia que não estão em uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Método CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780895"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Método CBaseAllocator. GetFreeCount

O `GetFreeCount` método recupera o número de amostras de mídia que não estão em uso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

Endereço de uma variável que recebe o número de amostras que não estão em uso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método implementa o método [**IMemAllocatorCallbackTemp:: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) . O alocador não expõe a interface IMemAllocatorCallbackTemp, a menos que o sinalizador *fEnableReleaseCallback* seja definido como **true** no Construtor CBaseAllocator.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




