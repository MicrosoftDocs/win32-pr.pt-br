---
description: Método CBaseDispatch. GetTypeInfo – o método GetTypeInfo recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch. GetTypeInfo (Ctlutil. h)
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
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120114"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Método CBaseDispatch. GetTypeInfo

O `GetTypeInfo` método recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.

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

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                             | Descrição                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Sucesso.<br/>                            |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>          |
| <dl> <dt>**Digite \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | O parâmetro *itinfo* não é zero.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método se comporta como o método **IDispatch:: GetTypeInfo** . No entanto, ele inclui um parâmetro adicional, *riid*, que especifica a interface para a qual recuperar informações de tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




