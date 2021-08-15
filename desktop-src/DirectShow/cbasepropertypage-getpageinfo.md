---
description: 'O método GetPageInfo recupera informações sobre a página de propriedades. Esse método implementa o método IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Método CBasePropertyPage. GetPageInfo (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: badb0678faa85b70dfa848bba7538319b905feea440339e24285f3d64b59d61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823156"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>Método CBasePropertyPage. GetPageInfo

O `GetPageInfo` método recupera informações sobre a página de propriedades. Esse método implementa o método **IPropertyPage:: GetPageInfo** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Ponteiro para uma estrutura **PROPPAGEINFO** alocada pelo chamador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                   | Descrição                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




