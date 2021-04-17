---
description: O método de desconfirmação deconfirma o alocador. Esse método implementa o método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator. decommit (Amfilter. h)
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
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755624"
---
# <a name="cbaseallocatordecommit-method"></a>Método CBaseAllocator. decommit

O `Decommit` método desconfirma o alocador. Esse método implementa o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Depois que esse método for chamado, ocorrerá uma falha nas chamadas para o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) . Conforme os exemplos são liberados, eles são retornados para a lista gratuita. Quando o último exemplo é retornado, o alocador chama o método [**CBaseAllocator:: Free**](cbaseallocator-free.md) , que libera a memória alocada. (Na classe base, **Free** é um método virtual puro.)

Além disso, esse método libera todos os threads bloqueados em chamadas **GetBuffer** . As chamadas para **GetBuffer** falham.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




