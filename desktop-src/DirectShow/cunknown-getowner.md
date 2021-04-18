---
description: O método GetOwner Recupera um ponteiro para a interface IUnknown do componente proprietário. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente pertence a si mesmo.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Método CUnknown. getproprietário (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749609"
---
# <a name="cunknowngetowner-method"></a>Método CUnknown. GetOwner

O `GetOwner` método recupera um ponteiro para a interface **IUnknown** do componente proprietário. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente pertence a si mesmo.

## <a name="syntax"></a>Sintaxe


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a interface **IUnknown** de controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




