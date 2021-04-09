---
title: Mensagem de MCIWNDM_PLAYREVERSE (VFW. h)
description: A \_ mensagem MCIWNDM PLAYREVERSE reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a reprodução.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYREVERSE
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
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085143"
---
# <a name="mciwndm_playreverse-message"></a>\_Mensagem MCIWNDM PLAYREVERSE

A mensagem **MCIWNDM \_ PLAYREVERSE** reproduz o conteúdo atual na direção inversa, começando na posição atual e terminando no início do conteúdo ou até que outro comando pare a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





