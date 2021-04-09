---
description: A primeira configuração não requer nenhuma configuração adicional além da instalação do protocolo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuração 1: sub-rede única com endereços de link local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010494"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Configuração 1: sub-rede única com endereços de link local

A primeira configuração não requer nenhuma configuração adicional além da instalação do protocolo Microsoft IPv6 Technology Preview. Essa configuração consiste em pelo menos dois nós na mesma sub-rede. Na terminologia IPv6, os dois nós estão no mesmo link sem roteadores intermediários.

A ilustração a seguir mostra a configuração de dois nós em uma única sub-rede usando endereços de link local.

![dois nós usando endereços de link local.](images/v6mig-1.png)

Por padrão, o IPv6 configura endereços IP de link local para cada interface correspondente aos adaptadores de rede Ethernet instalados. Os endereços de link local têm o prefixo FE80::/64. Os últimos 64 bits do endereço IPv6 são conhecidos como o identificador de interface e são derivados do endereço MAC de 48 bits do adaptador de rede.

Para criar o identificador de interface IPv6 do endereço Ethernet MAC de 48 bits (6 bytes):

-   Os dígitos hexadecimais 0xFF-FE são inseridos entre o terceiro e o quarto byte do endereço MAC.
-   O bit Universal/local, o segundo bit de ordem inferior do primeiro byte do endereço MAC, é complementado. Se for 1, ele será ativado como 0 e, se for 0, será ativado como 1.

Por exemplo, para o endereço MAC 00-60-08-52-F9-D8:

-   Os dígitos hexadecimais 0xFF-FE são inseridos entre 0x08 (o terceiro byte) e 0x52 (o quarto byte) do endereço MAC, que formam o endereço de 64 bits 00-60-08-FF-FE-52-F9-D8.
-   O bit Universal/local, o segundo bit de ordem inferior de 0x00 (o primeiro byte) do endereço MAC é complementado. O segundo bit de ordem inferior de 0x00 é 0, que, quando complementado, se torna 1. O resultado é que, para o primeiro byte, 0x00 torna-se 0x02.

Portanto, o identificador de interface IPv6 correspondente ao endereço Ethernet MAC de 00-60-08-52-F9-D8 é 02-60-08-FF-FE-52-F9-D8.

O endereço de vínculo local de um nó é a combinação do prefixo FE80::/64 e o identificador de interface de 64 bits expressos na notação hexadecimal de dois-pontos do IPv6. Portanto, o endereço de link local deste nó de exemplo com o prefixo FE80::/64 e o identificador de interface 02-60-08-FF-FE-52-F9-D8 é FE80:: 260:8FF: FE52: F9D8.

Você pode exibir seu endereço local do link usando IPv6 se, conforme demonstrado no exemplo a seguir:

**IPv6 se**

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

A interface 4 é uma interface correspondente a um adaptador Ethernet instalado com um endereço de link local de FE80:: 210:5AFF: FEAA: 20A2.

Para obter mais informações sobre o endereçamento IPv6 e uma visão geral dos conceitos do IPv6, consulte a introdução ao IPv6 white paper.

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Testando a conectividade entre dois hosts de link local

Você pode fazer um ping simples (uma troca de mensagens de resposta de eco e de solicitação de eco ICMPv6) usando o IPv6 entre dois hosts de link local.

**Para executar ping usando o IPv6 entre dois hosts de link local**

1.  Instale o Microsoft IPv6 Technology Preview para Windows em dois hosts do Windows (host A e host B) que estão no mesmo link (sub-rede).
2.  Use o IPv6 se estiver no host a para obter o endereço de vínculo local para a interface Ethernet.

    Exemplo: o endereço de link local do host A é FE80:: 210:5AFF: FEAA: 20A2.

3.  Use o IPv6 se estiver no host B para obter o endereço de link local para a interface Ethernet.

    Exemplo: o endereço de link local do host B é FE80:: 260:97FF: FE02:6EA5.

4.  No host A, execute ping no host B usando Ping6.exe.

    Exemplo: ping6 FE80:: 260:97FF: FE02:6EA5

Para especificar o endereço de origem do qual as mensagens de solicitação de eco são enviadas, você também pode usar a opção Ping6.exe-s. Por exemplo, para enviar solicitações de eco para o host B do endereço IPv6 de FE80:: 210:5AFF: FEAA: 20A2, use o seguinte comando:

**ping6-s FE80:: 210:5AFF: FEAA: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**

Ao executar ping de um endereço de link local ou site local, é recomendável especificar o Scope-ID para tornar o endereço de destino inambíguo. A notação para especificar o Scope-ID é o endereço% Scope-ID. Para endereços de vínculo local, o Scope-ID é igual ao número da interface, conforme exibido no comando IPv6 If. Para endereços de site local, o Scope-ID é igual ao número do site, conforme exibido no comando IPv6 If. Por exemplo, para enviar mensagens de solicitação de eco para o host B usando o escopo-ID 4, use o seguinte comando:

**ping6 FE80:: 260:97FF: FE02:6EA5% 4**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações recomendadas para IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



