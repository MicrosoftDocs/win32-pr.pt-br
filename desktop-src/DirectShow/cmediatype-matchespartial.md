---
description: O método MatchesPartial determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Método CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756621"
---
# <a name="cmediatypematchespartial-method"></a>Método CMediaType. MatchesPartial

O `MatchesPartial` método determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppartial* 
</dt> <dd>

Ponteiro para o tipo de mídia a ser correspondido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se os tipos de mídia corresponderem. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

O tipo de mídia especificado por *ppartial* pode ter um valor de GUID \_ NULL para o tipo principal, subtipo ou formato. Todos os membros com \_ valores nulos de GUID não são testados. (Em vigor, GUID \_ NULL atua como um curinga.) Os membros com valores diferentes de GUID \_ NULL devem corresponder ao tipo de mídia a ser correspondido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




