---
title: Up-Down estilos de controle (CommCtrl. h)
description: Esta seção lista os estilos usados ao criar controles de cima para baixo.
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749535"
---
# <a name="up-down-control-styles"></a>Up-Down estilos de controle

Esta seção lista os estilos usados ao criar controles de cima para baixo.



| Constante                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Posiciona o controle de cima para baixo ao lado da borda esquerda da janela do Buddy. A janela Buddy é movida para a direita e sua largura é diminuída para acomodar a largura do controle acima-abaixo.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Posiciona o controle de cima para baixo ao lado da borda direita da janela do Buddy. A largura da janela Buddy é diminuída para acomodar a largura do controle acima-abaixo.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS \_ ARROWKEYS**</dt> </dl>       | Faz com que o controle de cima para baixo aumente e reduza a posição quando as teclas seta para cima e seta para baixo são pressionadas.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTObuddy**</dt> </dl>       | Seleciona automaticamente a janela anterior na ordem z como a janela de amigo do controle de cima para baixo.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ na horizontal**</dt> </dl>                      | Faz com que as setas do controle de cima para baixo apontem para a esquerda e para a direita, em vez de para cima e para baixo.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Faz com que o controle exiba o comportamento de "acompanhamento dinâmico". Ou seja, ele realça a seta para cima e a seta para baixo no controle conforme o ponteiro passa sobre eles. Este estilo requer o Windows 98 ou o Windows 2000. Se o sistema estiver executando o Windows 95 ou o Windows NT 4,0, o sinalizador será ignorado. Para verificar se o rastreamento dinâmico está habilitado, chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOmilhares**</dt> </dl> | Não insere um separador de milhar entre cada três dígitos decimais. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Faz com que o controle de cima para baixo defina o texto da janela Buddy (usando a mensagem [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) ) quando a posição é alterada. O texto consiste na posição formatada como uma cadeia de caracteres decimal ou hexadecimal.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**\_encapsulamento de UDS**</dt> </dl>                      | Faz com que a posição seja "encapsulada" se for incrementada ou diminuída além do final ou do início do intervalo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

