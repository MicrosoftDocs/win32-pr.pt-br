---
description: O método IsPartiallySpecified determina se o tipo de mídia está parcialmente definido. Um tipo de mídia será parcial se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759313"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Método CMediaType. IsPartiallySpecified

O `IsPartiallySpecified` método determina se o tipo de mídia está parcialmente definido. Um tipo de mídia será *parcial* se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se o tipo de mídia for especificado parcialmente. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

O método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) pode aceitar tipos de mídia parciais.

A implementação, na verdade, não testa o subtipo. Se houver um tipo de formato especificado, o tipo de mídia não será considerado parcial, mesmo que o subtipo seja \_ nulo como GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




