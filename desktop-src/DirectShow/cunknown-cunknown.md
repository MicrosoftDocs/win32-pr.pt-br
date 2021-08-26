---
description: Construtor de CUnknown. CUnknown-método de construtor.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Construtor CUnknown. CUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7d2f1b70202200c705394790bb4b1e8d81349b71f534cc36fba9a8baed65f03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998926"
---
# <a name="cunknowncunknown-constructor"></a>Construtor CUnknown. CUnknown

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres que contém o nome do objeto; usado no construtor [**CBaseObject**](cbaseobject.md) para depuração.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto é inicializado com uma contagem de referência igual a zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




