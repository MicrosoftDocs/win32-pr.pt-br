---
description: O método CheckMediaType determina se o filtro aceita um tipo de mídia específico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Método CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758241"
---
# <a name="cbaserenderercheckmediatype-method"></a>Método CBaseRenderer. CheckMediaType

O `CheckMediaType` método determina se o filtro aceita um tipo de mídia específico.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o tipo de mídia proposto for aceitável. Caso contrário, retorna S \_ false ou um código de erro.

## <a name="remarks"></a>Comentários

O pino de entrada chama esse método de seu próprio método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) . A classe derivada deve implementar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




