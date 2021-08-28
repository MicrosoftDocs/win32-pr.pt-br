---
description: Método CBaseDispatch.GetTypeInfo – o método GetTypeInfo recupera as informações de tipo para o objeto , que pode ser usado para obter as informações de tipo para uma interface.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076676"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Método CBaseDispatch.GetTypeInfo

O método recupera as informações de tipo para o objeto , que pode ser usado `GetTypeInfo` para obter as informações de tipo para uma interface.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* 
</dt> <dd>

Referência a um IID (identificador de interface) que especifica a interface.

</dd> <dt>

*itinfo* 
</dt> <dd>

Digite informações a retornar. Deve ser zero.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificador de localidade.

</dd> <dt>

*Pptinfo* 
</dt> <dd>

Endereço de uma variável que recebe um **ponteiro ITypeInfo.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                             | Descrição                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                            |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>               | Argumento de ponteiro **NULL.**<br/>          |
| <dl> <dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | O *parâmetro itinfo* não é zero.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método se comporta como o **método IDispatch::GetTypeInfo.** No entanto, ele inclui um parâmetro adicional, *riid*, que especifica a interface para a qual recuperar informações de tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




