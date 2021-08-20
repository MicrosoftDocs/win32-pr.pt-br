---
description: Mensagem privada que define o estilo da janela como WS \_ EX \_ TOPMOST.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: Membro CBaseWindow::m_ShowStageTop (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dbd8943b297d6e33f3b86a62c7e67dd2039a6b99d316061be30a4c3016711c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016514"
---
# <a name="cbasewindowm_showstagetop-member"></a>Membro CBaseWindow::m \_ ShowStageTop

Mensagem privada que define o estilo da janela como WS \_ EX \_ TOPMOST.

## <a name="syntax"></a>Sintaxe


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Comentários

Os renderadores de vídeo deverão enviar essa mensagem para a janela se alternarem para o modo de tela inteira.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




