---
title: Sobre o EAP
description: EAP (Extensible Authentication Protocol), um padrão compatível com muitos componentes de rede da Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticação extensível, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366830"
---
# <a name="about-eap"></a>Sobre o EAP

Este tópico descreve o protocolo EAP (Extensible Authentication Protocol), um padrão compatível com muitos componentes de rede da Microsoft.

## <a name="eap-components"></a>Componentes do EAP

O EAP é crucial para proteger a segurança de LANs sem fio (802.1 X), LANs com fio e dial-up e redes virtuais privadas (VPNs).

Os componentes a seguir dão suporte ao protocolo EAP.

-   Os clientes e servidores de acesso remoto da Microsoft para dial-up e VPN (PPTP e L2TP/IPSec) implementam o EAP como uma extensão para o PPP. Para obter mais informações, consulte [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Os clientes compatíveis com redes locais com fio e Wireless do Microsoft IEEE 802.1 X e com fio implementam o EAP conforme definido no padrão de rascunho IEEE 802.1 X.
-   O servidor RADIUS da Microsoft, chamado IAS (serviço de autenticação da Internet), implementa o EAP conforme definido no [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).

Todos os componentes acima dão suporte a essa arquitetura extensível por meio do SDK (Software Development Kit) do Microsoft Windows, possibilitando a integração de módulos de autenticação de terceiros. Esse mecanismo extensível pode ser usado para dar suporte a placas de token, Kerberos, chave pública e protocolos de autenticação de chave/S.

## <a name="protected-extensible-authentication-protocol"></a>Protocolo de autenticação extensível protegida

Além do EAP, a implementação sem fio (802.1 X) e o servidor RADIUS também oferecem suporte a um padrão emergente chamado EAP protegido (PEAP).

O PEAP fornece vários serviços importantes para outros protocolos de autenticação EAP, da seguinte maneira.

-   O PEAP criptografa pacotes EAP de outros protocolos de autenticação EAP usando o protocolo TLS, uma tecnologia baseada em SSL (Secure Socket Layer). Para obter mais informações, consulte [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   O PEAP autentica o lado do servidor usando um certificado de servidor, com o servidor RADIUS.
-   O PEAP oferece capacidade de reautenticação rápida que dá suporte a roaming eficiente entre dispositivos sem fio.
-   O PEAP gerencia a fragmentação e a remontagem de pacotes EAP.
-   O PEAP gera chaves usadas para criptografar o tráfego sem fio.

O PEAP torna muito mais fácil escrever um protocolo EAP, pois o programador não precisa mais resolver esses problemas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o EAP e o EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




