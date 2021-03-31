---
title: Manipuladores de notificação
description: Uma chamada de RasDial assíncrona deve especificar um manipulador de notificação.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe735a17de4386bc48648cd20decd218ab102d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916586"
---
# <a name="notification-handlers"></a>Manipuladores de notificação

Uma chamada de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) assíncrona deve especificar um manipulador de notificação. Durante uma operação de conexão assíncrona, o Gerenciador de conexões de acesso remoto usa o manipulador de notificação para informar o cliente RAS sempre que o [estado da conexão](connection-states.md) é alterado ou ocorre um erro.

As ações executadas por um manipulador de notificação podem ser divididas nas seguintes categorias:

-   [Manipulação de erros](handling-ras-errors.md).
-   Fornecer comentários para o usuário conforme a operação de conexão prossegue pelos vários Estados de conexão. Consulte [notificações informativas](informational-notifications.md).
-   Tratamento de [Estados pausados](paused-states.md).
-   Sinalizar o aplicativo cliente RAS quando a operação de conexão for concluída. Consulte as [notificações de conclusão](completion-notifications.md).

Há três tipos de manipuladores de notificação, cada um dos quais recebe as mesmas informações básicas: o estado de conexão atual e um código de erro que é diferente de zero somente se ocorreu um erro.



| Valor                                | Definição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Um protótipo de função de retorno de chamada que recebe apenas o estado da conexão atual e as informações do código de erro.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Um protótipo de função de retorno de chamada que recebe o identificador de conexão **HRASCONN** e informações de erro estendidas, além das informações básicas. O parâmetro de identificador de conexão torna o [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) útil para aplicativos cliente que dão suporte a várias operações de conexão simultâneas. Isso permite que o cliente especifique a mesma função de retorno de chamada para todas as operações e habilita a função de retorno de chamada para determinar qual conexão está alterando os Estados. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Uma função de retorno de chamada semelhante a [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1). No entanto, o [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) é aprimorado para dar suporte a conexões de Multilink.                                                                                                                                                                                                                                                                                                                             |
| Identificador de janela                        | Um identificador de janela para o qual o RAS envia mensagens do [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) que contêm o estado da conexão atual e as informações do código de erro. Use esse método se o código-fonte precisar ser compatível com o Windows de 16 bits, porque o Windows de 16 bits não oferece suporte a nenhuma das funções de retorno de chamada.                                                                                                                                                                            |



 

O Gerenciador de conexões de acesso remoto suspende a operação de conexão até que o manipulador de notificação seja retornado. Por esse motivo, o manipulador deve retornar assim que possível, a menos que tenha ocorrido um erro.

A função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) não deve ser chamada de dentro de um manipulador de notificação. As outras funções de acesso remoto ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa), [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa), [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)e [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) podem ser chamadas de dentro de um manipulador.

 

 




