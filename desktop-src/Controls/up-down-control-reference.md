---
title: Controle de Up-Down
description: Esta seção contém informações sobre os elementos de programação usados com controles de cima para baixo.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005355"
---
# <a name="up-down-control"></a>Controle de Up-Down

Esta seção contém informações sobre os elementos de programação usados com controles de cima para baixo.

### <a name="overviews"></a>Visões gerais



| Tópico                                    | Sumário                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de cima para baixo](up-down-controls.md) | Um controle de cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle complementar (chamado de janela Buddy).<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                              | Sumário                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Cria um controle de cima para baixo. Observação: essa função está obsoleta. É uma função de 16 bits e não pode manipular valores de 32 bits para intervalo e posição.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETACCEL UDM**](udm-getaccel.md)                 | Recupera informações de aceleração para um controle de cima para baixo. <br/>                                                                                                                                                                 |
| [**UDM \_ GETbase**](udm-getbase.md)                   | Recupera a base da Radix atual (ou seja, a base 10 ou 16) para um controle acima-abaixo. <br/>                                                                                                                                   |
| [**UDM \_ GETbuddy**](udm-getbuddy.md)                 | Recupera o identificador para a janela atual do Buddy. <br/>                                                                                                                                                                          |
| [**\_GETPOS UDM**](udm-getpos.md)                     | Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits. <br/>                                                                                                                                                |
| [**\_GETPOS32 UDM**](udm-getpos32.md)                 | Retorna a posição de 32 bits de um controle acima-abaixo.<br/>                                                                                                                                                                          |
| [**GetRange do UDM \_**](udm-getrange.md)                 | Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo. <br/>                                                                                                                                                |
| [**\_GETRANGE32 UDM**](udm-getrange32.md)             | Recupera o intervalo de 32 bits de um controle acima-abaixo. <br/>                                                                                                                                                                          |
| [**\_GETUNICODEFORMAT UDM**](udm-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle. <br/>                                                                                                                                                               |
| [**\_SETACCEL UDM**](udm-setaccel.md)                 | Define a aceleração para um controle de cima para baixo. <br/>                                                                                                                                                                              |
| [**UDM \_ SETbase**](udm-setbase.md)                   | Define a base do Radix para um controle de cima para baixo. O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais. Os números hexadecimais são sempre não assinados e números decimais são assinados. <br/> |
| [**UDM \_ SETbuddy**](udm-setbuddy.md)                 | Define a janela Buddy para um controle de cima para baixo. <br/>                                                                                                                                                                              |
| [**\_SETPOS UDM**](udm-setpos.md)                     | Define a posição atual para um controle de cima para baixo com precisão de 16 bits. <br/>                                                                                                                                                    |
| [**\_SETPOS32 UDM**](udm-setpos32.md)                 | Define a posição de um controle de cima para baixo com precisão de 32 bits.<br/>                                                                                                                                                              |
| [**SETRANGE de UDM \_**](udm-setrange.md)                 | Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.<br/>                                                                                                                                                      |
| [**\_SETRANGE32 UDM**](udm-setrange32.md)             | Define o intervalo de 32 bits de um controle acima-abaixo. <br/>                                                                                                                                                                               |
| [**\_SETUNICODEFORMAT UDM**](udm-setunicodeformat.md) | Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/>                                   |



 

### <a name="notifications"></a>Notificações



| Tópico                                                            | Sumário                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (up-down)](nm-releasedcapture-up-down-.md) | Notifica uma janela pai do controle up que o controle está liberando a captura do mouse. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada. Isso acontece quando o usuário solicita uma alteração no valor pressionando a seta para cima ou para baixo do controle. A mensagem [UDN \_ DELTAPOS](udn-deltapos.md) é enviada na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estruturas



| Tópico                        | Sumário                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contém informações específicas para as mensagens de notificação de controle de cima para baixo. É idêntico a e substitui a estrutura **do \_ nm** . <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contém informações de aceleração para um controle de cima para baixo. <br/>                                                                             |



 

### <a name="constants"></a>Constantes



| Tópico                                                | Sumário                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Estilos de controle de cima para baixo](up-down-control-styles.md) | Esta seção lista os estilos usados ao criar controles de cima para baixo.<br/> |



 

 

 





