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
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094904"
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
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




