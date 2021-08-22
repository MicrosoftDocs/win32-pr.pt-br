---
title: Implementando filtros de firewall para Teredo
description: Windows permite que os aplicativos devam definir uma opção de soquete que permite que os aplicativos indiquem uma intenção explícita de receber o tráfego Teredo enviado ao firewall do host por meio da Windows Filtering Platform.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001801"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Implementando filtros de firewall para Teredo

Windows permite que os aplicativos devam definir uma opção de soquete que permite que os aplicativos indiquem uma intenção explícita de receber o tráfego Teredo enviado ao firewall do host por meio da Windows Filtering Platform. No Windows, uma opção de soquete para definir um nível de proteção é usada para permitir que um aplicativo defina o tipo de tráfego que está disposto a receber. Mais especificamente, em cenários que envolvem o tráfego Teredo, a [opção de soquete NÍVEL de \_ PROTEÇÃO \_ IPV6](/windows/desktop/WinSock/ipv6-protection-level) é especificada. É recomendável que as implementações de firewall de host mantenham os seguintes filtros para permitir seletivamente o tráfego Teredo para um aplicativo, enquanto bloqueiam o tráfego por padrão para qualquer aplicativo sem uma isenção.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Filtro de bloco padrão para tráfego de borda percorrido

Um firewall de host sempre deve manter um filtro de bloco padrão dentro da camada de filtragem RECV ACCEPT V6 de ALE AUTH para o tráfego que corresponde às condições de Teredo do tipo de interface Tunnel e \_ \_ \_ \_  **Tunnel** especificadas. Quando implementado, esse filtro indica a presença de um firewall de host com conhecimento de travessia de borda no sistema. Esse filtro é exibido como um contrato de API entre o firewall do host e Windows. Por padrão, esse filtro bloqueará o tráfego de borda percorrido para qualquer aplicativo.

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> As classes 'Delivery', 'Arrival' e 'Next Hop' de condições de interface são usadas para controlar um modelo de host fraco e o encaminhamento de pacotes entre interfaces. O exemplo acima utiliza a classe 'Delivery'. Revise [As Condições de Filtragem Disponíveis](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) em Cada Camada de Filtragem na documentação do SDK do WFP, pois seu design de segurança deve levar cada caso em consideração.

 

## <a name="allow-filter-for-exempt-applications"></a>Permitir filtro para aplicativos isentos

Se um aplicativo estiver isento de receber tráfego Teredo em um soquete de escuta, um filtro de permissão deverá ser implementado dentro da camada de filtragem ALE \_ AUTH \_ RCV ACCEPT V6 no \_ firewall do \_ host. É importante observar que, dependendo de como a isenção é configurada pelo usuário ou aplicativo, o firewall do host pode incluir uma opção de soquete.

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a>Filtro de saída de chamada de doiancy

O serviço Teredo no Windows implementa um modelo de doncy. A qualquer momento, se nenhum aplicativo estiver escutando em um soquete UDP ou TCP com a travessia de borda habilitada, o serviço passará para um estado inativo. Para que o mecanismo de doiancy funcione, o firewall do host deve manter um filtro de texto explicado para cada aplicativo isento especificado na camada de filtragem ALE AUTH LISTEN V6 para TCP e a camada de filtragem ALE RESOURCE ASSIGNMENT V6 para aplicativos baseados em \_ \_ \_ \_ \_ \_ UDP. O exemplo a seguir demonstra um texto explicado para um **aplicativo TCP.**

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 