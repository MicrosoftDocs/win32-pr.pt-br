---
description: O método CreateInstance cria uma nova instância da classe CMemAllocator.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Método CMemAllocator.CreateInstance (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8682a667685f38cd7a73e091067a86f528f64e1ec110c473f50000c18ba4d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156015"
---
# <a name="cmemallocatorcreateinstance-method"></a>Método CMemAllocator.CreateInstance

O `CreateInstance` método cria uma nova instância da classe **CMemAllocator.**

## <a name="syntax"></a>Sintaxe


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Punk* 
</dt> <dd>

Ponteiro para o proprietário desse objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, de definido esse parâmetro como **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um novo **objeto CMemAllocator,** digitado como um **objeto CUnknown.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




