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
ms.openlocfilehash: 8de57346138b4683f59cfa612f01fff1ef3d8fd9aceec9b34daee49bfa74ebbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157976"
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

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o tipo de mídia proposto for aceitável. Caso contrário, retorna S \_ false ou um código de erro.

## <a name="remarks"></a>Comentários

O pino de entrada chama esse método de seu próprio método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) . A classe derivada deve implementar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




