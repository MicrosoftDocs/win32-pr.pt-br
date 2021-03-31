---
description: Um programa de serviço contém código executável para um ou mais serviços.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836973"
---
# <a name="service-programs"></a>Programas de serviço

Um *programa de serviço* contém código executável para um ou mais serviços. Um programa de serviço criado com o próprio processo do tipo serviço do \_ Win32 \_ \_ contém o código para apenas um serviço. Um programa de serviço criado com o processo de compartilhamento Win32 do serviço de tipo \_ \_ \_ contém código para mais de um serviço, permitindo que eles compartilhem código. Um exemplo de um programa de serviço que faz isso é o processo de host de serviço genérico, Svchost.exe, que hospeda serviços internos do Windows. Observe que Svchost.exe é reservado para uso pelo sistema operacional e não deve ser usado por serviços que não sejam do Windows. Em vez disso, os desenvolvedores devem implementar seus próprios programas de Hospedagem de serviços.

Um programa de serviço pode ser configurado para ser executado no contexto de uma conta de usuário tanto do domínio interno (local), primário ou confiável. Ele também pode ser configurado para ser executado em uma [conta de usuário de serviço](service-user-accounts.md)especial.

Os tópicos a seguir descrevem os requisitos de interface do SCM ( [Gerenciador de controle de serviço](service-control-manager.md) ) que um programa de serviço deve incluir:

-   [Ponto de entrada de serviço](service-entry-point.md)
-   [Função Service-Main](service-servicemain-function.md)
-   [Função do manipulador do controle de serviço](service-control-handler-function.md)

Esses tópicos não se aplicam aos serviços de driver. Para obter os requisitos de interface dos serviços de driver, consulte o WDK (Windows Driver Kit).

Um serviço é executado como um processo em segundo plano que pode afetar o desempenho do sistema, a capacidade de resposta, a eficiência de energia e a segurança. Para obter diretrizes de otimização de serviço, consulte [desenvolvendo processos em segundo plano eficientes para o Windows](/windows-hardware/drivers/kernel/implementing-power-management). Os tópicos a seguir descrevem considerações de programação adicionais:

-   [Transições de estado do serviço](service-status-transitions.md)
-   [Recebendo eventos em um serviço](receiving-events-in-a-service.md)
-   [Serviços multithread](multithreaded-services.md)
-   [Serviços e o registro](services-and-the-registry.md)
-   [Serviços e unidades redirecionadas](services-and-redirected-drives.md)
-   [Eventos de gatilho de serviço](service-trigger-events.md)

Observe que, se o programa de serviço funcionar como um servidor RPC, ele deverá usar pontos de extremidade dinâmicos e autenticação mútua.

 

 
