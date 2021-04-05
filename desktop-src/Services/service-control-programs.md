---
description: Um programa de controle de serviço inicia e controla os serviços.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programas de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827021"
---
# <a name="service-control-programs"></a>Programas de controle de serviço

Um programa de controle de serviço inicia e controla os serviços. Ele executa as seguintes ações:

-   Inicia um serviço de serviço ou de driver se o tipo de inicialização for início da demanda de serviço \_ \_ .
-   Envia solicitações de controle para um serviço em execução.
-   Consulta o status atual de um serviço em execução.

Essas ações exigem um identificador aberto para o objeto de serviço. Para obter o identificador, o programa de controle de serviço deve:

1.  Use a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obter um identificador para o banco de dados SCM em um computador especificado.
2.  Use a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obter um identificador para o objeto de serviço.

Para mais informações, consulte os seguintes tópicos:

-   [Inicialização do serviço](service-startup.md)
-   [Solicitações de controle de serviço](service-control-requests.md)
-   [Controlando um serviço usando SC](controlling-a-service-using-sc.md)

 

 



