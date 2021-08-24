---
description: Ocorre quando o usuário libera um botão do mouse enquanto o mouse está sobre o controle InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit.MouseUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483333b246e84d2a9ed6f354198ebce5cd147ddb4fd3ccb5e2834d1802a0b744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712656"
---
# <a name="inkeditmouseup-event"></a>Evento InkEdit.MouseUp

Ocorre quando o usuário libera um botão do mouse enquanto o mouse está sobre o [controle InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Botão* 
</dt> <dd>

Um membro da [**enumeração MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica quais botões do mouse foram liberados.



| Valor                                                                                                                                                            | Significado                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NÃO \_ BOTÃO**</dt> </dl>             | Padrão. Nenhum botão do mouse foi pressionado. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**ESQUERDA \_ BOTÃO**</dt> </dl>       | O botão esquerdo do mouse foi pressionado. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**DIREITA \_ BOTÃO**</dt> </dl>    | O botão direito do mouse foi pressionado. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ BOTÃO**</dt> </dl> | O botão do meio do mouse foi pressionado. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Um membro da [**enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais chaves modificadores são desfeitas no momento do evento.



| Valor                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Deslocamento de \_ IKM**</dt> </dl>             | Especifica que a tecla SHIFT foi usada como um modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controle**</dt> </dl> | Especifica que a tecla CTRL foi usada como um modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que a tecla ALT foi usada como um modificador. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

A coordenada x atual, em pixels, do ponteiro do mouse.

</dd> <dt>

*yMouse* 
</dt> <dd>

A coordenada y atual, em pixels, do ponteiro do mouse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Se um botão do mouse for pressionado enquanto o ponteiro estiver sobre um controle [InkEdit,](inkedit-control-reference.md) esse controle capturará o mouse e receberá todos os eventos do mouse até e incluindo o último **evento MouseUp.** Isso implica que as coordenadas de ponteiro do mouse (x, y) retornadas por um evento do mouse nem sempre estão na área interna do objeto que as recebe.

Se os botões do mouse são pressionados em sucessão, o objeto que captura o mouse após a primeira pressionada recebe todos os eventos do mouse até que todos os botões sejam liberados.

Esse método de evento é definido na interface **\_ IInkEditEvents.** A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ IeeMouseUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked.h (também requer \_ i.c com tinta)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controle InkEdit do evento MouseDown \[\]**](inkedit-mousedown.md)
</dt> <dt>

[**Controle MouseMove Event \[ InkEdit\]**](inkedit-mousemove.md)
</dt> </dl>

 

