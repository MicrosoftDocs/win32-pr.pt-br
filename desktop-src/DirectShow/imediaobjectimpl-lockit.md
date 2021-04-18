---
description: A classe LockIt é uma classe interna que bloqueia e desbloqueia o DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Classe IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810219"
---
# <a name="imediaobjectimpllockit-class"></a>Classe IMediaObjectImpl:: LockIt

A `LockIt` classe é uma classe interna que bloqueia e desbloqueia o DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="p"></span><span id="P"></span>*DTI*
</dt> <dd>

Ponteiro para o objeto derivado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O `LockIt` Construtor bloqueia o DMO e o destruidor desbloqueia o DMO. Para bloquear o objeto de dentro de sua classe derivada, declare uma variável local do tipo `LockIt` . O DMO é bloqueado enquanto o `LockIt` objeto permanece no escopo:


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



Os métodos no **IMediaObjectImpl** bloqueiam automaticamente o DMO.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Modelo de classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




