---
description: O método DoSetWindowForeground traz a janela para o primeiro plano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Método CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751696"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>Método CBaseWindow. DoSetWindowForeground

O `DoSetWindowForeground` método leva a janela para o primeiro plano.

## <a name="syntax"></a>Sintaxe


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bFocus* 
</dt> <dd>

Valor booliano que especifica se o foco da janela deve ser fornecido. Se o valor for **true**, a janela ganha foco.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




