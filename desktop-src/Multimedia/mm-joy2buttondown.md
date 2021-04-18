---
title: Mensagem de MM_JOY2BUTTONDOWN (mmsystem. h)
description: A \_ mensagem mm JOY2BUTTONDOWN notifica a janela que capturou o joystick JOYSTICKID2 de que um botão foi pressionado.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- Multimídia do Windows de mensagem MM_JOY2BUTTONDOWN
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759199"
---
# <a name="mm_joy2buttondown-message"></a>\_Mensagem mm JOY2BUTTONDOWN

A mensagem **mm \_ JOY2BUTTONDOWN** notifica a janela que CAPTUROU o joystick JOYSTICKID2 de que um botão foi pressionado.


```C++
MM_JOY2BUTTONDOWN 
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

 

 





