---
title: Sobre o EAP
description: EAP (Protocolo de Autenticação Extensível), um padrão com suporte de muitos componentes de rede da Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticação extensível, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84866f7f550213850bf95c39a6f0847df31bed3550db66139f2ec30bf921b5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276039"
---
# <a name="about-eap"></a>Sobre o EAP

Este tópico descreve o Protocolo de Autenticação Extensível (EAP), um padrão com suporte de muitos componentes de rede da Microsoft.

## <a name="eap-components"></a>Componentes de EAP

A EAP é crucial para proteger a segurança de LANs sem fio (802.1X), LANs com fio e VPNs (Redes Privadas Virtuais) e discadas.

Os componentes a seguir são suportados pelo protocolo EAP.

-   Os Clientes e Servidores de Acesso Remoto da Microsoft para discagem e VPN (PPTP e L2TP/IPSec) implementam o EAP como uma extensão para PPP. Para obter mais informações, [consulte RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Os clientes lan sem fio e com fio compatíveis com o Microsoft IEEE 802.1X implementam o EAP conforme definido no padrão de rascunho do IEEE 802.1X.
-   O servidor RADIUS da Microsoft, chamado IAS (Serviço de Autenticação da Internet), implementa o EAP conforme definido [no RFC 2865.](https://go.microsoft.com/fwlink/p/?linkid=84055)

Todos os componentes acima suportam essa arquitetura extensível por meio do SDK (Software Development Kit) do Microsoft Windows, possibilitando a integração de módulos de autenticação de terceiros. Esse mecanismo extensível pode ser usado para dar suporte a cartões de token, kerberos, chave pública e protocolos de autenticação S/Key.

## <a name="protected-extensible-authentication-protocol"></a>Protocolo de autenticação extensível protegido

Além do EAP, a implementação sem fio (802.1X) e o servidor RADIUS também suportam um padrão emergente chamado PEAP (EAP Protegido).

O PEAP fornece vários serviços principais para outros protocolos de autenticação EAP, da seguinte forma.

-   O PEAP criptografa pacotes EAP de outros protocolos de autenticação EAP usando o protocolo TLS, uma tecnologia baseada em protocolo SSL. Para obter mais informações, [consulte RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   O PEAP autentica o lado do servidor usando um Certificado do Servidor, com o servidor RADIUS.
-   O PEAP oferece capacidade de re-autenticação rápida que dá suporte a roaming eficiente entre dispositivos sem fio.
-   O PEAP gerencia a fragmentação e o re assembly de pacotes EAP.
-   O PEAP gera chaves usadas para criptografar o tráfego sem fio.

O PEAP torna muito mais fácil escrever um protocolo EAP porque o programador não precisa mais resolver esses problemas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre EAP e EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




