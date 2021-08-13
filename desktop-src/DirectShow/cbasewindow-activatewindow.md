---
description: O método ActivateWindow tamanhos da janela de acordo com os requisitos da classe derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow.ActivateWindow (Winutil.h)
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
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658239"
---
# <a name="cbasewindowactivatewindow-method"></a>Método CBaseWindow.ActivateWindow

O `ActivateWindow` método tamanho da janela de acordo com os requisitos da classe derivada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | A janela já foi ativada.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esses métodos chamam o [**método CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar o tamanho da janela. A classe derivada deve substituir **GetDefaultRect** para retornar o tamanho das imagens que serão exibidas.

Se a janela já estiver ativa, chamar move a janela para a parte superior da ordem Z, mas não `ActivateWindow` resize a janela. O mesmo será verdadeiro se a janela tiver um pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




