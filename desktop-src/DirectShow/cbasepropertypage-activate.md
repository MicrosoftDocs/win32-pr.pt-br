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
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108516"
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

## <a name="return-value"></a>Valor retornado

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
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




