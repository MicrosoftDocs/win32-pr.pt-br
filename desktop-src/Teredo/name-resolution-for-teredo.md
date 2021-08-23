---
title: Resolução de nomes para Teredo
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 'Saiba mais sobre: Resolução de nomes para Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d9c41685977ef5a4ae3e94996a8d1a59db5f9812e2ed8efe758878a9055c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001684"
---
# <a name="name-resolution-for-teredo"></a>Resolução de nomes para Teredo

Atualmente, a interface Teredo utiliza os seguintes protocolos para resolução de nomes:

## <a name="domain-name-system"></a>Sistema de nomes de domínio

Atualmente, o DNS (Sistema de Nomes de Domínio) é a tecnologia de resolução de nomes mais proeminente na Internet. A maioria dos servidores Web registra endereços de URL com servidores DNS. No entanto, os endereços de uma rede inicial não são registrados com servidores DNS, pois a maioria dos usuários da página inicial obtém endereços IP por meio do protocolo DHCP de seu Provedor de Serviços de Internet. As concessões de DHCP são de duração relativamente curta e levam de 48 a 72 horas para propagar um nome em toda a nuvem DNS. Como resultado, o DNS se mostrou um método ineficaz de obter o endereço IP público de um usuário residencial. Um endereço Teredo inclui o endereço IPv4 público e, portanto, herda pelo menos a mesmaity dos endereços IPv4. Portanto, os endereços Teredo não estão registrados no DNS no momento.

## <a name="peer-name-resolution-protocol"></a>Protocolo PNRP

O PROTOCOLO PNRP é uma tecnologia DNS distribuída que armazena endereços IP em milhares de máquinas de usuário que fazem parte de uma nuvem PNRP. Usando Windows Vista, qualquer usuário residencial pode optar por se tornar um membro de uma nuvem PNRP e anunciar seu endereço Teredo IPv6 na rede PNRP. Ao contrário dos endereços dados aos servidores DNS, os endereços na rede PNRP geralmente levam menos de um minuto para se propagarem. Como os endereços Teredo podem mudar com frequência (o endereço IPv4 externo fornecido pelo ISP pode mudar ou a porta externa usada pelo dispositivo de gateway de Internet do usuário pode mudar), o PNRP se mostrou um mecanismo eficaz para usuários em casa. Nomes PNRP, endereços que terminam com ".pnrp.net" são baseados em propriedades exclusivas do sistema que não são alteradas. Como resultado, um nome PNRP é uma maneira confiável de se conectar a um usuário de casa. A API [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) pode ser usada para obter o endereço IP usando a tecnologia PNRP (nomes DNS que terminam com ".pnrp.net") e estabelecer conexão com outros hosts.

 

 
