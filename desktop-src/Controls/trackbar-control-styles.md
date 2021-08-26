---
title: Estilos de controle trackbar (CommCtrl.h)
description: Esta seção contém informações sobre os estilos usados com controles de barra de faixa.
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
ms.openlocfilehash: 9165325c2d78ac6e4dc1ae69e410d293100de24cb8d38868475e99e49c0faaa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046016"
---
# <a name="trackbar-control-styles"></a>Estilos de controle da barra de faixas

Esta seção contém informações sobre os estilos usados com controles de barra de faixa.



| Constante                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**TBS \_ AUTOTICKS**</dt> </dl>                      | O controle trackbar tem uma marca de escala para cada incremento em seu intervalo de valores. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS \_ VERT**</dt> </dl>                                     | O controle trackbar é orientado verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ HORZ**</dt> </dl>                                     | O controle trackbar é orientado horizontalmente. Essa é a orientação padrão. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS \_ TOP**</dt> </dl>                                        | O controle trackbar exibe marcas de escala acima do controle. Esse estilo só é válido com TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS \_ BOTTOM**</dt> </dl>                               | O controle trackbar exibe marcas de escala abaixo do controle . Esse estilo só é válido com TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS \_ LEFT**</dt> </dl>                                     | O controle trackbar exibe marcas de escala à esquerda do controle. Esse estilo só é válido com TBS \_ VERT. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS \_ RIGHT**</dt> </dl>                                  | O controle de barra de faixa exibe marcas de escala à direita do controle. Esse estilo só é válido com TBS \_ VERT. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ BOTH**</dt> </dl>                                     | O controle de barra de faixa exibe marcas de escala em ambos os lados do controle. Isso será tanto superior quanto inferior quando usado com TBS HORZ ou à esquerda e à direita, se \_ usado com TBS \_ VERT. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TBS \_ NOTICKS**</dt> </dl>                            | O controle de barra de faixa não exibe nenhuma marca de escala. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TBS \_ ENABLESELRANGE**</dt> </dl>       | O controle de barra de faixa exibe apenas um intervalo de seleção. As marcas de escala nas posições inicial e final de um intervalo de seleção são exibidas como triângulos (em vez de traços verticais) e o intervalo de seleção é realçada. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TBS \_ FIXEDLENGTH**</dt> </dl>                | O controle de barra de faixa permite que o tamanho do controle deslizante seja alterado com a [**mensagem \_ TBM SETTHUMBLENGTH.**](tbm-setthumblength.md) <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOTHUMB**</dt> </dl>                            | O controle de barra de faixa não exibe um controle deslizante. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**DICAS DE \_ FERRAMENTA TBS**</dt> </dl>                         | [Versão 4.70.](common-control-versions.md) O controle trackbar dá suporte a dicas de ferramenta. Quando um controle de barra de faixa é criado usando esse estilo, ele cria automaticamente um controle de dica de ferramenta padrão que exibe a posição atual do controle deslizante. Você pode alterar onde as dicas de ferramenta são exibidas usando a [**mensagem \_ TBM SETTIPSIDE.**](tbm-settipside.md) <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ INVERTIDOS**</dt> </dl>                         | [Versão 5.80.](common-control-versions.md) Esse bit de estilo é usado para barras de faixa "invertidas", em que um número menor indica "mais alto" e um número maior indica "inferior". Ele não tem nenhum efeito sobre o controle; é simplesmente um rótulo que pode ser verificado para determinar se uma barra de faixa é normal ou invertida.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TBS \_ DOWNISLEFT**</dt> </dl>                   | Por padrão, o controle de barra de faixa usa para baixo igual à direita e para cima igual à esquerda. Use o estilo TBS \_ DOWNISLEFT para inverter o padrão, rebaixando para a esquerda e para cima igual à direita. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TBS \_ NOTIFYBEFOREMOVE**</dt> </dl> | [Versão 6.00](common-control-versions.md) e **Windows Vista.** A barra de faixa deve notificar o pai antes de reposicionar o controle deslizante devido à ação do usuário (habilita o ajuste). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TBS \_ TRANSPARENTBKGND**</dt> </dl> | [Versão 6.00](common-control-versions.md) e **Windows Vista.** A tela de fundo é pintada pelo pai por meio da \_ mensagem WM PRINTCLIENT. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





