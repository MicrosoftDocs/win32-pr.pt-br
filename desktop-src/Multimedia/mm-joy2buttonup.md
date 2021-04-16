---
title: Mensagem de MM_JOY2BUTTONUP (mmsystem. h)
description: A \_ mensagem mm JOY2BUTTONUP notifica a janela que capturou o joystick JOYSTICKID2 de que um botão foi liberado.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- Multimídia do Windows de mensagem MM_JOY2BUTTONUP
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811084"
---
# <a name="mm_joy2buttonup-message"></a>\_Mensagem mm JOY2BUTTONUP

A mensagem **mm \_ JOY2BUTTONUP** notifica a janela que CAPTUROU o joystick JOYSTICKID2 de que um botão foi liberado.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifica o botão que alterou o estado e os botões que são pressionados. Pode ser um dos seguintes:



| Valor                                                                                                                                                            | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**BUTTON1CHG de alegria \_**</dt> </dl> | O primeiro botão de joystick alterou o estado.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**BUTTON2CHG de alegria \_**</dt> </dl> | O segundo botão de joystick alterou o estado.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**BUTTON3CHG de alegria \_**</dt> </dl> | O terceiro botão de joystick alterou o estado.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**BUTTON4CHG de alegria \_**</dt> </dl> | O quarto botão de joystick alterou o estado.<br/> |



 

e um ou mais dos seguintes:



| Valor                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**JOY \_ Button1**</dt> </dl> | O primeiro botão de joystick é pressionado.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**JOY \_ Button1**</dt> </dl> | O segundo botão de joystick é pressionado.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**BUTTON3 de alegria \_**</dt> </dl> | O terceiro botão de joystick é pressionado.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**BUTTON4 de alegria \_**</dt> </dl> | O quarto botão de joystick é pressionado.<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.

</dd> <dt>

**yPos** 
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

 

 





