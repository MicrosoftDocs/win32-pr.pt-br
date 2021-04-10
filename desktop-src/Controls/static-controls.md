---
title: Controle estático
description: Esta seção contém informações sobre os elementos de programação usados com controles estáticos. Um controle estático é um controle que permite que um aplicativo forneça ao usuário texto informativo e elementos gráficos que normalmente não exigem resposta.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008450"
---
# <a name="static-control"></a>Controle estático

Esta seção contém informações sobre os elementos de programação usados com controles estáticos. Um *controle estático* é um controle que permite que um aplicativo forneça ao usuário texto informativo e elementos gráficos que normalmente não exigem resposta.

### <a name="overviews"></a>Visões gerais



| Tópico                                              | Sumário                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [Sobre controles estáticos](about-static-controls.md) | Este tópico discute como os controles estáticos são usados.<br/>         |
| [Estilos de controle estático](static-control-styles.md) |                                                                       |
| [Usando controles estáticos](using-static-controls.md) | Este tópico fornece um exemplo que usa um controle estático.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                 | Sumário                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**STM \_ GETicon**](stm-geticon.md)   | Um aplicativo envia a mensagem de [**\_ GetIcon STM**](stm-geticon.md) para recuperar um identificador para o ícone associado a um controle estático que tem o \_ estilo de ícone SS. <br/> |
| [**STM \_ GETimage**](stm-getimage.md) | Um aplicativo envia uma mensagem [**STM \_ GetImage**](stm-getimage.md) para recuperar um identificador para a imagem (ícone ou bitmap) associado a um controle estático. <br/>          |
| [**\_ícone STM**](stm-seticon.md)   | Um aplicativo envia a mensagem de [**\_ autoícone STM**](stm-seticon.md) para associar um ícone a um controle de ícone. <br/>                                                     |
| [**\_imagem STM**](stm-setimage.md) | Um aplicativo envia uma mensagem [**STM \_ SetImage**](stm-setimage.md) para associar uma nova imagem a um controle estático.<br/>                                                |



 

### <a name="notifications"></a>Notificações



| Tópico                                           | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ clicou](stn-clicked.md)                 | O código de notificação [ \_ clicado em STN](stn-clicked.md) é enviado quando o usuário clica em um controle estático que tem o estilo de [**\_ notificação SS**](static-control-styles.md) . A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | O código de notificação [STN \_ DBLCLK](stn-dblclk.md) é enviado quando o usuário clica duas vezes em um controle estático com o estilo de **\_ notificação SS** . A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                                          |
| [STN \_ desabilitar](stn-disable.md)                 | O código de notificação de [ \_ desabilitação de STN](stn-disable.md) é enviado quando um controle estático é desabilitado. O controle estático deve ter o **estilo \_ de notificação SS** para receber esse código de notificação. A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                            |
| [STN \_ habilitar](stn-enable.md)                   | O código de notificação [STN \_ Enable](stn-enable.md) é enviado quando um controle estático é habilitado. O controle estático deve ter o **estilo \_ de notificação SS** para receber esse código de notificação. A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                               |
| [**CTLCOLORSTATIC do WM \_**](wm-ctlcolorstatic.md) | Um controle estático, ou um controle de edição que é somente leitura ou desabilitado, envia a mensagem do [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) para sua janela pai quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de dispositivo especificado para definir o texto e as cores de plano de fundo do controle estático. <br/> Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |



 

 

