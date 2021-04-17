---
description: O método DoRealisePalette percebe a paleta atual da janela.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Método CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755602"
---
# <a name="cbasewindowdorealisepalette-method"></a>Método CBaseWindow. DoRealisePalette

O `DoRealisePalette` método percebe a paleta atual da janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bForceBackground* 
</dt> <dd>

Valor booliano que especifica se a paleta é forçada a ser uma paleta de plano de fundo. Para obter mais informações, consulte **SelectPalette** no SDK da plataforma.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Uma chamada interna para **GdiFlush** retornou um erro.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                            |



 

## <a name="remarks"></a>Comentários

O método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) chama esse método. Para definir uma nova paleta, chame o método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




