---
title: Controle de endereço IP
description: Esta seção contém informações sobre os elementos de programação usados com controles de endereço IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453553"
---
# <a name="ip-address-control"></a>Controle de endereço IP

Esta seção contém informações sobre os elementos de programação usados com controles de endereço IP.

### <a name="overviews"></a>Visões gerais



| Tópico                                          | Sumário                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Controles de endereço IP](ip-address-controls.md) | Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido.<br/> |



 

### <a name="macros"></a>Macros



| Tópico                                         | Sumário                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PRIMEIRO \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | Extrai o valor do campo 0 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**QUARTO \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | Extrai o valor do campo 3 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | Empacota quatro valores de byte em um único LPARAM adequado para uso com a mensagem [**IPM \_ SetAddress**](ipm-setaddress.md) . <br/>  |
| [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | Compacta dois valores de byte em um único LPARAM adequado para uso com a mensagem [**IPM \_ SETRANGE**](ipm-setrange.md) . <br/>       |
| [**SEGUNDO \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | Extrai o valor do campo 1 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**TERCEIRO \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | Extrai o valor do campo 2 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                         | Sumário                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CLEARADDRESS IPM**](ipm-clearaddress.md) | Limpa o conteúdo do controle de endereço IP. <br/>                                                                            |
| [**\ \_ endereço IPM**](ipm-getaddress.md)     | Obtém os valores de endereço para todos os quatro campos no controle de endereço IP. <br/>                                                    |
| [**IPM \_ ISblank**](ipm-isblank.md)           | Determina se todos os campos no controle de endereço IP estão em branco. <br/>                                                             |
| [**de \_ IPM**](ipm-setaddress.md)     | Define os valores de endereço para todos os quatro campos no controle de endereço IP. <br/>                                                    |
| [**IPM \_ SETFOCUS**](ipm-setfocus.md)         | Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado. <br/> |
| [**IPM \_ SETRANGE**](ipm-setrange.md)         | Define o intervalo válido para o campo especificado no controle de endereço IP. <br/>                                                   |



 

### <a name="notifications"></a>Notificações



| Tópico                                     | Sumário                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_campo IPN](ipn-fieldchanged.md) | Enviado quando o usuário altera um campo no controle ou move de um campo para outro. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estruturas



| Tópico                              | Sumário                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | Contém informações para o código de notificação [ \_ FieldChanged IPN](ipn-fieldchanged.md) . <br/> |



 

 

 





