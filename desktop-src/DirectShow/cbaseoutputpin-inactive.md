---
description: O método inativo notifica o PIN de que o filtro não está mais ativo.
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Método CBaseOutputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afec15e295e5c14cfb3d9efa6e733d1dc288b319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750700"
---
# <a name="cbaseoutputpininactive-method"></a>Método CBaseOutputPin. Inactive

O `Inactive` método notifica o PIN de que o filtro não está mais ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                          | Descrição                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Êxito.<br/>                          |
| <dl> <dt>**VFW \_ E \_ nenhum \_ alocador**</dt> </dl> | Não há alocador de memória disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: Inactive**](cbasepin-inactive.md) . Ele chama o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desconfirmar o alocador de memória.

Se você substituir esse método, chame o método de classe base do seu método de substituição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




