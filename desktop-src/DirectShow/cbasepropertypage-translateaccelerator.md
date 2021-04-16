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
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747402"
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

## <a name="return-value"></a>Retornar valor

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Substitua esse método se desejar fornecer aceleradores de teclado para a página de propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




