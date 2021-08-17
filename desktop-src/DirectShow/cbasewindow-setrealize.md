---
description: O método setrealize especifica se a janela do percebe as paletas.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Método CBaseWindow. setrealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825a020b73bc74b38a32daa6f6870b76a009f5b8090e253370c77dfce7d7dc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954556"
---
# <a name="cbasewindowsetrealize-method"></a>Método CBaseWindow. setrealde

O `SetRealize` método especifica se a janela do percebe as paletas.

## <a name="syntax"></a>Sintaxe


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bRealize* 
</dt> <dd>

Valor booliano que especifica se as paletas devem ser concretizadas. Se **for true**, o método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) perceberá paletas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Por padrão, o método **SetPalette** percebe a paleta especificada. Chame esse método para alterar o comportamento padrão, de modo que as paletas sejam selecionadas, mas não realizadas. Esse método define a variável de membro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




