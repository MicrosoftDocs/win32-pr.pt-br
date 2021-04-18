---
description: O método de alocador recupera um ponteiro para o alocador de memória.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Método CRendererInputPin. alocador (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769210"
---
# <a name="crendererinputpinallocator-method"></a>Método CRendererInputPin. alocador

O `Allocator` método recupera um ponteiro para o alocador de memória.

## <a name="syntax"></a>Sintaxe


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador ou **NULL**.

## <a name="remarks"></a>Comentários

Esse método retorna a variável de membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) . O método não incrementa a contagem de referência na interface. Esse método é estritamente um método acessador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




