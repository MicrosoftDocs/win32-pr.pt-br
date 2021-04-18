---
description: O método ActivateWindow dimensiona a janela de acordo com os requisitos da classe derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779561"
---
# <a name="cbasewindowactivatewindow-method"></a>Método CBaseWindow. ActivateWindow

O `ActivateWindow` método dimensiona a janela de acordo com os requisitos da classe derivada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | A janela já foi ativada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esses métodos chamam o método [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar o tamanho da janela. A classe derivada deve substituir **GetDefaultRect** para retornar o tamanho das imagens que serão exibidas.

Se a janela já estiver ativa, chamar `ActivateWindow` move a janela para a parte superior da ordem Z, mas não redimensiona a janela. O mesmo será verdadeiro se a janela tiver um pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




