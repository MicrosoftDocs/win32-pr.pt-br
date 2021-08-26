---
title: Recebendo tráfego não solicitado em Teredo
description: O Teredo fornece conectividade global usando recursos de travessia IPv6 e NAT.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca6a4a6580200eee1f039fc87da29515db00a29f94700ff02548c38ba776f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099626"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Recebendo tráfego não solicitado em Teredo

[O Teredo](about-teredo.md) fornece conectividade global usando recursos de travessia IPv6 e NAT. No entanto, muitos aplicativos, incluindo ponto a ponto, exigirão que o Teredo receba tráfego não solicitado da Internet. Um aplicativo pode ser programado para receber tráfego em uma única interface IPv6 ou em todas as interfaces com capacidade para IPv6. Esta documentação descreve os requisitos para aplicativos que usam a interface Teredo para receber tráfego IPv6 não solicitado.

Um aplicativo receberá tráfego não solicitado pela interface Teredo somente se o aplicativo estiver registrado no [firewall Windows .](/previous-versions/windows/desktop/ics/windows-firewall-start-page) Para receber o tráfego não solicitado, o seguinte deve ocorrer:

-   Os usuários devem ser instruídos a usar o MMC (Console de Gerenciamento Microsoft) para habilitar a opção "Travessia de Borda" para um aplicativo. Essa opção está disponível na Windows Firewall Snap-In --> <application name> --> guia "Avançado". A opção "Travessia de Borda" deve ser habilitada individualmente para cada aplicativo.

-   A opção "Travessia de Borda" está habilitada pelo aplicativo. É possível que os aplicativos capazes de receber tráfego não solicitado registrem-se com o firewall do Windows para "Travessia de Borda" e recebam tráfego não solicitado pela interface Teredo. Para fazer isso, um aplicativo deve chamar a API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) com a opção "Travessia de Borda" definida como VARIANT \_ TRUE. O consentimento do usuário é necessário para essa chamada à API antes que um aplicativo seja autorizado a escutar o tráfego.

-   O aplicativo define a opção de soquete [WINSOCK IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) como **PROTECTION LEVEL \_ \_ UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt). Isso permitirá que o aplicativo receba tráfego de Travessia do Edge.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recebendo tráfego solicitado em Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 