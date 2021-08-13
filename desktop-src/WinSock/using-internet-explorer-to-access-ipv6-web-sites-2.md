---
description: "O Microsoft Internet Explorer dá suporte ao uso de IPv6 para conectar e acessar sites habilitados para IPv6 (servidores Web e servidores FTP, por exemplo) quando as seguintes circunstâncias são atendidas: o computador host que executa Internet Explorer deve ter o IPv6 instalado e habilitado. Ao se conectar a um host que está fora da sub-rede local, a interface que fornece a conectividade deve ter um endereço IPv6 rouco atribuído. Ao se conectar ao endereço de loopback IPv6 (::1) ou a um destino de link local, um endereço IPv6 stável não é necessário. Se a URL solicitada contiver um nome (www.contoso.com, por exemplo), a consulta DNS (Sistema de Nomes de Domínio) para esse nome deverá retornar um ou mais endereços IPv6. Se a URL solicitada contiver um endereço IPv6 (::1, por exemplo), o endereço IPv6 deverá estar entre colchetes (https:// \\[ ::1 \\] ). As IDs de escopo, às vezes chamadas de índices de zona, têm suporte como parte do endereço IPv6. A ID de escopo é usada para determinar qual interface de rede usar ao enviar a solicitação em computadores com vários interfaces de rede. A ID de escopo é especificada usando o caractere '%' após o endereço IPv6 principal (fe80::1%11, por exemplo). No entanto, o caractere '%' deve ser escapado na URL usada com Internet Explorer. Por exemplo, a ID de escopo 11 em um endereço local de link seria especificada como https:// \\[ fe80::1%2511 ao usar \\] Internet Explorer. Essa capacidade de usar endereços IPv6 em uma URL tem suporte Internet Explorer 7 e posteriores."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Usando Internet Explorer para acessar sites IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48a9f18e80e0e163ad6fe4ccda0aaef43826edd4becb28e294aad5eca7085c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559267"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Usando Internet Explorer para acessar sites IPv6

O Microsoft Internet Explorer dá suporte ao uso de IPv6 para conectar e acessar sites habilitados para IPv6 (servidores Web e servidores FTP, por exemplo) quando as seguintes circunstâncias são atendidas:

-   O computador host em Internet Explorer deve ter o IPv6 instalado e habilitado.
    -   Ao se conectar a um host que está fora da sub-rede local, a interface que fornece a conectividade deve ter um endereço IPv6 rouco atribuído.
    -   Ao se conectar ao endereço de loopback IPv6 (::1) ou a um destino de link local, um endereço IPv6 stável não é necessário.
-   Se a URL solicitada contiver um nome (www.contoso.com, por exemplo), a consulta DNS (Sistema de Nomes de Domínio) para esse nome deverá retornar um ou mais endereços IPv6.
-   Se a URL solicitada contiver um endereço IPv6 (::1, por exemplo), o endereço IPv6 deverá estar entre colchetes (https:// \[ ::1 \] ). As IDs de escopo, às vezes chamadas de índices de zona, têm suporte como parte do endereço IPv6. A ID de escopo é usada para determinar qual interface de rede usar ao enviar a solicitação em computadores com vários interfaces de rede. A ID de escopo é especificada usando o caractere '%' após o endereço IPv6 principal (fe80::1%11, por exemplo). No entanto, o caractere '%' deve ser escapado na URL usada com Internet Explorer. Por exemplo, a ID de escopo 11 em um endereço local de link seria especificada como https:// \[ fe80::1%2511 ao usar \] Internet Explorer. Essa capacidade de usar endereços IPv6 em uma URL tem suporte Internet Explorer 7 e posteriores.

> [!Note]  
> Se Internet Explorer estiver configurado para usar um servidor proxy, o servidor proxy deverá ter um endereço IPv6 atribuído e o servidor proxy deverá ser capaz de proxy de endereços IPv6. O servidor proxy seria usado para se conectar a um host externo usando IPv6. O servidor proxy normalmente seria ignorado para o endereço de loopback IPv6 e endereços locais de link IPv6.

 

 

 



