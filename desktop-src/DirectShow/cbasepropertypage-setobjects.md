---
description: 'O método SetObjects fornece ponteiros IUnknown para os objetos associados à página de propriedades. Esse método implementa o método IPropertyPage:: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage. SetObjects (cProp. h)
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
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758244"
---
# <a name="cbasepropertypagesetobjects-method"></a>Método CBasePropertyPage. SetObjects

O `SetObjects` método fornece ponteiros **IUnknown** para os objetos associados à página de propriedades. Esse método implementa o método **IPropertyPage:: SetObjects** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cObjects* 
</dt> <dd>

Especifica o número de ponteiros **IUnknown** na matriz especificada por *ppunk*.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Especifica uma matriz de ponteiros **IUnknown** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/>        |



 

## <a name="remarks"></a>Comentários

Embora *ppunk* especifique uma matriz de ponteiros **IUnknown** , a classe **CBasePropertyPage** é projetada apenas para dar suporte a um objeto associado. Se *CObjects* for maior que 1, o método retornará E será \_ inesperado.

Se *CObjects* for igual a 1, esse método chamará o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) . Se *CObjects* for igual a 0, esse método chamará o método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) . A classe derivada deve substituir esses dois métodos; para obter detalhes, consulte os comentários para esses métodos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




