---
description: O método IsPartiallySpecified determina se o tipo de mídia está parcialmente definido. Um tipo de mídia será parcial se o tipo principal, subtipo ou tipo de formato for GUID \_ NULL.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType.IsPartiallySpecified (Mtype.h)
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
ms.openlocfilehash: 2c2e7bdbbc43195222b4054f71ec05ebe3c8a7e15ac8c634d57fba61e45bf319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084466"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Método CMediaType.IsPartiallySpecified

O `IsPartiallySpecified` método determina se o tipo de mídia está parcialmente definido. Um tipo de mídia *será parcial* se o tipo principal, subtipo ou tipo de formato for GUID \_ NULL.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o tipo de mídia for parcialmente especificado. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

O [**método IPin::Conexão**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) pode aceitar tipos de mídia parciais.

Na verdade, a implementação não testa o subtipo . Se houver um tipo de formato especificado, o tipo de mídia não será considerado parcial, mesmo que o subtipo seja GUID \_ NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




