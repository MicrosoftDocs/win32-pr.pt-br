---
description: Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Baixando o Netmon e exemplos de filtros DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030216"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Baixando o Netmon e exemplos de filtros DPWS

Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede. O Netmon deve ser baixado antes que as etapas de solução de problemas fornecidas em Inspecionando rastreamentos de rede para descoberta de [WS UDP](inspecting-network-traces-for-udp-ws-discovery.md) e Inspecionando rastreamentos de rede para metadados [HTTP Exchange](inspecting-network-traces-for-http-metadata-exchange.md) possam ser seguidas. Depois que o Netmon tiver sido baixado, os filtros DPWS poderão ser usados para ajudar a isolar o tráfego de interesse.

## <a name="downloading-netmon"></a>Baixando o Netmon

Para baixar o Netmon, acesse [Monitor de Rede da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e siga as instruções. Para obter mais informações sobre o Netmon, consulte "Informações sobre Monitor de Rede 3.0" na Base de Dados de Conhecimento de Ajuda e Suporte em [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Exemplo de filtros DPWS

Às vezes, WS-Discovery solução de problemas de troca de metadados e deve ocorrer em uma rede ocupada. Os filtros de exemplo podem ser usados para ajudar a limitar a saída netmon ao tráfego de interesse. Para obter mais informações sobre como usar filtros Netmon, consulte [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

O exemplo a seguir mostra um filtro que limita a saída a todos os tráfegos WS-Discovery difusão.

> [!Note]  
> Esse filtro não captura o tráfego de pilhas que não respondem a mensagens WS-Discovery multicast originadas na porta 3702. Se essa pilha estiver sendo usada, esse filtro de exemplo deverá ser modificado antes do uso.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

O exemplo a seguir mostra um filtro que limita a saída a mensagens HTTP enviadas para pilhas WSDAPI na porta padrão.

> [!Note]  
> Os serviços podem enviar mensagens HTTP relevantes de portas diferentes da 5357. Se o tráfego de outras portas for de interesse, esse filtro de exemplo deverá ser modificado antes do uso.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

O exemplo a seguir mostra um filtro que limita a saída ao tráfego multicast IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

O exemplo a seguir mostra um filtro que limita a saída ao tráfego multicast IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Alguns filtros podem ser combinados para limitar ainda mais os resultados. O exemplo a seguir mostra um filtro que limita a saída ao tráfego de WS-Discovery multicast IPv4.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Quando esses filtros são usados, o tráfego relevante pode ser excluído dos resultados do Netmon. A exclusão pode ocorrer quando os serviços residem em portas diferentes das portas padrão (5357/5358) e quando uma pilha DPWS não responde a mensagens usando a porta padrão. Nesses casos, os filtros devem ser modificados antes do uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



