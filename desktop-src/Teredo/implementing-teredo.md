---
title: Implementando o Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Saiba mais sobre: Implementando o Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b24f4524d6c513dc0a5cd11e7f6420eb7e546fa3bce75c830759fc38faaef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681646"
---
# <a name="implementing-teredo"></a>Implementando o Teredo

Embora não seja necessário fazer alterações de programação para [Teredo](about-teredo.md), é recomendável que os desenvolvedores façam pequenas alterações que resultem no uso mais eficiente da interface Teredo:

-   É possível para aplicativos que só são capazes de utilizar o Teredo. No entanto, o processamento de tráfego IPv4 e IPv6 deve ser levado em consideração ao desenvolver o protocolo de aplicativo. O aplicativo precisará se ligar a AF \_ INET6 ou AF \_ inspec em opções de soquete.
-   os aplicativos que são capazes de escutar o tráfego não solicitado da Internet são necessários para habilitar a opção de passagem NAT (conversão de endereços de rede) dentro do Windows Firewall. Isso é feito chamando a API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) com a opção "travessia de borda" definida como Variant \_ true. Windows O vista garante que o endereço Teredo esteja disponível para uso quando um aplicativo o exigir. Como resultado, o endereço Teredo é estabilizado automaticamente quando a interface Teredo é usada. Se um aplicativo quiser garantir que o endereço Teredo seja estável, chamar a API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) acionará o Teredo para fazer a transição para um estado estável.
-   Os aplicativos também podem usar a opção de soquete WinSock de [ \_ \_ nível de proteção IPv6](/windows/desktop/WinSock/ipv6-protection-level) para definir o nível de proteção, que permite que o tráfego de entrada não solicitado passe pelo firewall. Consulte [recebendo tráfego não solicitado sobre Teredo](receiving-unsolicited-traffic-over-teredo.md) para obter mais informações.

A implementação do auxiliar de protocolo de Internet (auxiliar de IP) de funções Teredo específicas serve como um exemplo de como o endereço Teredo pode ser verificado e disponibilizado para um aplicativo. Para obter mais informações, consulte [usando Teredo com auxiliar de IP](using-teredo-with-ip-helper.md).

 

 
