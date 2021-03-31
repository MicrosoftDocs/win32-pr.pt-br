---
title: Sinalizadores de ponteiro
description: Os valores que podem aparecer no campo pointerFlags da estrutura de POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644857"
---
# <a name="pointer-flags"></a>Sinalizadores de ponteiro

Os valores que podem aparecer no campo **pointerFlags** da estrutura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Padrão


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica a chegada de um novo ponteiro.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que esse ponteiro continua a existir. Quando esse sinalizador não é definido, ele indica que o ponteiro tem um intervalo de detecção à esquerda.

Esse sinalizador normalmente não é definido somente quando um ponteiro em foco deixa o intervalo de detecção (**POINTER_FLAG_UPDATE** é definido) ou quando um ponteiro em contato com uma superfície de janela sai do intervalo de detecção (**POINTER_FLAG_UP** é definido).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que esse ponteiro está em contato com a superfície digitalizadora. Quando esse sinalizador não é definido, ele indica um ponteiro em foco.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica uma ação primária, análoga a um botão esquerdo do mouse para baixo.

Um ponteiro de toque tem esse sinalizador definido quando ele está em contato com a superfície digitalizadora.

Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora sem botões pressionados.

Um ponteiro do mouse tem esse sinalizador definido quando o botão esquerdo do mouse está inativo.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica uma ação secundária, análoga a um botão direito do mouse.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta tem esse sinalizador definido quando está em contato com a superfície digitalizadora com o botão de rosca de caneta pressionado.

Um ponteiro do mouse tem esse sinalizador definido quando o botão direito do mouse está inativo.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Análogo a um botão de roda do mouse para baixo.

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o botão da roda do mouse está inativo.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Análogo a um botão do primeiro mouse estendido (XButton1).

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o botão do primeiro mouse estendido (XBUTTON1) está inoperante.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Análogo a um segundo botão do mouse estendido (XButton2).

Um ponteiro de toque não usa esse sinalizador.

Um ponteiro de caneta não usa esse sinalizador.

Um ponteiro do mouse tem esse sinalizador definido quando o segundo botão do mouse estendido (XBUTTON2) está inoperante.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que esse ponteiro foi designado como o ponteiro principal. Um ponteiro principal é um único ponteiro que pode executar ações além daquelas disponíveis para ponteiros não primários. Por exemplo, quando um ponteiro principal faz contato com uma superfície da janela, ele pode fornecer à janela uma oportunidade de ativação, enviando a ele uma mensagem [**WM_POINTERACTIVATE**](wm-pointeractivate.md) .

O ponteiro principal é identificado de todas as interações atuais do usuário no sistema (mouse, toque, caneta e assim por diante). Como tal, o ponteiro principal pode não estar associado ao seu aplicativo. O primeiro contato em uma interação multitoque é definido como o ponteiro principal. Depois que um ponteiro principal é identificado, todos os contatos devem ser levantados antes que um novo contato possa ser identificado como um ponteiro principal. Para aplicativos que não processam a entrada do ponteiro, somente os eventos do ponteiro principal são promovidos para eventos do mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



Confiança é uma sugestão do dispositivo de origem sobre se o ponteiro representa uma interação pretendida ou acidental, que é especialmente relevante para ponteiros de PT_TOUCH em que uma interação acidental (como com a palma da mão) pode disparar a entrada. A presença desse sinalizador indica que o dispositivo de origem tem alta confiança de que essa entrada faz parte de uma interação pretendida.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Indica que o ponteiro está se deparando de forma anormal, por exemplo, quando o sistema recebe uma entrada inválida para o ponteiro ou quando um dispositivo com ponteiros ativos faz parte abruptamente. Se o aplicativo que está recebendo a entrada estiver em uma posição para fazer isso, ele deverá tratar a interação como não concluída e inverter os efeitos do ponteiro preocupado.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Indica que esse ponteiro fez a transição para um estado inativo; ou seja, ele fez contato com a superfície digitalizadora.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que se trata de uma atualização simples que não inclui alterações de estado de ponteiro.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica que esse ponteiro fez a transição para um estado ativo; ou seja, o contato com a superfície do digitalizador terminou.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Indica a entrada associada a uma roda de ponteiro. Para ponteiros do mouse, isso é equivalente à ação da roda de rolagem do mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Indica a entrada associada a um ponteiro h-Wheel. Para ponteiros do mouse, isso é equivalente à ação da roda de rolagem horizontal do mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Indica que esse ponteiro foi capturado por (associado a) outro elemento e o elemento original perdeu a captura (consulte [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Indica que esse ponteiro tem uma transformação associada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

XBUTTON1 e XBUTTON2 são botões adicionais usados em vários dispositivos de mouse. Eles retornam os mesmos dados que os botões padrão do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

