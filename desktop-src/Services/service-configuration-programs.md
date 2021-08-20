---
description: Os programadores e administradores do sistema usam programas de configuração de serviço para modificar ou consultar o banco de dados dos serviços instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuração de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad7ef3efffb185b2d29c6eab496bf76d12343a0e16f845702e910695220b048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967700"
---
# <a name="service-configuration-programs"></a>Programas de configuração de serviço

Os programadores e administradores do sistema usam programas de configuração de serviço para modificar ou consultar o banco de dados dos serviços instalados. O banco de dados também pode ser acessado usando as funções de registro. No entanto, você deve usar apenas as funções de configuração do SCM, que garantem que o serviço esteja instalado e configurado corretamente.

As funções de configuração do SCM exigem um identificador para um objeto SCManager ou um identificador para um objeto de serviço. Para obter esses identificadores, o programa de configuração de serviço deve:

1.  Use a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obter um identificador para o banco de dados SCM em um computador especificado.
2.  Use a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obter um identificador para o objeto de serviço.

Para obter mais informações, consulte estes tópicos:

-   [Instalação, remoção e enumeração de serviço](service-installation-removal-and-enumeration.md)
-   [Configuração de serviço](service-configuration.md)
-   [Configurando um serviço usando SC](configuring-a-service-using-sc.md)

 

 



