---
description: Lista e explica as responsabilidades do LTD.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades do LTD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e4d2189d1d4258566a5e4baab357dc446a8f1c4ea409d7af328a85bf84c217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919034"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilidades do LTD

> [!Note]  
> As DLLs DE VALOR são ignoradas no Windows Vista.

 

Uma DLL [*DO LTD*](../secgloss/g-gly.md) tem as seguintes responsabilidades:

-   Monitoramento de SAS

    O LTD é responsável por reconhecer uma SAS [*(sequência*](../secgloss/s-gly.md) de atenção segura), monitorar eventos de SAS e notificar o Winlogon quando ocorreu uma SAS. Observe que pode haver mais de uma SAS definida e o conjunto de SASs definido pode mudar ao longo do tempo. Por exemplo, pode haver um conjunto de SASs quando [*o Winlogon*](../secgloss/w-gly.md) está no estado de logout e outro definido quando ele está no estado conectado.

    O Winlogon fornece serviços para ajudar oRL a usar a CTRL+ALT+DEL SAS.

-   Processamento de SAS

    Um motivo para tornar o LTD substituível é fornecer mecanismos alternativos de identificação e autenticação. Para fazer isso, o LTD deve apresentar todas as interfaces do usuário resultantes do reconhecimento de uma SAS. Quando nenhum usuário está conectado, o LTD é responsável por apresentar opções de identificação e autenticação, bem como outras opções permitidas que não são autenticadas. Quando um usuário está conectado, o LTD é responsável por apresentar as opções relevantes para o usuário, bem como tomar as ações que são consideradas apropriadas. Por exemplo, em um sistema que inclui um [*cartão*](../secgloss/s-gly.md)inteligente , pode ser apropriado bloquear automaticamente a estação de trabalho se o usuário remover o cartão inteligente.

-   Ativação do shell

    Quando um usuário faz o login, oLP é responsável por criar um ou mais processos iniciais para esse usuário. (Nesta documentação, supõe-se que esses processos iniciais apresentem uma interface para o usuário. No entanto, os processos podem ser, na verdade, qualquer processo e não precisam necessariamente interagir com o usuário.) Esses processos são chamados de shell *de usuário ou* apenas o *shell*. Como parte da ativação do shell, o LTD deve atribuir o token do usuário recém-conectado aos processos. O Winlogon fornece um serviço para auxiliar oLP na atribuição do token.

 

 
