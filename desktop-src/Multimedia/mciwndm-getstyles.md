---
title: Mensagem de MCIWNDM_GETSTYLES (VFW. h)
description: A \_ mensagem GETestilos MCIWNDM recupera os sinalizadores que especificam os estilos de janela MCIWnd atuais usados por uma janela. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- mensagem de MCIWNDM_GETSTYLES Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783286"
---
# <a name="mciwndm_getstyles-message"></a>\_Mensagem de GETestilizas MCIWNDM

A **mensagem \_ getestilos MCIWNDM** recupera os sinalizadores que especificam os estilos de janela MCIWnd atuais usados por uma janela. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna um valor que representa os estilos atuais da janela MCIWnd. O valor de retorno é o operador de bits OR de MCIWnd de estilos de janela (sinalizadores MCIWNDF).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





