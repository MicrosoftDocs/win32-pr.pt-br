---
description: Quando o Winlogon é inicializado, ele registra a SAS (sequência de atenção segura) CTRL + ALT + DEL com o sistema e, em seguida, cria três áreas de trabalho na estação de janela do WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inicializando Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171257"
---
# <a name="initializing-winlogon"></a>Inicializando Winlogon

Quando o [Winlogon](winlogon.md) é inicializado, ele registra a SAS ( [*sequência de atenção segura*](../secgloss/s-gly.md) ) Ctrl + Alt + Del com o sistema e, em seguida, cria três áreas de trabalho na estação de janela do WinSta0.

O registro de CTRL + ALT + DEL faz com que essa inicialização seja o primeiro processo, garantindo que nenhum outro aplicativo tenha conectado essa sequência de chaves.

WinSta0 é o nome do objeto de estação da janela que representa a tela física, o teclado e o mouse. O Winlogon cria as seguintes áreas de trabalho no objeto WinSta0.



| Área de trabalho              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Área de trabalho do Winlogon     | Essa é a área de trabalho que o Winlogon e a [*Gina*](../secgloss/g-gly.md) usam para identificação e autenticação interativas e outras caixas de diálogo seguras. O Winlogon alterna automaticamente para esta área de trabalho quando recebe a notificação de eventos de SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Área de trabalho do aplicativo  | Cada vez que um usuário faz logon com êxito, um desktop de aplicativo é criado para essa [*sessão de logon*](../secgloss/l-gly.md). A área de trabalho do aplicativo também é conhecida como a área de trabalho padrão ou do usuário. Essa área de trabalho é o local em que toda a atividade do usuário ocorre. O aplicativo desktop está protegido; somente o sistema e a sessão de logon interativo têm acesso a ele. Observe que apenas uma instância específica do usuário conectado tem acesso à área de trabalho. Se o usuário interativo ativar um processo usando o controlador de serviço, esse aplicativo de serviço não terá acesso ao aplicativo desktop. |
| Área de trabalho de proteção de tela | Esta é a área de trabalho atual quando uma proteção de tela está em execução. Se um usuário estiver conectado, tanto o sistema quanto a sessão de logon interativo terão acesso à área de trabalho. Caso contrário, somente o sistema terá acesso à área de trabalho.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Como o proprietário dessas áreas de trabalho, o Winlogon pode mudar a área de trabalho atual, ou visível, para qualquer um dos três desktops e permitir que o GINA acesse essa funcionalidade. Em geral, os desenvolvedores da GINA não alterarão a área de trabalho atual, pois o Winlogon define a área de trabalho apropriadamente antes de se comunicar com a GINA. A descrição de cada função GINA indica qual área de trabalho é a atual para essa chamada.



| Para obter informações sobre                                    | Consulte                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Os diferentes Estados em que o Winlogon pode ser executado           | [Estados do Winlogon](winlogon-states.md)                                                                   |
| Operações de tempo limite                                      | [Caixa de diálogo com suporte Tempo de Serviço operações de saída](supported-dialog-box-service-time-out-operations.md) |
| Enviando mensagens para GINA enquanto uma caixa de diálogo é exibida | [Enviando mensagens para a GINA](sending-messages-to-the-gina.md)                                         |
| Funções de suporte                                        | [Funções de suporte do Winlogon](authentication-functions.md)                    |



 

 

 
