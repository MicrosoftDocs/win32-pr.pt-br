---
description: 'O método move posiciona e redimensiona a caixa de diálogo. Esse método implementa o método IPropertyPage:: move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Método CBasePropertyPage. Move (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750697"
---
# <a name="cbasepropertypagemove-method"></a>Método CBasePropertyPage. move

O `Move` método posiciona e redimensiona a caixa de diálogo. Esse método implementa o método **IPropertyPage:: move** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que contém as informações de posicionamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




