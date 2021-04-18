---
description: O método CreateInstance chama a função de criação de objeto para a classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Método CFactoryTemplate. CreateInstance (combase. h)
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
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750046"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Método CFactoryTemplate. CreateInstance

O `CreateInstance` método chama a função de criação de objeto para a classe.

## <a name="syntax"></a>Sintaxe


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de agregação.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma instância do objeto de classe.

## <a name="remarks"></a>Comentários

O método **IClassFactory:: CreateInstance** chama esse método de classe. Esse método chama a função apontada pela variável de membro [**CFactoryTemplate:: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




