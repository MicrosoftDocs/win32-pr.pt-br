---
description: O método GetTypeInfo recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780867"
---
# <a name="cmediapositiongettypeinfo-method"></a>Método CMediaPosition. GetTypeInfo

O `GetTypeInfo` método recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*itinfo* 
</dt> <dd>

Digite as informações a serem retornadas. Deve ser zero.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificador de localidade.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro **ITypeInfo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                             | Descrição                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                            |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>          |
| <dl> <dt>**Digite \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | O parâmetro *itinfo* não é zero.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




