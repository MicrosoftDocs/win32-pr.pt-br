---
description: Construtor de CBaseObject. CBaseObject-método de construtor.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Construtor CBaseObject. CBaseObject (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35443d212fc244c80da958f2f87d03363c59348be4189393c1c3493521a0439b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076576"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Construtor CBaseObject. CBaseObject

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres que contém o nome do objeto, para fins de depuração.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método incrementa a contagem de objetos ativos. (Consulte [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).)

Aloque o parâmetro *pname* na memória estática:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



A macro de [**nome**](name.md) compila como **NULL** em compilações de varejo, para que as cadeias de caracteres estáticas apareçam somente em compilações de depuração. Para obter mais informações, consulte [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseObject**](cbaseobject.md)
</dt> </dl>

 

 




