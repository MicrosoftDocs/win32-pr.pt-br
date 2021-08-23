---
title: Sinalizadores de mensagem de ponteiro
description: Valores usados em várias macros de ponteiro (consulte Macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 70d329c6a48eb92f6f50ff49d5543c2aaf5cfc3ce9ef23b48290c7aa029eecf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602328"
---
# <a name="pointer-message-flags"></a>Sinalizadores de mensagem de ponteiro

Valores usados em várias macros de ponteiro (consulte [Macros](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica a chegada de um novo ponteiro.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que esse ponteiro continua a existir. Quando esse sinalizador não está definido, ele indica que o ponteiro tem o intervalo de detecção à esquerda.

Normalmente, esse sinalizador não é definido somente quando um ponteiro de foco sai do intervalo de detecção **(POINTER_FLAG_UPDATE** está definido) ou quando um ponteiro em contato com uma superfície de janela sai do intervalo de detecção **(POINTER_FLAG_UP** está definido).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que esse ponteiro está em contato com a superfície do digitalizador. Quando esse sinalizador não está definido, ele indica um ponteiro de foco.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica uma ação primária, análoga a um botão esquerdo do mouse para baixo.

Um ponteiro de toque tem esse sinalizador definido quando ele está em contato com a superfície do digitalizador.

Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície do digitalizador sem botões pressionados.

Um ponteiro do mouse tem esse sinalizador definido quando o botão esquerdo do mouse está ino mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica uma ação secundária, análoga a um botão direito do mouse para baixo.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície do digitalizador com o botão de caneta pressionado.

Um ponteiro do mouse tem esse sinalizador definido quando o botão direito do mouse está ino mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Análogo a um botão de roda do mouse para baixo.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o botão de roda do mouse está ino mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Análogo a um primeiro botão estendido do mouse (XButton1) para baixo.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o primeiro botão estendido do mouse (XBUTTON1) está inoc baixo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Análogo a um segundo botão de mouse estendido (XButton2) para baixo.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o segundo botão estendido do mouse (XBUTTON2) está inoc baixo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que esse ponteiro foi designado como o ponteiro primário. Um ponteiro primário é um único ponteiro que pode executar ações além daquelas disponíveis para ponteiros não primários. Por exemplo, quando um ponteiro primário faz contato com a superfície de uma janela, ele pode fornecer à janela uma oportunidade de ativar enviando uma mensagem WM_POINTERACTIVATE janela.

O ponteiro primário é identificado de todas as interações atuais do usuário no sistema (mouse, toque, caneta e assim por diante). Dessa forma, o ponteiro primário pode não estar associado ao seu aplicativo. O primeiro contato em uma interação com vários toques é definido como o ponteiro primário. Depois que um ponteiro primário é identificado, todos os contatos devem ser retirados antes que um novo contato possa ser identificado como um ponteiro primário. Para aplicativos que não processam a entrada de ponteiro, somente os eventos do ponteiro primário são promovidos para eventos do mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



A confiança é uma sugestão do dispositivo de origem sobre se o ponteiro representa uma interação pretendido ou acidental, que é especialmente relevante para ponteiros de PT_TOUCH em que uma interação acidental (como com a mão) pode disparar a entrada. A presença desse sinalizador indica que o dispositivo de origem tem alta confiança de que essa entrada faz parte de uma interação pretendido.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indica que o ponteiro está partindo de uma maneira anormal, como quando o sistema recebe entrada inválida para o ponteiro ou quando um dispositivo com ponteiros ativos sai de forma anormal. Se o aplicativo que recebe a entrada estiver em uma posição para fazer isso, ele deverá tratar a interação como não concluída e reverter os efeitos do ponteiro em questão.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

XBUTTON1 e XBUTTON2 são botões adicionais usados em muitos dispositivos do mouse. Eles retornam os mesmos dados que os botões padrão do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[Macros](macros.md)
</dt> </dl>

 

 





