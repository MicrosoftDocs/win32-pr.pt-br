---
description: Método CTransformOutputPin. CurrentMediaType – o método CurrentMediaType recupera o tipo de mídia para a conexão do PIN atual.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Método CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b223c8c75cd2345c80b5f0905ef7c6699ccc2499b209cbd17681bec5fec01142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756766"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>Método CTransformOutputPin. CurrentMediaType

O `CurrentMediaType` método recupera o tipo de mídia para a conexão do PIN atual.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna uma referência à variável de membro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




