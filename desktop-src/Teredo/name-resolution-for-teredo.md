---
title: Resolução de nomes para Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Saiba mais sobre: resolução de nomes para Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b5d40fda0546c29bd7c47ee773977c374784c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768556"
---
# <a name="name-resolution-for-teredo"></a>Resolução de nomes para Teredo

Atualmente, a interface teredo utiliza os seguintes protocolos para a resolução de nomes:

## <a name="domain-name-system"></a>Sistema de nomes de domínio

O DNS (sistema de nomes de domínio) é atualmente a tecnologia de resolução de nomes mais proeminente na Internet. A maioria dos servidores Web registra endereços de URL com servidores DNS. No entanto, os endereços de uma rede doméstica não são registrados com servidores DNS, pois a maioria dos usuários domésticos Obtém endereços IP por meio do protocolo DHCP do seu provedor de serviços de Internet. As concessões de DHCP são de duração relativamente curta e levam de 48 a 72 horas para propagar um nome em toda a nuvem DNS. Como resultado, o DNS provou ser um método ineficaz de obter o endereço IP público de um usuário doméstico. Um endereço Teredo inclui o endereço IPv4 público e, portanto, herda pelo menos o mesmo volatilidade dos endereços IPv4. Portanto, os endereços Teredo atualmente não estão registrados no DNS.

## <a name="peer-name-resolution-protocol"></a>Protocolo PNRP

O PNRP (Peer Name Resolution Protocol) é uma tecnologia de DNS distribuída que armazena endereços IP em milhares de computadores de usuário que fazem parte de uma nuvem PNRP. Usando o Windows Vista, qualquer usuário doméstico pode optar por se tornar membro de uma nuvem PNRP e anunciar seu endereço IPv6 Teredo na rede PNRP. Ao contrário dos endereços fornecidos aos servidores DNS, os endereços na rede PNRP geralmente levam menos de um minuto para serem propagados. Como os endereços Teredo podem ser alterados com frequência (o endereço IPv4 externo fornecido pelo ISP pode ser alterado ou a porta externa usada pelo dispositivo de gateway de Internet do usuário pode ser alterada), o PNRP provou ser um mecanismo eficaz para os usuários domésticos. Nomes PNRP, endereços que terminam com ". pnrp.net" são baseados em propriedades exclusivas do sistema que não são alteradas. Como resultado, um nome PNRP é uma maneira confiável de se conectar a um usuário doméstico. A API [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) pode ser usada para obter o endereço IP usando a tecnologia PNRP (nomes DNS que terminam com ". PNRP.net") e estabelecer conexão com outros hosts.

 

 
