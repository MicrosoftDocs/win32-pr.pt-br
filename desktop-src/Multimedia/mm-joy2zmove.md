---
title: Mensagem de MM_JOY2ZMOVE (mmsystem. h)
description: A \_ mensagem mm JOY2ZMOVE notifica a janela que capturou o joystick JOYSTICKID2 que a posição do joystick no eixo z foi alterada.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Multimídia do Windows de mensagem MM_JOY2ZMOVE
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788133"
---
# <a name="mm_joy2zmove-message"></a>\_Mensagem mm JOY2ZMOVE

A mensagem **mm \_ JOY2ZMOVE** notifica a janela que CAPTUROU o joystick JOYSTICKID2 que a posição do joystick no eixo z foi alterada.


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica os botões que são pressionados. Pode ser um ou mais dos valores a seguir.



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

 

 





