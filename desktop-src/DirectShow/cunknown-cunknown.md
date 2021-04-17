---
description: Método de construtor.
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
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748186"
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
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




