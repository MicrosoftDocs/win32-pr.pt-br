---
title: Mensagem de MCIWNDM_GETSTYLES (VFW. h)
description: A \_ mensagem GETestilos MCIWNDM recupera os sinalizadores que especificam os estilos de janela MCIWnd atuais usados por uma janela. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSTYLES
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
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768707"
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

 

 





