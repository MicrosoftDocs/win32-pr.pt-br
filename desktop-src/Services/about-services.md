---
description: O SCM (Gerenciador de controle de serviços) mantém um banco de dados de serviços e serviços de driver instalados e fornece meios unificados e seguros de controlá-los.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Sobre serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922098"
---
# <a name="about-services"></a>Sobre serviços

O SCM ( [Gerenciador de controle de serviços](service-control-manager.md) ) mantém um banco de dados de serviços e serviços de driver instalados e fornece meios unificados e seguros de controlá-los. O banco de dados inclui informações sobre como cada serviço de serviço ou de driver deve ser iniciado. Ele também permite que os administradores de sistema personalizem os requisitos de segurança para cada serviço e, portanto, controlem o acesso ao serviço.

Os tipos de programas a seguir usam as funções fornecidas pelo SCM.



| Tipo                          | Descrição                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programa de serviço               | Um programa que fornece código executável para um ou mais serviços. Os programas de serviço usam funções que se conectam ao SCM e enviam informações de status para o SCM.                                                                                                                                                                          |
| Programa de configuração de serviço | Um programa que consulta ou modifica o banco de dados de serviços. Os programas de configuração de serviço usam funções que abrem o banco de dados, instalam ou excluem serviços no banco de dados e consultam ou modificam os parâmetros de configuração e segurança dos serviços instalados. Os programas de configuração de serviço gerenciam serviços e serviços de driver. |
| Programa de controle de serviço       | Um programa que inicia e controla serviços e serviços de driver. Os programas de controle de serviço usam funções que enviam solicitações para o SCM, que realiza a solicitação.                                                                                                                                                                     |



 

Esta visão geral aborda os seguintes tópicos:

-   [Gerenciador de Controle de Serviço](service-control-manager.md)
-   [Programas de serviço](service-programs.md)
-   [Programas de configuração de serviço](service-configuration-programs.md)
-   [Programas de controle de serviço](service-control-programs.md)
-   [Contas de usuário de serviço](service-user-accounts.md)
-   [Serviços interativos](interactive-services.md)
-   [Segurança do serviço e direitos de acesso](service-security-and-access-rights.md)
-   [Depurar um serviço](debugging-a-service.md)
-   [Eventos de gatilho de serviço](service-trigger-events.md)

 

 



