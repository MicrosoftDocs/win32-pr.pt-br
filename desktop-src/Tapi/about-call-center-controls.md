---
description: A TAPI 3 define cinco objetos ad principais que o Agent trata da fila do grupo ad do agente e da sessão do agente. Ele também estende o objeto TAPI com uma interface adicional ITTAPICallCenter.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: Sobre controles do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091619"
---
# <a name="about-call-center-controls"></a>Sobre controles do Call Center

A TAPI 3 define cinco objetos ad principais: o manipulador de agente, a fila, o grupo ad, o agente e a sessão do agente. Ele também estende o objeto TAPI com uma interface adicional — [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Objeto do agente

O objeto Agent representa um agente capaz de lidar com chamadas. Normalmente, isso é uma pessoa, mas pode ser um IVR ou alguma outra combinação de software e hardware. Os agentes são fundamentais para um Call Center; Eles são responsáveis por receber e processar chamadas de entrada e, às vezes, fazer chamadas de saída para clientes ou clientes potenciais.

Na TAPI, o objeto do agente se relaciona diretamente a uma conta de usuário, para fornecer compatibilidade com os sistemas de alternância herdados existentes. Além disso, para fornecer compatibilidade com os sistemas de comutação herdados existentes, o agente também pode estar relacionado a uma ID de agente de comutador.

O objeto Agent expõe a interface [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) . Essa interface implementa métodos que podem criar uma sessão de agente e recuperar estatísticas, como o total de chamadas tratadas. Os aplicativos podem usar o objeto Agent para manipular o estado do agente e determinar as estatísticas globais do agente.

## <a name="agent-handler-object"></a>Objeto manipulador de agente

Um manipulador de agente representa software ou hardware capaz de passar chamadas para um grupo de agentes. Normalmente, esse é um comutador proprietário que conecta linhas externas a telefones em estações de agente. A maioria dos sistemas ad tem apenas um desses comutadores, mas grandes operações podem ter mais. No caso em que um agente tem dispositivos em mais de um sistema AD, o agente verá um número correspondente de objetos de manipulador de agente. Também haverá uma instância do objeto Agent relacionada à aparência do agente em cada sistema AD.

O objeto manipulador de agente expõe a interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) . Essa interface implementa métodos que fornecem informações sobre os [grupos de AD](#acd-group-object) associados ao manipulador de agente e os endereços que ele pode usar.

## <a name="agent-session-object"></a>Objeto de sessão do agente

Uma sessão de agente representa um agente que fez logon e é qualificado para lidar com chamadas para um determinado [grupo de AD](#acd-group-object). Uma sessão de agente é um objeto criado dinamicamente, que relaciona um agente a um grupo ad, para o qual eles fornecerão serviço, e também o endereço, em que eles receberão chamadas (Turret, estação, telefone, etc.). Os aplicativos podem usar o objeto de sessão do agente para acompanhar a atividade do agente em um determinado grupo de AD.

O objeto de sessão do agente expõe a interface [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) . Essa interface implementa métodos que podem recuperar informações como tempo médio de comunicação para uma chamada.

## <a name="acd-group-object"></a>Objeto de grupo ad

Um grupo ad representa uma classe de chamadas que requer um determinado tipo de manipulação. Por exemplo, algumas chamadas de entrada para o Call Center de um banco podem se preocupar com contas existentes e outras podem estar relacionadas a novas contas. Alguns agentes podem ter experiência em ambas as áreas, mas a maioria será especializada em uma. Grupos de AD serão criados para lidar com cada tipo de chamada. Um grupo ad serviços de uma ou mais filas. À medida que as chamadas de entrada são classificadas, elas serão passadas para filas associadas ao grupo ad relevante. Uma chamada que chega à fila é passada para um agente que criou um [objeto de sessão de agente](#agent-session-object) indicando que é capaz de lidar com chamadas desse grupo de AD.

O objeto de grupo ad expõe a interface [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) . Essa interface implementa métodos que fornecem acesso às filas associadas ao grupo ad atual.

## <a name="queue-object"></a>Objeto de fila

O objeto Queue representa um ponto dentro do sistema ad onde as chamadas são mantidas temporariamente pendentes. O objeto de fila expõe a interface [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) . Essa interface implementa métodos que reúnem estatísticas em uma fila, como o número de chamadas atualmente enfileiradas. O [proxy ad](acd-proxy.md) usa essas informações para distribuir chamadas para agentes e para produzir relatórios administrativos.

O acesso a um objeto de fila permite que um aplicativo Leia uma variedade de estatísticas padrão relacionadas ao uso da fila, mas não dá a ela a capacidade de controlar chamadas na fila. Somente os aplicativos com acesso aos endereços e linhas associados (normalmente o aplicativo de proxy AD) seriam capazes de controlar as chamadas na fila.

A maioria das filas está relacionada diretamente a um [objeto de grupo ad](#acd-group-object)e manterá uma chamada até que um agente possa tratá-lo. Outras filas podem existir para permitir guias de chamada complexos (o caminho definido, uma chamada não atendida, levará por um interruptor). Por exemplo, as chamadas podem ser colocadas em filas de retenção antes de serem roteadas para uma fila atendida por um grupo de AD.

 

 
