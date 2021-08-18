---
description: os serviços web na API de dispositivos (WSDAPI) fornecem suporte para o perfil de dispositivos para serviços Web (DPWS) no Windows Vista, que habilita a comunicação de serviços web (WS) entre PCs com Windows e dispositivos conectados à rede.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformidade de especificação do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991386"
---
# <a name="wsdapi-specification-compliance"></a>Conformidade de especificação do WSDAPI

os serviços web na API de dispositivos (WSDAPI) fornecem suporte para o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) no Windows Vista, que habilita a comunicação de serviços web (WS) entre PCs com Windows e dispositivos conectados à rede. O DPWS monta especificações básicas do WS, como [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), além de aprimorar ou restringir a capacidade de fornecer um conjunto de linha de base de recursos para dispositivos com restrição de recursos. Essa especificação de linha de base contém a funcionalidade necessária, como a capacidade de descrever as propriedades do dispositivo por meio de metadados e funcionalidade opcional, como a capacidade de rejeitar mensagens específicas por motivos de segurança.

a implementação de WSDAPI no Windows Vista é a primeira versão do suporte explícito para o DPWS e é uma implementação não gerenciada de DPWS que é separada e distinta de outras implementações de serviços da Web (como o [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

os tópicos a seguir são de interesse dos fabricantes de dispositivos e outros implementadores de dispositivos que criam dispositivos que interoperam com clientes e hosts WSDAPI baseados em Windows sem usar o WSDAPI. Estes tópicos descrevem a implementação de WSDAPI em relação às especificações subjacentes. Eles abordam a implementação de funcionalidade necessária, funcionalidade opcional e funcionalidade adicional não definida na especificação.

-   [Conformidade de especificação do DPWS](dpws-specification-compliance.md)
-   [Conformidade de especificação do WS-Discovery](ws-discovery-specification-compliance.md)
-   [Conformidade de especificação WS-MetadataExchange e WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funcionalidade adicional de WS-Discovery](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de dispositivo WSD](wsd-device-development.md)
</dt> <dt>

[Recomendações de implementação do dispositivo WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
