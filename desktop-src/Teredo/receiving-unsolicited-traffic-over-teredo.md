---
title: Recebendo tráfego não solicitado por Teredo
description: O Teredo fornece conectividade global usando recursos de passagem de NAT e IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641535"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Recebendo tráfego não solicitado por Teredo

O [Teredo](about-teredo.md) fornece conectividade global usando recursos de passagem de NAT e IPv6. No entanto, muitos aplicativos, incluindo ponto a ponto, exigirão que o Teredo receba tráfego não solicitado da Internet. Um aplicativo pode ser programado para receber tráfego em uma única interface IPv6 ou em todas as interfaces compatíveis com IPv6. Esta documentação descreve os requisitos para aplicativos que usam a interface Teredo para receber tráfego IPv6 não solicitado.

Um aplicativo receberá tráfego não solicitado pela interface teredo somente se o aplicativo estiver registrado no firewall do [Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page). Para receber o tráfego não solicitado, deve ocorrer o seguinte:

-   Os usuários devem ser instruídos a usar o MMC (console de gerenciamento Microsoft) para habilitar a opção de "passagem de borda" para um aplicativo. Essa opção está disponível em Firewall do Windows Snap-In--> <application name> --> guia "avançado". A opção "travessia de borda" deve ser habilitada individualmente para cada aplicativo.

-   A opção "travessia de borda" é habilitada pelo aplicativo. É possível que aplicativos com capacidade de receber tráfego não solicitado registrem-se no firewall do Windows para "travessia de borda" e recebam tráfego não solicitado pela interface teredo. Para fazer isso, um aplicativo deve chamar a API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) com a opção "travessia de borda" definida como Variant \_ true. O consentimento do usuário é necessário para essa chamada à API antes que um aplicativo tenha permissão para escutar o tráfego.

-   O aplicativo define a opção de soquete de [ \_ \_ nível de proteção](/windows/desktop/WinSock/ipv6-protection-level) do Winsock IPv6 para o **nível de proteção \_ \_ irrestrito** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt). Isso permitirá que o aplicativo receba o tráfego de percurso de borda.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recebendo tráfego solicitado por Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 