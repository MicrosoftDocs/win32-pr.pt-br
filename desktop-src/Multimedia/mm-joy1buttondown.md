---
title: Mensagem de MM_JOY1BUTTONDOWN (mmsystem. h)
description: A \_ mensagem mm JOY1BUTTONDOWN notifica a janela que capturou o joystick JOYSTICKID1 de que um botão foi pressionado.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- mensagem de MM_JOY1BUTTONDOWN Windows multimídia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137187"
---
# <a name="mm_joy1buttondown-message"></a>\_Mensagem mm JOY1BUTTONDOWN

A mensagem **mm \_ JOY1BUTTONDOWN** notifica a janela que CAPTUROU o joystick JOYSTICKID1 de que um botão foi pressionado.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica o botão que alterou o estado e os botões que são pressionados. Pode ser um dos seguintes:



| Requisito | Valor |
|-----------------|-------------------------------------------|
| BUTTON1CHG de alegria \_ | O primeiro botão de joystick alterou o estado.  |
| BUTTON2CHG de alegria \_ | O segundo botão de joystick alterou o estado. |
| BUTTON3CHG de alegria \_ | O terceiro botão de joystick alterou o estado.  |
| BUTTON4CHG de alegria \_ | O quarto botão de joystick alterou o estado. |



 

e um ou mais dos seguintes:



| Requisito | Valor |
|--------------|------------------------------------|
| JOY \_ Button1 | O primeiro botão de joystick é pressionado.  |
| JOY \_ Button1 | O segundo botão de joystick é pressionado. |
| BUTTON3 de alegria \_ | O terceiro botão de joystick é pressionado.  |
| BUTTON4 de alegria \_ | O quarto botão de joystick é pressionado. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

A coordenada x do joystick em relação ao canto superior esquerdo da área do cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.

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

 

 





