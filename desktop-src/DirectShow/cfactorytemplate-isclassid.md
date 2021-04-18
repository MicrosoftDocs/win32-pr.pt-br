---
description: O método isclassidid determina se um CLSID corresponde a esse modelo de classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Método CFactoryTemplate. isclassidid (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751489"
---
# <a name="cfactorytemplateisclassid-method"></a>Método CFactoryTemplate. isclassidid

O `IsClassID` método determina se um CLSID corresponde a esse modelo de classe.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rclsid* 
</dt> <dd>

Referência a um CLSID.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o *parâmetro rclsid* for o mesmo CLSID que a variável de membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) ou, caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




