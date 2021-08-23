---
description: Um programa de controle de serviço inicia e controla os serviços.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programas de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889039"
---
# <a name="service-control-programs"></a>Programas de controle de serviço

Um programa de controle de serviço inicia e controla os serviços. Ele executa as seguintes ações:

-   Inicia um serviço de serviço ou de driver se o tipo de inicialização for início da demanda de serviço \_ \_ .
-   Envia solicitações de controle para um serviço em execução.
-   Consulta o status atual de um serviço em execução.

Essas ações exigem um identificador aberto para o objeto de serviço. Para obter o identificador, o programa de controle de serviço deve:

1.  Use a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obter um identificador para o banco de dados SCM em um computador especificado.
2.  Use a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obter um identificador para o objeto de serviço.

Para obter mais informações, consulte estes tópicos:

-   [Inicialização do serviço](service-startup.md)
-   [Solicitações de controle de serviço](service-control-requests.md)
-   [Controlando um serviço usando SC](controlling-a-service-using-sc.md)

 

 



