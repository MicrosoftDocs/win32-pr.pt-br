---
title: Mensagem de MM_JOY1ZMOVE (mmsystem. h)
description: A \_ mensagem mm JOY1ZMOVE notifica a janela que capturou o joystick JOYSTICKID1 que a posição do joystick no eixo z foi alterada.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- mensagem de MM_JOY1ZMOVE Windows multimídia
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b0efe11870ac822f7fe8aa0f7aa1deb4856bd8f1394bd1533362d78a3aee00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065536"
---
# <a name="mm_joy1zmove-message"></a>\_Mensagem mm JOY1ZMOVE

A mensagem **mm \_ JOY1ZMOVE** notifica a janela que CAPTUROU o joystick JOYSTICKID1 que a posição do joystick no eixo z foi alterada.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica os botões que são pressionados. Pode ser um ou mais dos seguintes valores:



| Requisito | Valor |
|--------------|------------------------------------|
| JOY \_ Button1 | O primeiro botão de joystick é pressionado.  |
| JOY \_ Button1 | O segundo botão de joystick é pressionado. |
| BUTTON3 de alegria \_ | O terceiro botão de joystick é pressionado.  |
| BUTTON4 de alegria \_ | O quarto botão de joystick é pressionado. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

A coordenada z do joystick.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensagens do joystick de multimídia](multimedia-joystick-messages.md)
</dt> </dl>

 

 





