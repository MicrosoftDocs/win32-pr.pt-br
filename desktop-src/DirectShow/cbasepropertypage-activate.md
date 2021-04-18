---
description: 'O método Activate cria a janela da caixa de diálogo. Esse método implementa o método IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Método CBasePropertyPage. Activate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756638"
---
# <a name="cbasepropertypageactivate-method"></a>Método CBasePropertyPage. Activate

O `Activate` método cria a janela da caixa de diálogo. Esse método implementa o método **IPropertyPage:: Activate** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* 
</dt> <dd>

Identificador para a janela pai da caixa de diálogo.

</dd> <dt>

*prect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que contém informações de posicionamento para a caixa de diálogo.

</dd> <dt>

*fModal* 
</dt> <dd>

Valor booliano que indica se o quadro da caixa de diálogo é modal (**true**) ou sem janela restrita (**false**).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                   | Descrição                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo** .<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Falha inesperada.<br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




