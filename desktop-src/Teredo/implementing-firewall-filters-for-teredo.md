---
title: Implementando filtros de firewall para Teredo
description: O Windows permite que os aplicativos definam uma opção de soquete que permite que os aplicativos indiquem uma intenção explícita de receber o tráfego Teredo enviado ao firewall do host por meio da plataforma de filtragem do Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641538"
---
# <a name="implementing-firewall-filters-for-teredo"></a><span data-ttu-id="e9017-103">Implementando filtros de firewall para Teredo</span><span class="sxs-lookup"><span data-stu-id="e9017-103">Implementing Firewall Filters for Teredo</span></span>

<span data-ttu-id="e9017-104">O Windows permite que os aplicativos definam uma opção de soquete que permite que os aplicativos indiquem uma intenção explícita de receber o tráfego Teredo enviado ao firewall do host por meio da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="e9017-104">Windows allows applications to set a socket option that allows applications to indicate an explicit intent to receive Teredo traffic sent to the host firewall via the Windows Filtering Platform.</span></span> <span data-ttu-id="e9017-105">No Windows, uma opção de soquete para definir um nível de proteção é usada para permitir que um aplicativo defina o tipo de tráfego que ele está disposto a receber.</span><span class="sxs-lookup"><span data-stu-id="e9017-105">In Windows, a socket option for setting a protection level is used to allow an application to define what type of traffic it is willing to receive.</span></span> <span data-ttu-id="e9017-106">Mais especificamente, em cenários que envolvem o tráfego de Teredo, a opção de soquete de [ \_ \_ nível de proteção IPv6](/windows/desktop/WinSock/ipv6-protection-level) é especificada.</span><span class="sxs-lookup"><span data-stu-id="e9017-106">More specifically, in scenarios involving Teredo traffic, the [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option is specified.</span></span> <span data-ttu-id="e9017-107">É recomendável que as implementações de firewall do host mantenham os filtros a seguir para permitir seletivamente o tráfego Teredo para um aplicativo, ao mesmo tempo que bloqueia o tráfego por padrão para qualquer aplicativo sem isenção.</span><span class="sxs-lookup"><span data-stu-id="e9017-107">It is recommended that host firewall implementations maintain the following filters to selectively allow Teredo traffic for an application, while blocking traffic by default for any application without an exemption.</span></span>

## <a name="default-block-filter-for-edge-traversed-traffic"></a><span data-ttu-id="e9017-108">Filtro de bloco padrão para tráfego de borda atravessado</span><span class="sxs-lookup"><span data-stu-id="e9017-108">Default Block Filter for Edge Traversed Traffic</span></span>

<span data-ttu-id="e9017-109">Um firewall de host sempre deve manter um filtro de bloqueio padrão dentro \_ da \_ camada de \_ filtragem V6 de aceitação de autenticação \_ de Ale para tráfego correspondente ao **túnel de tipo de interface** especificado e às condições de Teredo do tipo de **túnel** .</span><span class="sxs-lookup"><span data-stu-id="e9017-109">A host firewall must always maintain a default block filter within the ALE\_AUTH\_RECV\_ACCEPT\_V6 filtering layer for traffic matching the specified **Interface Type Tunnel** and **Tunnel Type Teredo** conditions.</span></span> <span data-ttu-id="e9017-110">Quando implementada, esse filtro indica a presença de um firewall de host com reconhecimento de borda no sistema.</span><span class="sxs-lookup"><span data-stu-id="e9017-110">When implemented, this filter indicates the presence of an edge traversal aware host firewall in the system.</span></span> <span data-ttu-id="e9017-111">Esse filtro é exibido como um contrato de API entre o Firewall do host e o Windows.</span><span class="sxs-lookup"><span data-stu-id="e9017-111">This filter is viewed as an API contract between the host firewall and Windows.</span></span> <span data-ttu-id="e9017-112">Por padrão, esse filtro bloqueará o tráfego de borda atravessado para qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9017-112">By default, this filter will block edge traversed traffic to any application.</span></span>

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
> <span data-ttu-id="e9017-113">As classes ' Delivery ', ' chegada ' e ' próximo salto ' de condições de interface são usadas para controlar um modelo de host fraco e encaminhamento de pacotes entre interfaces.</span><span class="sxs-lookup"><span data-stu-id="e9017-113">The 'Delivery', 'Arrival', and 'Next Hop' classes of interface conditions are used to control a weak-host model and packet forwarding across interfaces.</span></span> <span data-ttu-id="e9017-114">O exemplo acima utiliza a classe ' Delivery '.</span><span class="sxs-lookup"><span data-stu-id="e9017-114">The example above utilizes the 'Delivery' class.</span></span> <span data-ttu-id="e9017-115">Examine as [condições de filtragem disponíveis em cada camada de filtragem](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) na documentação do SDK do WFP, já que seu design de segurança deve levar cada caso em consideração.</span><span class="sxs-lookup"><span data-stu-id="e9017-115">Please review [Filtering Conditions Available at Each Filtering Layer](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in the WFP SDK documentation, as your security design must take each case into consideration.</span></span>

 

## <a name="allow-filter-for-exempt-applications"></a><span data-ttu-id="e9017-116">Permitir filtro para aplicativos isentos</span><span class="sxs-lookup"><span data-stu-id="e9017-116">Allow Filter for Exempt Applications</span></span>

<span data-ttu-id="e9017-117">Se um aplicativo estiver isento de receber tráfego Teredo em um soquete de escuta, um filtro de permissão deverá ser implementado dentro da \_ camada de filtragem de autenticação Ale \_ RCV \_ Accept \_ V6 no firewall do host.</span><span class="sxs-lookup"><span data-stu-id="e9017-117">If an application is exempt from receiving Teredo traffic on a listening socket, a permit filter must be implemented within the ALE\_AUTH\_RCV\_ACCEPT\_V6 filtering layer on the host firewall.</span></span> <span data-ttu-id="e9017-118">É importante observar que, dependendo de como a isenção é configurada pelo usuário ou aplicativo, o Firewall do host pode incluir uma opção de soquete.</span><span class="sxs-lookup"><span data-stu-id="e9017-118">It is important to note that depending on how the exemption is configured by the user or application, the host firewall can include a socket option.</span></span>

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

## <a name="dormancy-callout-filter"></a><span data-ttu-id="e9017-119">Filtro de texto explicativo dormência</span><span class="sxs-lookup"><span data-stu-id="e9017-119">Dormancy Callout Filter</span></span>

<span data-ttu-id="e9017-120">O serviço Teredo no Windows implementa um modelo dormência.</span><span class="sxs-lookup"><span data-stu-id="e9017-120">The Teredo service in Windows implements a dormancy model.</span></span> <span data-ttu-id="e9017-121">A qualquer momento, se nenhum aplicativo estiver escutando em um soquete UDP ou TCP com percurso de borda habilitado, o serviço passará para um estado inativo.</span><span class="sxs-lookup"><span data-stu-id="e9017-121">At any given time, if no applications are listening on a UDP or TCP socket with edge traversal enabled, the service moves to a dormant state.</span></span> <span data-ttu-id="e9017-122">Para que o mecanismo dormência funcione, o Firewall do host deve manter um filtro de texto explicativo para cada aplicativo isento especificado na \_ \_ camada de \_ filtragem V6 de escuta de autenticação Ale para TCP e \_ \_ \_ camada de filtragem V6 de atribuição de recursos Ale para aplicativos baseados em UDP.</span><span class="sxs-lookup"><span data-stu-id="e9017-122">For the dormancy mechanism to work, the host firewall must maintain a callout filter for each exempt application specified within the ALE\_AUTH\_LISTEN\_V6 filtering layer for TCP, and ALE\_RESOURCE\_ASSIGNMENT\_V6 filtering layer for UDP based applications.</span></span> <span data-ttu-id="e9017-123">O exemplo a seguir demonstra um texto explicativo dormência para um aplicativo **TCP** .</span><span class="sxs-lookup"><span data-stu-id="e9017-123">The following sample below demonstrates a dormancy callout for a **TCP** application.</span></span>

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

 

 