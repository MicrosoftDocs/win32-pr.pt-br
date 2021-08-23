---
description: Sinalizador que especifica se a janela publica ou envia sua mensagem de destruição.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070b94cc75fa3fb2d9b5983901abc2406b2e601ec3370323854905708ee681f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954605"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Membro de CBaseWindow:: m \_ bDoPostToDestroy

Sinalizador que especifica se a janela publica ou envia sua mensagem de destruição. Se **for true**, o método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usará a função **CreateMessage** para enviar a si mesmo uma mensagem de destruição privada. Se **for false**, **DoneWithWindow** usará a função **SendMessage** para enviar a mensagem. Por padrão, o valor é **false**.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




