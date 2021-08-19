---
title: MM_JOY1MOVE mensagem (Mmsystem.h)
description: A mensagem MM MM MM1MOVE notifica a janela que capturou \_ o captou o HASID1 de que a posição do botão foi alterada.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8c8a71bc91b541bc17017fc2673bb6c0ed7e84a2de44ff312954b8f9915dc57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802441"
---
# <a name="mm_joy1move-message"></a>Mensagem \_ MM MM MM1MOVE

A **mensagem MM MM \_ MM1MOVE** notifica a janela que capturou o captou o HASID1 de que a posição do botão foi alterada.


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica os botões que são pressionados. Pode ser um ou mais dos seguintes valores:



| Requisito | Valor |
|--------------|------------------------------------|
| BOTÃO DE \_ BOTÃO1 | O primeiro botão de button é pressionado.  |
| JOY \_ BUTTON2 | O segundo botão de button é pressionado. |
| BOTÃO DE \_ BOTÃO3 | O terceiro botão de button é pressionado.  |
| BOTÃO DE \_ BOTÃO4 | O quarto botão de button é pressionado. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*Xpos*
</dt> <dd>

As coordenadas X do quadrante em relação ao canto superior esquerdo da área do cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*Ypos*
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

 

 





