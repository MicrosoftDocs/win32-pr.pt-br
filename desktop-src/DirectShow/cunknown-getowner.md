---
description: O método GetOwner recupera um ponteiro para a interface IUnknown do componente proprietário. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente é proprietário de si mesmo.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Método CUnknown.GetOwner (Combase.h)
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
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076036"
---
# <a name="cunknowngetowner-method"></a>Método CUnknown.GetOwner

O `GetOwner` método recupera um ponteiro para a interface **IUnknown** do componente de propriedade. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente é proprietário de si mesmo.

## <a name="syntax"></a>Sintaxe


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para a interface **IUnknown de** controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




