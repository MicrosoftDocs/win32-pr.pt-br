---
description: O método Decommit delimita o alocador. Esse método implementa o método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator.Decommit (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 614986a912f08d918d4fbbaf6b3eeeb0d3b2c3eabc47748351934a08b8280cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017544"
---
# <a name="cbaseallocatordecommit-method"></a>Método CBaseAllocator.Decommit

O `Decommit` método delimita o alocador. Esse método implementa o [**método IMemAllocator::D ecommit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Depois que esse método for chamado, as chamadas para o [**método CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) falharão. À medida que os exemplos são liberados, eles são retornados para a lista gratuita. Quando o último exemplo é retornado, o alocador chama o [**método CBaseAllocator::Free,**](cbaseallocator-free.md) que libera a memória alocada. (Na classe base, **Free** é um método virtual puro.)

Além disso, esse método libera todos os threads bloqueados em **chamadas GetBuffer.** As chamadas para **GetBuffer** falham.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




