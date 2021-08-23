---
description: O método Free libera toda a memória do buffer. Esse método é chamado quando o filtro de propriedade delimita o alocador, após o último exemplo de mídia ser liberado.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Método CBaseAllocator.Free (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77555094625bfc6a31a0527fc3223a124b012e72c28ea76e5774de289d63391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794206"
---
# <a name="cbaseallocatorfree-method"></a>Método CBaseAllocator.Free

O `Free` método libera toda a memória do buffer. Esse método é chamado quando o filtro de propriedade delimita o alocador, após o último exemplo de mídia ser liberado.

## <a name="syntax"></a>Sintaxe


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que [**o método Decommit**](cbaseallocator-decommit.md) é chamado, o alocador chama esse método quando ele libera o último exemplo de mídia. A classe derivada deve implementar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




