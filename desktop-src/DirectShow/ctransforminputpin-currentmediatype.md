---
description: Método CTransformInputPin.CurrentMediaType – o método CurrentMediaType recupera o tipo de mídia para a conexão de pino atual.
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Método CTransformInputPin.CurrentMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e313cc132f325b57a09e2b8609bc14f052aaaac69187ac4468ee1d5471d2442
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053572"
---
# <a name="ctransforminputpincurrentmediatype-method"></a>Método CTransformInputPin.CurrentMediaType

O `CurrentMediaType` método recupera o tipo de mídia para a conexão de pino atual.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna uma referência à [**variável de membro CBasePin::mt. \_**](cbasepin-m-mt.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




