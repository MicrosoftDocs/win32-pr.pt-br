---
title: MM_JOY2BUTTONUP mensagem (Mmsystem.h)
description: A mensagem MM \_ MM2BUTTONUP notifica a janela que capturou o button KIBID2 de que um botão foi liberado.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP mensagem Windows Multimídia
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
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557306"
---
# <a name="mm_joy2buttonup-message"></a>Mensagem \_ MM MMBUTTONUP

A **mensagem MM \_ MM2BUTTONUP** notifica a janela que capturou o button KIBID2 de que um botão foi liberado.


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
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**BUTTON DE \_ BOTÃO1CHG**</dt> </dl> | O primeiro botão de botão de mouse alterou o estado.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**BUTTON \_ BUTTON2CHG**</dt> </dl> | O segundo botão de button alterou o estado.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**BUTTON \_ BUTTON3CHG**</dt> </dl> | O terceiro botão de botão de botão alterou o estado.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**BUTTON \_ DE BOTÃO4CHG**</dt> </dl> | O quarto botão de button do button alterou o estado.<br/> |



 

e um ou mais dos seguintes:



| Valor                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**BOTÃO DE \_ BOTÃO1**</dt> </dl> | O primeiro botão de button é pressionado.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**JOY \_ BUTTON2**</dt> </dl> | O segundo botão de button é pressionado.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**BOTÃO DE \_ BOTÃO3**</dt> </dl> | O terceiro botão de button é pressionado.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**BOTÃO DE \_ BOTÃO4**</dt> </dl> | O quarto botão de button é pressionado.<br/> |



 

</dd> <dt>

**Xpos** 
</dt> <dd>

As coordenadas X do quadrante em relação ao canto superior esquerdo da área do cliente.

</dd> <dt>

**Ypos** 
</dt> <dd>

A coordenada Y do quadrante em relação ao canto superior esquerdo da área do cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensagens de Multimídia Dols](multimedia-joystick-messages.md)
</dt> </dl>

 

 





