---
title: MCIWNDM_SETPALETTE mensagem (Vfw.h)
description: A mensagem SETPALETTE MCIWNDM envia um alça de paleta para o dispositivo MCI associado \_ à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525226"
---
# <a name="mciwndm_setpalette-message"></a>Mensagem SETPALETTE MCIWNDM \_

A **mensagem \_ SETPALETTE MCIWNDM** envia um alça de paleta para o dispositivo MCI associado à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Alça da paleta.

</dd> </dl>

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

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





