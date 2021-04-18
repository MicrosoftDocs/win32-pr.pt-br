---
title: Estilos de controle TrackBar (CommCtrl. h)
description: Esta seção contém informações sobre os estilos usados com controles TrackBar.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771690"
---
# <a name="trackbar-control-styles"></a>Estilos de controle TrackBar

Esta seção contém informações sobre os estilos usados com controles TrackBar.



| Constante                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**\_AUTOtiques TBS**</dt> </dl>                      | O controle TrackBar tem uma marca de escala para cada incremento em seu intervalo de valores. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS \_ Vert**</dt> </dl>                                     | O controle TrackBar é orientado verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**\_na horizontal TBS**</dt> </dl>                                     | O controle TrackBar é orientado horizontalmente. Essa é a orientação padrão. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**superior de TBS \_**</dt> </dl>                                        | O controle TrackBar exibe as marcas de escala acima do controle. Esse estilo é válido somente com TBS \_ na horizontal. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**inferior de TBS \_**</dt> </dl>                               | O controle TrackBar exibe as marcas de escala abaixo do controle. Esse estilo é válido somente com TBS \_ na horizontal. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS \_ restantes**</dt> </dl>                                     | O controle TrackBar exibe as marcas de escala à esquerda do controle. Esse estilo é válido somente com TBS \_ vertes. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS \_ à direita**</dt> </dl>                                  | O controle TrackBar exibe as marcas de escala à direita do controle. Esse estilo é válido somente com TBS \_ vertes. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ ambos**</dt> </dl>                                     | O controle TrackBar exibe marcas de escala em ambos os lados do controle. Isso será tanto de cima quanto de baixo quando usado com TBS \_ na horizontal ou Left e Right, se usado com TBS \_ Vert. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TBS \_ NOtiques**</dt> </dl>                            | O controle TrackBar não exibe nenhuma marca de escala. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**\_ENABLESELRANGE TBS**</dt> </dl>       | O controle TrackBar exibe apenas um intervalo de seleção. As marcas de escala nas posições inicial e final de um intervalo de seleção são exibidas como triângulos (em vez de traços verticais) e o intervalo de seleção é realçado. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**\_Cadeia TBS**</dt> </dl>                | O controle TrackBar permite que o tamanho do controle deslizante seja alterado com a mensagem [**tbm \_ SETTHUMBLENGTH**](tbm-setthumblength.md) . <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOthumb**</dt> </dl>                            | O controle TrackBar não exibe um controle deslizante. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_dicas de ferramenta TBS**</dt> </dl>                         | [Versão 4,70](common-control-versions.md). O controle TrackBar dá suporte a dicas de ferramenta. Quando um controle TrackBar é criado usando esse estilo, ele cria automaticamente um controle de dica de ferramenta padrão que exibe a posição atual do controle deslizante. Você pode alterar onde as dicas de ferramenta são exibidas usando a mensagem [**tbm \_ SETTIPSIDE**](tbm-settipside.md) . <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ invertidos**</dt> </dl>                         | [Versão 5,80.](common-control-versions.md) Esse bit de estilo é usado para trackbars "invertido", em que um número menor indica "mais alto" e um número maior indica "menor". Ele não tem efeito sobre o controle; é simplesmente um rótulo que pode ser verificado para determinar se um TrackBar é normal ou invertido.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**\_DOWNISLEFT TBS**</dt> </dl>                   | Por padrão, o controle TrackBar usa igual à direita e superior igual à esquerda. Use o \_ estilo DOWNISLEFT TBS para inverter o padrão, deixando igual esquerdo e superior igual direito. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**\_NOTIFYBEFOREMOVE TBS**</dt> </dl> | [Versão 6, 0](common-control-versions.md) e **Windows Vista.** TrackBar deve notificar o pai antes de reposicionar o controle deslizante devido à ação do usuário (habilita o ajuste). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**\_TRANSPARENTBKGND TBS**</dt> </dl> | [Versão 6, 0](common-control-versions.md) e **Windows Vista.** O plano de fundo é pintado pelo pai por meio da mensagem do WM \_ fileclient. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





