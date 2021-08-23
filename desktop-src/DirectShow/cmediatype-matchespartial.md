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
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073970"
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

## <a name="return-value"></a>Valor retornado

Retornará **true** se os tipos de mídia corresponderem. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

O tipo de mídia especificado por *ppartial* pode ter um valor de GUID \_ NULL para o tipo principal, subtipo ou formato. Todos os membros com \_ valores nulos de GUID não são testados. (Em vigor, GUID \_ NULL atua como um curinga.) Os membros com valores diferentes de GUID \_ NULL devem corresponder ao tipo de mídia a ser correspondido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




