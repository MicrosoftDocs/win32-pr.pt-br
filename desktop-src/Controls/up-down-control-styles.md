---
title: Up-Down de controle (CommCtrl.h)
description: Esta seção lista os estilos usados ao criar controles para cima e para baixo.
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
ms.openlocfilehash: 809ab4ce2c4d8670363dc7f0751ae4a3756ee7b4e5dc9b75c79986c3a56d359d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957695"
---
# <a name="up-down-control-styles"></a>Up-Down de controle

Esta seção lista os estilos usados ao criar controles para cima e para baixo.



| Constante                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Posiciona o controle para cima para baixo ao lado da borda esquerda da janela do parceiro. A janela do colega é movida para a direita e sua largura é reduzida para acomodar a largura do controle de cima para baixo.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Posiciona o controle para cima para baixo ao lado da borda direita da janela do colega. A largura da janela do parceiro é reduzida para acomodar a largura do controle de cima para baixo.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**TECLAS DE DIREÇÃO \_ DO UDS**</dt> </dl>       | Faz com que o controle para cima para baixo incremente e decremente a posição quando as teclas SETA PARA CIMA e SETA PARA BAIXO são pressionadas.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTOBUDDY**</dt> </dl>       | Seleciona automaticamente a janela anterior na ordem z como a janela do parceiro do controle de cima para baixo.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ HORZ**</dt> </dl>                      | Faz com que as setas do controle para cima para baixo apontem para a esquerda e para a direita em vez de para cima e para baixo.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Faz o controle exibir o comportamento de "acompanhamento a quente". Ou seja, ele realça a SETA PARA CIMA e a SETA PARA BAIXO no controle à medida que o ponteiro passa sobre eles. Esse estilo requer Windows 98 ou Windows 2000. Se o sistema estiver executando Windows 95 ou Windows NT 4.0, o sinalizador será ignorado. Para verificar se o acompanhamento a quente está habilitado, chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOTHOUSANDS**</dt> </dl> | Não insere um separador de milhares entre cada três dígitos decimais. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Faz com que o controle para cima para baixo de definir o texto da janela do parceiro (usando a mensagem [**WM \_ SETTEXT)**](/windows/desktop/winmsg/wm-settext) quando a posição é muda. O texto consiste na posição formatada como uma cadeia de caracteres decimal ou hexadecimal.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UDS \_ WRAP**</dt> </dl>                      | Faz com que a posição seja "wrap" se ela for incrementada ou decrementada além do término ou início do intervalo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

