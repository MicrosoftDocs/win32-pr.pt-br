---
title: Barra de Andamento
description: Esta seção contém informações sobre os elementos de programação usados com controles de barra de progresso.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c9cd66326336cd3733f881f3f19d82fedc3bf8d8420f83035bf20dc914c7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670647"
---
# <a name="progress-bar"></a>Barra de Andamento

Esta seção contém informações sobre os elementos de programação usados com controles de barra de progresso.

### <a name="overviews"></a>Visões gerais



| Tópico                                            | Sumário                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Controle da barra de progresso](progress-bar-control.md) | Uma barra de progresso é uma janela que um aplicativo pode usar para indicar o progresso de uma operação demorada.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                       | Sumário                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELTAPOS do PBM \_**](pbm-deltapos.md)       | Avança a posição atual de uma barra de progresso por um incremento especificado e redesenha a barra para refletir a nova posição. <br/>                                                                                                                                 |
| [**GETBARCOLOR do PBM \_**](pbm-getbarcolor.md) | Obtém a cor da barra de progresso.<br/>                                                                                                                                                                                                                        |
| [**GETBKCOLOR do PBM \_**](pbm-getbkcolor.md)   | Obtém a cor do plano de fundo da barra de progresso.<br/>                                                                                                                                                                                                             |
| [**GETPOS do PBM \_**](pbm-getpos.md)           | Recupera a posição atual da barra de progresso. <br/>                                                                                                                                                                                                       |
| [**GetRange do PBM \_**](pbm-getrange.md)       | Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso. <br/>                                                                                                                                                              |
| [**o PBM \_ GETstate**](pbm-getstate.md)       | Obtém o estado da barra de progresso.<br/>                                                                                                                                                                                                                        |
| [**getstep do PBM \_**](pbm-getstep.md)         | Recupera o incremento de etapa para uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) .<br/>                                               |
| [**SETBARCOLOR do PBM \_**](pbm-setbarcolor.md) | Define a cor da barra de indicadores de progresso no controle da barra de progresso. <br/>                                                                                                                                                                                 |
| [**SETBKCOLOR do PBM \_**](pbm-setbkcolor.md)   | Define a cor do plano de fundo na barra de progresso. <br/>                                                                                                                                                                                                            |
| [**setmarquee do PBM \_**](pbm-setmarquee.md)   | Define a barra de progresso para o modo de letreiro. Isso faz com que a barra de progresso se mova como um letreiro.<br/>                                                                                                                                                                |
| [**SETPOS do PBM \_**](pbm-setpos.md)           | Define a posição atual de uma barra de progresso e redesenha a barra para refletir a nova posição. <br/>                                                                                                                                                             |
| [**SETRANGE do PBM \_**](pbm-setrange.md)       | Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.<br/>                                                                                                                                                       |
| [**SETRANGE32 do PBM \_**](pbm-setrange32.md)   | Define o intervalo de um controle de barra de progresso para um valor de 32 bits. <br/>                                                                                                                                                                                               |
| [**Estado do PBM \_**](pbm-setstate.md)       | Define o estado da barra de progresso.<br/>                                                                                                                                                                                                                        |
| [**SetStep do PBM \_**](pbm-setstep.md)         | Especifica o incremento de etapa para uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) . Por padrão, o incremento Step é definido como 10. <br/> |
| [**STEPIT do PBM \_**](pbm-stepit.md)           | Avança a posição atual de uma barra de progresso pela etapa incremento e redesenha a barra para refletir a nova posição. Um aplicativo define o incremento de etapa enviando a mensagem do [**PBM \_ SetStep**](pbm-setstep.md) . <br/>                                |



 

### <a name="structures"></a>Estruturas



| Tópico                      | Sumário                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contém informações sobre os limites alto e baixo de um controle de barra de progresso. Essa estrutura é usada com a mensagem do [**PBM \_ GetRange**](pbm-getrange.md) . <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                                          | Sumário                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de controle da barra de progresso](progress-bar-control-styles.md) | Os seguintes estilos de controle têm suporte dos controles de **barra de progresso** :<br/> |



 

 

 





