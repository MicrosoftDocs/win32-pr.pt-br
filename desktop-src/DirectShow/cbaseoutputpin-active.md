---
description: Método CBaseOutputPin.Active – o método Ativo notifica o pino de que o filtro agora está ativo.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Método CBaseOutputPin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94e71b3a85fdddd3ea4554575b07871ecdc09070f00c988f24f31378e9effb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640026"
---
# <a name="cbaseoutputpinactive-method"></a>Método CBaseOutputPin.Active

O `Active` método notifica o pino de que o filtro agora está ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                          | Descrição                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Êxito.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Nenhum alocador está disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBasePin::Active.**](cbasepin-active.md) Ele chama o [**método IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) no alocador para alocar memória para buffers.

Se você substituir esse método, chame o método de classe base do método de substituição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




