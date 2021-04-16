---
title: Configuração da instalação
description: A configuração da instalação requer privilégios de administrador e é persistente entre as reinicializações.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43b543bfc81f963341d7b5f690f4b40312ee420
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498609"
---
# <a name="setup-configuration"></a>Configuração da instalação

A configuração da instalação requer privilégios de administrador e é persistente entre as reinicializações. Normalmente, um aplicativo de instalação em execução com privilégios de administrador executa essa configuração persistente durante a instalação para que os aplicativos possam, então, executar com privilégios mais baixos, embora a configuração persistente possa ser feita a qualquer momento. A configuração da instalação pode incluir qualquer uma das quatro atividades a seguir:

-   Criando uma reserva de URL. A API HTTP permite que o aplicativo de instalação Reserve prefixos de URL para filas de solicitações associadas a aplicativos específicos. Para reservar uma URL, o aplicativo de instalação chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro *configid* definido como **HttpServiceConfigUrlAclInfo** e passa um ponteiro no parâmetro *pConfigInformation* para uma estrutura de conjunto de [**URLACL do \_ serviço http \_ config \_ \_**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) que contém as informações de registro. Para obter mais informações, consulte [reservas de namespace, registros e roteamento](namespace-reservations-registrations-and-routing.md).
-   Configurando SSL. Para configurar o SSL, o administrador chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro *configid* definido como **HttpServiceConfigSSLCertInfo** e passa um ponteiro no parâmetro *pConfigInformation* para uma estrutura de conjunto de [**SSL de \_ configuração de serviço \_ \_ \_ http**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) que contém as informações do certificado SSL.
-   Definir outras configurações persistentes de servidor HTTP, como os endereços IP nos quais o servidor HTTP escutará e o valor de tempo limite de todo o servidor. Consulte [lista de escuta de IP](ip-listen-list.md) e [**\_ \_ \_ tempo limite \_ de configuração do serviço http definido**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




