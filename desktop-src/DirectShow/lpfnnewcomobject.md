---
description: Ponteiro de função LPFNNewCOMObject-ponteiro para uma função que cria uma instância do objeto.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Ponteiro de função LPFNNewCOMObject (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116524"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Ponteiro de função LPFNNewCOMObject

Ponteiro para uma função que cria uma instância do objeto.

## <a name="syntax"></a>Sintaxe


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto que agrega o novo objeto, se houver. Esse ponteiro pode ser **nulo**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Se o Construtor falhar, esse parâmetro receberá um código de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma nova instância do objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




