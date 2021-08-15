---
description: O sistema usa as informações de configuração para determinar como iniciar o serviço.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuração de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f64b5cef835e1c7efef10c12555c81c132e707c8d1fb2814a7fcb95cf6d71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889076"
---
# <a name="service-configuration"></a>Configuração de Serviço

O sistema usa as informações de configuração para determinar como iniciar o serviço. As informações de configuração também incluem o nome de exibição do serviço e sua descrição. Por exemplo, para o serviço DHCP, você pode usar o nome de exibição "Serviço de Protocolo de Configuração de Host Dinâmico" e a descrição "Fornece endereços de Internet para o computador em sua rede".

Para modificar as informações de configuração de um objeto de serviço, um programa de configuração usa a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) Para ver um exemplo, consulte [Alterando uma configuração de serviço](changing-a-service-configuration.md).

Para recuperar as informações de configuração de um objeto de serviço, o programa de configuração usa a função [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) ou [**QueryServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) Para ver um exemplo, consulte [Consultando a configuração de um serviço.](querying-a-service-s-configuration.md)

As funções de configuração de serviço [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) são suportadas pelo uso de gatilhos para controlar o início do serviço.

Para modificar o descritor de segurança para um objeto SCManager ou um objeto de serviço, um programa de configuração usa a [**função SetServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) Para recuperar uma cópia do descritor de segurança, o programa de configuração usa a [**função QueryServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um serviço usando SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
