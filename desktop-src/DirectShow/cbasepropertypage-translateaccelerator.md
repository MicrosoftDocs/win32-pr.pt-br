---
description: 'O método TranslateAccelerator instrui a página de propriedades a processar um pressionamento de tecla. Esse método implementa o método IPropertyPage:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Método CBasePropertyPage. TranslateAccelerator (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc86d50c5692f48c7fb00b45228b13c88c96137473cee3609013f782a0a2d7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502836"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>Método CBasePropertyPage. TranslateAccelerator

O `TranslateAccelerator` método instrui a página de propriedades a processar um pressionamento de tecla. Esse método implementa o método **IPropertyPage:: TranslateAccelerator** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpMsg* 
</dt> <dd>

Ponteiro para uma estrutura **msg** que descreve a tecla para processar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Substitua esse método se desejar fornecer aceleradores de teclado para a página de propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




