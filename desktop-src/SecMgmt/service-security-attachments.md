---
description: O conjunto de ferramentas de configuração de segurança da Microsoft é um conjunto do MMC (console de gerenciamento Microsoft) que simplifica a configuração e a análise da segurança do sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Anexos de segurança de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296267"
---
# <a name="service-security-attachments"></a>Anexos de segurança de serviço

O conjunto de ferramentas de configuração de segurança da Microsoft é um conjunto do MMC (console de gerenciamento Microsoft) que simplifica a configuração e a análise da segurança do sistema. Alguns serviços, no entanto, têm necessidades de configuração especializadas que vão além das configurações de segurança fornecidas pelo conjunto de ferramentas padrão. Para lidar com essas necessidades, você pode estender a funcionalidade do conjunto de ferramentas escrevendo um anexo que manipula as tarefas de segurança específicas do serviço.

Por exemplo, o spooler é um serviço do Windows NT que define objetos privados, que precisam ser protegidos, por exemplo, impressoras. Essa funcionalidade não é tratada pelo conjunto de ferramentas padrão e, portanto, requer um anexo para lidar com a configuração e a análise de objetos de impressora. A configuração de parâmetros de segurança geral, como a política de invocação de serviço, ainda é manipulada pelo conjunto de ferramentas de configuração de segurança.

Os anexos do serviço de segurança estendem a funcionalidade da ferramenta configuração de segurança definida para dar suporte a configurações específicas do serviço.

Um anexo tem dois componentes:

-   Uma extensão de snap-in do MMC que implementa a interface do usuário do anexo.
-   Um mecanismo de anexo que processa tarefas de análise e configuração de segurança específicas de serviço.

A extensão do snap-in de anexos é hospedada pelos snap-ins de configuração de segurança. Esses são snap-ins do MMC que fornecem ao usuário interfaces para configurar e analisar as configurações de segurança gerais de um serviço. As configurações específicas do serviço são configuradas usando a extensão de snap-in de anexo.

Quando o usuário altera uma definição de configuração, os snap-ins de configuração de segurança armazenam as novas informações e, em seguida, passam a solicitação para o mecanismo de configuração de segurança. O mecanismo processa a solicitação e define o serviço para a nova configuração. Se a solicitação afetar uma configuração de segurança padrão, ela será manipulada pelo mecanismo. Se a solicitação for específica do serviço, o mecanismo chamará o mecanismo de anexo apropriado para manipular a solicitação.

A ilustração a seguir mostra como o mecanismo de anexo e a extensão do snap-in funcionam dentro da estrutura do conjunto de ferramentas de configuração de segurança.

![mecanismo de anexo e snap-ins](images/model1a.png)

Para obter mais informações sobre como usar o conjunto de ferramentas de configuração de segurança da Microsoft, pesquise configuração de segurança usando seu mecanismo de pesquisa preferido.

 

 



