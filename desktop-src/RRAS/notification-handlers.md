---
title: Manipuladores de notificação
description: Uma chamada RasDial assíncrona deve especificar um manipulador de notificação.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7210072e0542eeb63e3de6116d61995ef2363ca7b43e7a9e2c309165c0e862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074026"
---
# <a name="notification-handlers"></a>Manipuladores de notificação

Uma chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) assíncrona deve especificar um manipulador de notificação. Durante uma operação de conexão assíncrona, o Gerenciador de Conexões de Acesso Remoto usa [](connection-states.md) o manipulador de notificação para informar o cliente RAS sempre que o estado da conexão for alterando ou ocorrendo um erro.

As ações executadas por um manipulador de notificação podem ser divididas nas seguintes categorias:

-   [Manipulação de erros](handling-ras-errors.md).
-   Fornecer comentários para o usuário à medida que a operação de conexão passa pelos vários estados de conexão. Consulte [Notificações informativas.](informational-notifications.md)
-   Tratamento [de estados em pausa.](paused-states.md)
-   Sinalizando o aplicativo cliente RAS quando a operação de conexão for concluída. Consulte [Notificações de conclusão.](completion-notifications.md)

Há três tipos de manipuladores de notificação, cada um deles recebe as mesmas informações básicas: o estado de conexão atual e um código de erro que não é zero somente se ocorreu um erro.



| Valor                                | Definição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Um protótipo de função de retorno de chamada que recebe apenas o estado de conexão atual e as informações de código de erro.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Um protótipo de função de retorno de chamada que recebe o alçamento de **conexão HRASCONN** e informações de erro estendidas, além das informações básicas. O parâmetro de alça de conexão [**torna RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) útil para aplicativos cliente que suportam várias operações de conexão simultâneas. Isso permite que o cliente especifique a mesma função de retorno de chamada para todas as operações e permite que a função de retorno de chamada determine qual conexão está alterando estados. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Uma função de retorno de chamada semelhante [**a RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) No entanto, [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) é aprimorado para dar suporte a conexões multilink.                                                                                                                                                                                                                                                                                                                             |
| Alça de janela                        | Um alça de janela para o qual o RAS envia [**mensagens WM \_ RASDIALEVENT**](wm-rasdialevent.md) contendo o estado de conexão atual e informações de código de erro. Use esse método se o código-fonte deve ser compatível com Windows de 16 bits, porque o Windows de 16 bits não dá suporte a nenhuma das funções de retorno de chamada.                                                                                                                                                                            |



 

O sistema de Gerenciador de Conexões remoto suspende a operação de conexão até que o manipulador de notificação retorne. Por esse motivo, o manipulador deve retornar assim que possível, a menos que tenha ocorrido um erro.

A [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) não deve ser chamada de dentro de um manipulador de notificação. As outras funções de acesso remoto ( [**RasGetConnectStatus,**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections,**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)e [**RasGetUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) podem ser chamadas de dentro de um manipulador.

 

 




