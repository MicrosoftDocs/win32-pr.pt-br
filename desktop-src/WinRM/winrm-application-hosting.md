---
title: Infraestrutura para gerenciar serviços hospedados
description: Gerenciamento Remoto do Windows 2,0 (WinRM) apresenta uma estrutura de hospedagem. Para usar a estrutura, os plug-ins do WinRM são escritos para expor dados de gerenciamento de um aplicativo na infraestrutura do WinRM.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292782"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infraestrutura para gerenciar serviços hospedados

Gerenciamento Remoto do Windows 2,0 (WinRM) apresenta uma estrutura de hospedagem. Para usar a estrutura, os plug-ins do WinRM são escritos para expor dados de gerenciamento de um aplicativo na infraestrutura do WinRM. Há suporte para dois modelos de hospedagem. Uma é Serviços de Informações da Internet (IIS) â € "com base no serviço e o outro é WinRMâ". O modelo baseado em WinRM usa HTTP.sys e não depende do IIS.

As seções a seguir descrevem os modelos de hospedagem:

-   [Modelo de Hospedagem de extensão do IIS do WinRM](#winrm-iis-extension-hosting-model)
    -   [Balanceamento de carga no modelo de Hospedagem de extensão do IIS do WinRM](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Redirecionamento de HTTP no modelo de Hospedagem de extensão do IIS do WinRM](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modelo de hospedagem do serviço WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modelo de Hospedagem de extensão do IIS do WinRM

O módulo de extensão do IIS do WinRM é um componente opcional que é instalado usando o **Gerenciador do servidor**. O módulo de extensão do IIS do WinRM é usado para criar pontos de extremidade habilitados para WinRMâ de dentro do serviço IIS. Esse módulo pode ser habilitado no nível do site ou do diretório virtual. Ele funciona interceptando e redirecionando as solicitações de entrada para o site ou diretório virtual associado. As solicitações são redirecionadas para um módulo do WinRM que analisa o conteúdo e, em seguida, determina qual plug-in WinRM está configurado para lidar com cada solicitação. Para obter mais informações, consulte [configuração de plug-in do host do IIS](iis-host-plug-in-configuration.md).

O modelo de Hospedagem de extensão do IIS do WinRM foi projetado para lidar com um grande volume de solicitações. Se o modelo baseado no IIS for usado como a estrutura de hospedagem, os seguintes recursos estarão disponíveis:

-   Os módulos de autenticação padrão do IIS.
-   O processo do pool de aplicativos do IIS para hospedar todos os plug-ins.
-   Gerenciamento de cotas para limitação de usuários pesados do sistema. Para obter mais informações, consulte [Gerenciamento de cota para shells remotos](quotas.md).
-   Um modelo de plug-in de Shell. Consulte [API do shell do cliente WinRM](client-shell-api.md).
-   Um modelo de autorização flexível. Consulte [API de plug-in do WinRM](winrm-plugin-api.md).

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Balanceamento de carga no modelo de Hospedagem de extensão do IIS do WinRM

A maioria dos balanceadores de carga (LBs) dá suporte a um modelo de adesão baseado em cookie. O LB insere um cookie na resposta à primeira solicitação do cliente. Para todas as solicitações subsequentes, o cookie é transmitido na solicitação e o LB usa o cookie para rotear a solicitação para o servidor apropriado.

Em ambientes em que o WinRM 2,0 é hospedado por trás de um LB, o LB deve ser configurado para prefixar MS-WSMAN para o nome do cookie. Além disso, o LB precisa ser configurado para permitir que o tempo de vida do cookie seja infinito, pois o cliente WinRM deve controlar por quanto tempo o cookie é válido.

Veja a seguir um exemplo de um nome de cookie:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Redirecionamento de HTTP no modelo de Hospedagem de extensão do IIS do WinRM

O WinRM 2,0 pode lidar com o redirecionamento de HTTP. É recomendável que todo o redirecionamento use protocolo SSL (SSL) e que todos os aplicativos validem o URI Redirecionado antes de criar uma nova sessão.

## <a name="winrm-service-hosting-model"></a>Modelo de hospedagem do serviço WinRM

O modelo baseado em serviço WinRM é executado sobre HTTP.sys. O serviço WinRM é um serviço voltado para a rede que lida com solicitações de clientes WinRM. O serviço determina se a solicitação é roteada para um plug-in que é executado no serviço principal ou é roteado por meio de um host onde o plug-in de terceiros é executado. Esse modelo destina-se a cenários em que a carga no nó gerenciado está baixa. Além disso, esse modelo destina-se a cenários em que a hospedagem do IIS não é uma opção. Para obter mais informações, consulte [configuração de plug-in do serviço WinRM](wsman-service-plug-in-configuration.md).

 

 




