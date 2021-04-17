---
description: Ocorre quando o usuário move o mouse enquanto o mouse está sobre o controle InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: Evento InkEdit. MouseMove (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749716"
---
# <a name="inkeditmousemove-event"></a>Evento InkEdit. MouseMove

Ocorre quando o usuário move o mouse enquanto o mouse está sobre o controle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MouseMove(
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

Um membro da enumeração [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica quais botões do mouse são pressionados.



| Valor                                                                                                                                                            | Significado                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**Não \_ BOTÃO**</dt> </dl>             | Padrão. Nenhum botão do mouse foi pressionado. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**À esquerda \_ BOTÃO**</dt> </dl>       | O botão esquerdo do mouse foi pressionado. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**À direita \_ BOTÃO**</dt> </dl>    | O botão direito do mouse foi pressionado. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**Meio \_ BOTÃO**</dt> </dl> | O botão do meio do mouse foi pressionado. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Um membro da enumeração [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais teclas modificadoras são pressionadas no momento do evento.



| Valor                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Especifica que a tecla SHIFT foi usada como um modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controle** do</dt> </dl> | Especifica que a tecla CTRL foi usada como um modificador. <br/>  |
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

## <a name="return-value"></a>Retornar valor

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se um botão do mouse for pressionado enquanto o ponteiro estiver sobre um controle [InkEdit](inkedit-control-reference.md) , esse controle capturará o mouse e receberá todos os eventos do mouse até e incluindo o último evento [**MouseUp**](inkedit-mouseup.md) . Isso implica que as coordenadas do ponteiro do mouse (x, y) retornadas por um evento do mouse talvez nem sempre estejam na área interna do objeto que as recebe.

Se os botões do mouse forem pressionados sucessivamente, o objeto que captura o mouse após o primeiro pressionamento receberá todos os eventos do mouse até que todos os botões sejam liberados.

O evento **MouseMove** é gerado continuamente à medida que o ponteiro do mouse se move entre objetos. A menos que outro objeto tenha capturado o mouse, um controle [InkEdit](inkedit-control-reference.md) reconhece um evento **MouseMove** sempre que a posição do mouse está dentro de suas bordas.

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeMouseMove DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controle de evento InkEdit do MouseDown \[\]**](inkedit-mousedown.md)
</dt> <dt>

[**Controle de evento InkEdit do MouseUp \[\]**](inkedit-mouseup.md)
</dt> </dl>

 

