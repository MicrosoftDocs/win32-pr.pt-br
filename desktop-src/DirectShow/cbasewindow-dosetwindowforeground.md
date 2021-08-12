---
description: O método DoSetWindowForeground leva a janela para o primeiro plano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Método CBaseWindow.DoSetWindowForeground (Winutil.h)
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
ms.openlocfilehash: 4f0d0dd99f5e2c5e5afffb78066a9380c56f744a4ba54b64bf987df15ea58862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658015"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>Método CBaseWindow.DoSetWindowForeground

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

Valor booliana que especifica se o foco da janela deve ser determinado. Se o valor for **TRUE,** a janela obtém o foco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




