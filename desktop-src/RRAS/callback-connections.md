---
title: Conexões de retorno de chamada
description: O RAS dá suporte a conexões nas quais o servidor remoto desliga e, em seguida, chama o cliente para estabelecer a conexão.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641730"
---
# <a name="callback-connections"></a>Conexões de retorno de chamada

O RAS dá suporte a conexões nas quais o servidor remoto desliga e, em seguida, chama o cliente para estabelecer a conexão.

Para cada usuário que pode se conectar a um servidor RAS, o servidor armazena um atributo de retorno de chamada que controla como a conexão é feita. O atributo padrão não é um retorno de chamada, o que significa que o usuário pode se conectar ao servidor RAS sem um retorno de chamada. Como alternativa, o administrador do servidor RAS pode atribuir a um usuário o atributo de retorno de chamada predefinido ou definido pelo chamador.

Para que um usuário tenha a restrição predefinida atribuída, o administrador especifica um número de telefone que o servidor RAS deve chamar de volta para estabelecer uma conexão. O usuário não pode especificar um número diferente e a conexão não pode ser feita sem um retorno de chamada.

Uma operação de retorno de chamada predefinida é manipulada automaticamente pelo Gerenciador de conexões de acesso remoto e pelo servidor remoto. O aplicativo cliente RAS não precisa fazer nada além de fornecer comentários ao usuário quando o manipulador de notificação é chamado durante os vários Estados da operação de retorno de chamada.

Um usuário que atribuiu o privilégio definido pelo chamador pode optar por conectar-se com ou sem um retorno de chamada. A chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) usa o membro **SzCallbackNumber** da estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para indicar a escolha.

O membro **szCallBackNumber** pode simplesmente especificar o número de retorno de chamada; ou, para estabelecer a conexão sem um retorno de chamada, **szCallBackNumber** pode apontar para uma cadeia de caracteres vazia, "". Em qualquer um desses casos, o Gerenciador de conexões de acesso remoto manipula a operação de conexão automaticamente. Assim como acontece com uma operação de retorno de chamada predefinida, o cliente RAS não precisa executar nenhuma ação além de fornecer comentários ao usuário.

Se a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) permitir [Estados em pausa](paused-states.md), **szCallBackNumber** poderá apontar para uma cadeia de caracteres de asterisco, " \* ", para indicar que a operação de conexão deve entrar em um estado de pausa para permitir que o usuário digite o número de retorno de chamada. Nesse caso, a operação de conexão para um conjunto pelo usuário do chamador entra em um estado de pausa depois que o servidor remoto tiver autenticado o usuário. Durante o estado de pausa, o cliente RAS Obtém a entrada do número de retorno de chamada do usuário. Em seguida, o cliente retoma a operação de conexão fazendo uma segunda chamada **RasDial** , na qual **szCallBackNumber** especifica o número fornecido pelo usuário.

> [!Note]  
> Se os Estados em pausa não estiverem habilitados, haverá um significado diferente quando **szCallBackNumber** apontar para uma cadeia de caracteres de asterisco, " \* ". Nesse caso, o asterisco indica que o número de retorno de chamada é armazenado no arquivo de catálogo telefônico especificado pela chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

 

No caso de um retorno de chamada, a chamada para [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) não retorna até que o servidor tenha chamado de volta o cliente.

 

 