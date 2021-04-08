---
title: Mensagem de MM_JOY1BUTTONUP (mmsystem. h)
description: A \_ mensagem mm JOY1BUTTONUP notifica a janela que capturou o joystick JOYSTICKID1 de que um botão foi liberado.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- Multimídia do Windows de mensagem MM_JOY1BUTTONUP
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086504"
---
# <a name="mm_joy1buttonup-message"></a>\_Mensagem mm JOY1BUTTONUP

A mensagem **mm \_ JOY1BUTTONUP** notifica a janela que CAPTUROU o joystick JOYSTICKID1 de que um botão foi liberado.


```C++
MM_JOY1BUTTONUP 
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

As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.

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

 

 





