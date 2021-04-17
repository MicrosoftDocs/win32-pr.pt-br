---
description: O método PrepareWindow cria a janela.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Método CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747596"
---
# <a name="cbasewindowpreparewindow-method"></a>Método CBaseWindow. PrepareWindow

O `PrepareWindow` método cria a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                            | Descrição         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método depois de criar o objeto. Esse método executa algumas escriturações iniciais e, em seguida, chama o método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) para criar a janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




