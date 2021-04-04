---
description: Lista e explica as responsabilidades da GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades da GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010980"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilidades da GINA

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Uma dll [*Gina*](../secgloss/g-gly.md) tem as seguintes responsabilidades:

-   Monitoramento de SAS

    A GINA é responsável por reconhecer uma SAS ( [*sequência de atenção segura*](../secgloss/s-gly.md) ), o monitoramento de eventos de SAS e a notificação do Winlogon quando ocorre uma SAS. Observe que pode haver mais de uma SAS definida, e o conjunto de SASs definido pode mudar ao longo do tempo. Por exemplo, pode haver um conjunto de SASs quando o [*Winlogon*](../secgloss/w-gly.md) está no estado conectado e outro definido quando está no estado conectado.

    O Winlogon fornece serviços para ajudar a GINA no uso da SAS CTRL + ALT + DEL.

-   Processamento de SAS

    Um motivo para fazer a GINAção substituível é fornecer mecanismos alternativos de identificação e autenticação. Para fazer isso, a GINA deve apresentar todas as interfaces de usuário resultantes do reconhecimento de uma SAS. Quando nenhum usuário está conectado, o GINA é responsável por apresentar as opções de identificação e autenticação, bem como outras opções permitidas que não são autenticadas. Quando um usuário está conectado, a GINA é responsável por apresentar as opções relevantes para o usuário, bem como pegar quaisquer ações que sejam consideradas apropriadas. Por exemplo, em um sistema que inclui um [*cartão inteligente*](../secgloss/s-gly.md), pode ser apropriado bloquear a estação de trabalho automaticamente se o usuário remover o cartão inteligente.

-   Ativação do Shell

    Quando um usuário faz logon, a GINA é responsável por criar um ou mais processos iniciais para esse usuário. (Nesta documentação, supõe-se que esses processos iniciais apresentem uma interface para o usuário. No entanto, os processos podem realmente ser qualquer processo e não precisam necessariamente interagir com o usuário.) Esses processos são chamados de shell do *usuário* ou apenas do *shell*. Como parte da ativação do Shell, a GINA deve atribuir o token do usuário conectado recentemente aos processos. O Winlogon fornece um serviço para ajudar a GINA na atribuição do token.

 

 
