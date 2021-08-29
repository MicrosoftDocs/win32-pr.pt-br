---
title: MCIWNDM_PLAYREVERSE mensagem (Vfw.h)
description: A mensagem MCIWNDM PLAYREVERSE reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a \_ reprodução.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5664ea53f73745648e668a78a6dc5f6da28a9cb27d54b96fced09523f655ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037966"
---
# <a name="mciwndm_playreverse-message"></a>Mensagem MCIWNDM \_ PLAYREVERSE

A **mensagem MCIWNDM \_ PLAYREVERSE** reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayReverse.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





