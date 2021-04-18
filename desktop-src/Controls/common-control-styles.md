---
title: Estilos comuns de controle (CommCtrl. h)
description: Esta seção lista os estilos de controle comuns. Exceto quando observado, esses estilos se aplicam a controles Rebar, controles de barra de ferramentas e janelas de status.
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749537"
---
# <a name="common-control-styles"></a>Estilos comuns de controle

Esta seção lista os estilos de controle comuns. Exceto quando observado, esses estilos se aplicam a controles Rebar, controles de barra de ferramentas e janelas de status.



| Constante                                                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS \_ ajustável**</dt> </dl>          | Habilita os recursos de personalização internos de uma barra de ferramentas, o que permite ao usuário arrastar um botão para uma nova posição ou remover um botão arrastando-o para fora da barra de ferramentas. Além disso, o usuário pode clicar duas vezes na barra de ferramentas para exibir a caixa de diálogo **Personalizar barra de ferramentas** , que permite ao usuário adicionar, excluir e reorganizar botões da barra de ferramentas.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**\_parte inferior da CCS**</dt> </dl>                      | Faz com que o controle se posicione na parte inferior da área do cliente da janela pai e define a largura como a mesma que a largura da janela pai. As janelas de status têm esse estilo por padrão.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ esquerda**</dt> </dl>                            | [Versão 4,70](common-controls-intro.md). Faz com que o controle seja exibido verticalmente no lado esquerdo da janela pai.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ NOdivider**</dt> </dl>             | Impede que um realce de dois pixels seja desenhado na parte superior do controle. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Versão 4,70](common-controls-intro.md). Faz com que o controle redimensione e se mova verticalmente, mas não horizontalmente, em resposta a uma mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) . Se CCS \_ noResize for usado, esse estilo não se aplicará.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOmover**</dt> </dl>                   | Faz com que o controle redimensione e se mova horizontalmente, mas não verticalmente, em resposta a uma mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) . Se CCS \_ noResize for usado, esse estilo não se aplicará. As janelas de cabeçalho têm esse estilo por padrão.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Impede que o controle se mova automaticamente para a parte superior ou inferior da janela pai. Em vez disso, o controle mantém sua posição dentro da janela pai apesar das alterações no tamanho do pai. Se CCS \_ Top ou ccs \_ Bottom também for usado, a altura será ajustada para o padrão, mas a posição e a largura permanecerão inalteradas. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ redimensionar**</dt> </dl>                | Impede que o controle use a largura e a altura padrão ao definir seu tamanho inicial ou um novo tamanho. Em vez disso, o controle usa a largura e a altura especificadas na solicitação de criação ou dimensionamento. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ à direita**</dt> </dl>                         | [Versão 4,70](common-controls-intro.md). Faz com que o controle seja exibido verticalmente no lado direito da janela pai.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ superior**</dt> </dl>                               | Faz com que o controle se posicione na parte superior da área do cliente da janela pai e define a largura como a mesma que a largura da janela pai. As barras de ferramentas têm esse estilo por padrão. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ Vert**</dt> </dl>                            | [Versão 4,70](common-controls-intro.md). Faz com que o controle seja exibido verticalmente.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentários

Os tópicos a seguir descrevem os estilos de controle adicionais:

-   [**Estilos de controle de animação**](animation-control-styles.md)
-   [**Estilos de botão**](button-styles.md)
-   [**Estilos de caixa de combinação**](combo-box-styles.md)
-   [**Estilos estendidos do controle ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Estilos de controle do seletor de data e hora**](date-and-time-picker-control-styles.md)
-   [**Editar estilos de controle**](edit-control-styles.md)
-   [**Estilos de controle de cabeçalho**](header-control-styles.md)
-   [**Estilos de caixa de listagem**](list-box-styles.md)
-   [**Listar estilos de janela de exibição**](list-view-window-styles.md)
-   [**Estilos de controle de calendário mensal**](month-calendar-control-styles.md)
-   [**Estilos de controle de pager**](pager-control-styles.md)
-   [**Estilos de controle da barra de progresso**](progress-bar-control-styles.md)
-   [**Estilos de controle rebar**](rebar-control-styles.md)
-   [**Estilos de controle de edição avançados**](rich-edit-control-styles.md)
-   [**Estilos de controle da barra de rolagem**](scroll-bar-control-styles.md)
-   [Estilos de controle estático](static-control-styles.md)
-   [**Estilos da barra de status**](status-bar-styles.md)
-   [**Estilos de controle SysLink**](syslink-control-styles.md)
-   [**Estilos de controle de guia**](tab-control-styles.md)
-   [**Controle da barra de ferramentas e estilos de botão**](toolbar-control-and-button-styles.md)
-   [**Estilos de dica de ferramenta**](tooltip-styles.md)
-   [**Estilos de controle TrackBar**](trackbar-control-styles.md)
-   [**Estilos de janela de controle de exibição de árvore**](tree-view-control-window-styles.md)
-   [**Estilos de controle de cima para baixo**](up-down-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

