---
description: Os serviços Web na API de dispositivos (WSDAPI) fornecem suporte para o perfil de dispositivos para serviços Web (DPWS) no Windows Vista, que habilita a comunicação de serviços Web (WS) entre PCs baseados no Windows e dispositivos conectados à rede.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformidade de especificação do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169642"
---
# <a name="wsdapi-specification-compliance"></a>Conformidade de especificação do WSDAPI

Os serviços Web na API de dispositivos (WSDAPI) fornecem suporte para o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) no Windows Vista, que habilita a comunicação de serviços Web (WS) entre PCs baseados no Windows e dispositivos conectados à rede. O DPWS monta especificações básicas do WS, como [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), além de aprimorar ou restringir a capacidade de fornecer um conjunto de linha de base de recursos para dispositivos com restrição de recursos. Essa especificação de linha de base contém a funcionalidade necessária, como a capacidade de descrever as propriedades do dispositivo por meio de metadados e funcionalidade opcional, como a capacidade de rejeitar mensagens específicas por motivos de segurança.

A implementação de WSDAPI no Windows Vista é a primeira versão do suporte explícito para o DPWS e é uma implementação não gerenciada de DPWS que é separada e distinta de outras implementações de serviços da Web (como o [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

Os tópicos a seguir são de interesse dos fabricantes de dispositivos e outros implementadores de dispositivos que criam dispositivos que interoperam com clientes e hosts WSDAPI baseados no Windows sem usar o WSDAPI. Estes tópicos descrevem a implementação de WSDAPI em relação às especificações subjacentes. Eles abordam a implementação de funcionalidade necessária, funcionalidade opcional e funcionalidade adicional não definida na especificação.

-   [Conformidade de especificação do DPWS](dpws-specification-compliance.md)
-   [Conformidade de especificação do WS-Discovery](ws-discovery-specification-compliance.md)
-   [Conformidade de especificação WS-MetadataExchange e WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funcionalidade adicional de WS-Discovery](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de dispositivo WSD](wsd-device-development.md)
</dt> <dt>

[Recomendações de implementação de dispositivo WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
