---
description: O método CreateInstance chama a função de criação de objeto para a classe .
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Método CFactoryTemplate.CreateInstance (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074200"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Método CFactoryTemplate.CreateInstance

O `CreateInstance` método chama a função de criação de objeto para a classe .

## <a name="syntax"></a>Sintaxe


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Punk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de agreging.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma instância do objeto de classe.

## <a name="remarks"></a>Comentários

O **método IClassFactory::CreateInstance** chama esse método de classe. Esse método chama a função apontada pela variável de membro [**CFactoryTemplate::m \_ lpfnNew.**](cfactorytemplate-m-lpfnnew.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




