---
description: Método CBaseOutputPin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Método CBaseOutputPin. Active (Amfilter. h)
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
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096204"
---
# <a name="cbaseoutputpinactive-method"></a>Método CBaseOutputPin. active

O `Active` método notifica o PIN de que o filtro está ativo agora.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                          | Descrição                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Sucesso.<br/>                   |
| <dl> <dt>**VFW \_ E \_ nenhum \_ alocador**</dt> </dl> | Nenhum alocador disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: active**](cbasepin-active.md) . Ele chama o método [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) no alocador para alocar memória para buffers.

Se você substituir esse método, chame o método de classe base do seu método de substituição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




