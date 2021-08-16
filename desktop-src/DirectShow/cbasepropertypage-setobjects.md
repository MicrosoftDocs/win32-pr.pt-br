---
description: O método SetObjects fornece ponteiros IUnknown para os objetos associados à página de propriedades. Esse método implementa o método IPropertyPage::SetObjects.
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage.SetObjects (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5c29d1ddc646ef05faad2bc283887265e8b85109fcb679924d9a5641ef13fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823021"
---
# <a name="cbasepropertypagesetobjects-method"></a>Método CBasePropertyPage.SetObjects

O `SetObjects` método fornece **ponteiros IUnknown** para os objetos associados à página de propriedades. Esse método implementa o **método IPropertyPage::SetObjects.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cobjects* 
</dt> <dd>

Especifica o número de **ponteiros IUnknown** na matriz especificada por *ppUnk.*

</dd> <dt>

*ppUnk* 
</dt> <dd>

Especifica uma matriz de **ponteiros IUnknown.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Argumento de ponteiro **NULL.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Falha inesperada.<br/>        |



 

## <a name="remarks"></a>Comentários

Embora *ppUnk* especifique uma matriz de ponteiros **IUnknown,** a classe **CBasePropertyPage** foi projetada apenas para dar suporte a um objeto associado. Se *cObjects for* maior que 1, o método retornará E \_ UNEXPECTED.

Se *cObjects* for igual a 1, esse método chamará o [**método CBasePropertyPage::OnConnect.**](cbasepropertypage-onconnect.md) Se *cObjects* for igual a 0, esse método chamará o [**método CBasePropertyPage::OnDisconnect.**](cbasepropertypage-ondisconnect.md) A classe derivada deve substituir ambos os métodos; Para obter detalhes, consulte os comentários para esses métodos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




