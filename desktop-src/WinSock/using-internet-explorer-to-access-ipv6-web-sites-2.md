---
description: "O Microsoft Internet Explorer dá suporte ao uso do IPv6 para conectar e acessar sites habilitados para IPv6 (servidores Web e servidores FTP, por exemplo) quando as seguintes circunstâncias são atendidas: o computador host executando o Internet Explorer deve ter o IPv6 instalado e habilitado. Ao se conectar a um host que está fora da sub-rede local, a interface que fornece a conectividade deve ter um endereço IPv6 roteável atribuído. Ao conectar-se ao endereço de loopback IPv6 (:: 1) ou a um destino de link local, um endereço IPv6 roteável não é necessário. Se a URL solicitada contiver um nome (www.contoso.com, por exemplo), a consulta do DNS (sistema de nomes de domínio) para esse nome deverá retornar um ou mais endereços IPv6. Se a URL solicitada contiver um endereço IPv6 (:: 1, por exemplo), o endereço IPv6 deverá estar entre colchetes (https:// \\[ :: 1 \\] ). As IDs de escopo, às vezes chamadas de índices de zona, têm suporte como parte do endereço IPv6. A ID do escopo é usada para determinar qual interface de rede usar ao enviar a solicitação em computadores com várias interfaces de rede. A ID do escopo é especificada usando o caractere '% ' após o endereço IPv6 principal (FE80:: 1% 11, por exemplo). No entanto, o caractere '% ' deve ser escapado na URL usada com o Internet Explorer. Por exemplo, a ID de escopo 11 em um endereço de link local seria especificada como https:// \\[ FE80:: 1% 2511 \\] ao usar o Internet Explorer. Essa capacidade de usar endereços IPv6 em uma URL tem suporte no Internet Explorer 7 e posterior."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Usando o Internet Explorer para acessar sites IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786158"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Usando o Internet Explorer para acessar sites IPv6

O Microsoft Internet Explorer dá suporte ao uso do IPv6 para conectar e acessar sites habilitados para IPv6 (servidores Web e servidores FTP, por exemplo) quando as seguintes circunstâncias são atendidas:

-   O computador host que executa o Internet Explorer deve ter o IPv6 instalado e habilitado.
    -   Ao se conectar a um host que está fora da sub-rede local, a interface que fornece a conectividade deve ter um endereço IPv6 roteável atribuído.
    -   Ao conectar-se ao endereço de loopback IPv6 (:: 1) ou a um destino de link local, um endereço IPv6 roteável não é necessário.
-   Se a URL solicitada contiver um nome (www.contoso.com, por exemplo), a consulta do DNS (sistema de nomes de domínio) para esse nome deverá retornar um ou mais endereços IPv6.
-   Se a URL solicitada contiver um endereço IPv6 (:: 1, por exemplo), o endereço IPv6 deverá estar entre colchetes (https:// \[ :: 1 \] ). As IDs de escopo, às vezes chamadas de índices de zona, têm suporte como parte do endereço IPv6. A ID do escopo é usada para determinar qual interface de rede usar ao enviar a solicitação em computadores com várias interfaces de rede. A ID do escopo é especificada usando o caractere '% ' após o endereço IPv6 principal (FE80:: 1% 11, por exemplo). No entanto, o caractere '% ' deve ser escapado na URL usada com o Internet Explorer. Por exemplo, a ID de escopo 11 em um endereço de link local seria especificada como https:// \[ FE80:: 1% 2511 \] ao usar o Internet Explorer. Essa capacidade de usar endereços IPv6 em uma URL tem suporte no Internet Explorer 7 e posterior.

> [!Note]  
> Se o Internet Explorer estiver configurado para usar um servidor proxy, o servidor proxy deverá ter um endereço IPv6 atribuído e o servidor proxy deverá ser capaz de fazer o proxy de endereços IPv6. O servidor proxy seria usado para se conectar a um host externo usando IPv6. O servidor proxy normalmente seria ignorado para o endereço de loopback IPv6 e endereços de link local IPv6.

 

 

 



