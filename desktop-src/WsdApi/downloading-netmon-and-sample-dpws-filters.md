---
description: O Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Baixando os filtros de DPWS e de exemplo do Netmon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788951"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Baixando os filtros de DPWS e de exemplo do Netmon

O Monitor de Rede da Microsoft 3 (Netmon) é um analisador de pacotes usado para inspecionar o tráfego de rede. O Netmon deve ser baixado antes das etapas de solução de problemas fornecidas na [inspeção de rastreamentos de rede para a descoberta de UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e [inspeção de rastreamentos de rede para que o intercâmbio de metadados http](inspecting-network-traces-for-http-metadata-exchange.md) possa ser seguido. Após o download do Netmon, os filtros DPWS podem ser usados para ajudar a isolar o tráfego de interesse.

## <a name="downloading-netmon"></a>Baixando o Netmon

Para baixar o Netmon, vá para [Monitor de rede da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e siga as instruções. Para obter mais informações sobre o Netmon, consulte "informações sobre o Monitor de Rede 3,0" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Filtros de DPWS de exemplo

Às vezes, a solução de problemas de WS-Discovery e troca de metadados deve ocorrer em uma rede ocupada. Os filtros de exemplo podem ser usados para ajudar a limitar a saída do Netmon ao tráfego de interesse. Para obter mais informações sobre como usar filtros do Netmon, consulte [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

O exemplo a seguir mostra um filtro que limita a saída a todos os WS-Discovery tráfego de difusão.

> [!Note]  
> Esse filtro não captura o tráfego de pilhas que não respondem a mensagens WS-Discovery multicast que se originam na porta 3702. Se tal pilha estiver sendo usada, esse filtro de exemplo deverá ser modificado antes do uso.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

O exemplo a seguir mostra um filtro que limita a saída para mensagens HTTP enviadas a pilhas WSDAPI na porta padrão.

> [!Note]  
> Os serviços podem enviar mensagens HTTP relevantes de portas diferentes de 5357. Se o tráfego de outras portas for interessante, esse filtro de exemplo deverá ser modificado antes do uso.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

O exemplo a seguir mostra um filtro que limita a saída ao tráfego de multicast IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

O exemplo a seguir mostra um filtro que limita a saída para o tráfego de multicast IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Alguns filtros podem ser combinados para limitar os resultados. O exemplo a seguir mostra um filtro que limita a saída para o tráfego de WS-Discovery multicast IPv4.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Quando esses filtros são usados, o tráfego relevante pode ser excluído dos resultados do Netmon. A exclusão pode ocorrer quando os serviços residem em portas diferentes das portas padrão (5357/5358) e quando uma pilha DPWS não responde às mensagens que usam a porta padrão. Nesses casos, os filtros devem ser modificados antes do uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



