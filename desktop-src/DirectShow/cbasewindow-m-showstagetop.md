---
description: Mensagem privada que define o estilo da janela como WS \_ ex mais \_ alta.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membro CBaseWindow:: m_ShowStageTop (Winutil. h)'
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
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749624"
---
# <a name="cbasewindowm_showstagetop-member"></a>Membro de CBaseWindow:: m \_ ShowStageTop

Mensagem privada que define o estilo da janela como WS \_ ex mais \_ alta.

## <a name="syntax"></a>Sintaxe


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Comentários

Os renderizadores de vídeo devem enviar essa mensagem para a janela se mudarem para o modo de tela inteira.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




