---
description: O sistema usa as informações de configuração para determinar como iniciar o serviço.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuração de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501579"
---
# <a name="service-configuration"></a>Configuração de Serviço

O sistema usa as informações de configuração para determinar como iniciar o serviço. As informações de configuração também incluem o nome de exibição do serviço e sua descrição. Por exemplo, para o serviço DHCP, você pode usar o nome de exibição "serviço de protocolo de configuração de host dinâmico" e a descrição "fornece endereços de Internet para o computador em sua rede".

Para modificar as informações de configuração de um objeto de serviço, um programa de configuração usa a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) . Para obter um exemplo, consulte [alterando uma configuração de serviço](changing-a-service-configuration.md).

Para recuperar as informações de configuração de um objeto de serviço, o programa de configuração usa a função [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) ou [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) . Para obter um exemplo, consulte [consultando a configuração de um serviço](querying-a-service-s-configuration.md).

As funções de configuração do serviço [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) dão suporte ao uso de gatilhos para controlar o início do serviço.

Para modificar o descritor de segurança para um objeto SCManager ou um objeto de serviço, um programa de configuração usa a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Para recuperar uma cópia do descritor de segurança, o programa de configuração usa a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um serviço usando SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
