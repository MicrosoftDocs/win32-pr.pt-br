---
description: O monitoramento e o controle do status do agente ad nas estações têm suporte por meio dessas funções lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState e lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Monitoramento e controle do AD Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52d3cf9387819bada069920099b19da65e6a1e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011447"
---
# <a name="acd-agent-monitoring-and-control"></a>Monitoramento e controle do AD Agent

O monitoramento e o controle do status do agente ad nas estações têm suporte por meio dessas funções: [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)e [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

A [**mensagem \_ AGENTSTATUS de linha**](line-agentstatus.md) é usada para indicar quando as informações do agente foram alteradas.

Esses controles são associados a um endereço em vez de uma linha porque muitos sistemas ad são implementados com diferentes filas do AD associadas a botões no terminal do telefone (e aparências de chamada separadas). Além disso, os telefones ad Agent geralmente podem ter aparências de chamada separadas para chamadas pessoais.

Em termos de arquitetura, a funcionalidade ad deve ser implementada em um aplicativo baseado em servidor. As funções de cliente mencionadas acima, em vez de mapear para o provedor de serviços de telefonia, são transmitidas a um aplicativo de servidor que tenha sido registrado (usando uma opção de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) como um manipulador para essas funções. A mensagem de [**linha \_ PROXYREQUEST**](line-proxyrequest.md) é usada para sinalizar para o aplicativo de manipulador quando uma solicitação é feita; ela chama a função [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para retornar resultados e dados. Os aplicativos de manipulador também podem chamar [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) para gerar mensagens de AGENTSTATUS de linha \_ quando necessário. No caso de um PBX herdado ou ad autônomo que implementa a funcionalidade de AD em si, o provedor de serviços de telefonia para o comutador deve incluir um aplicativo de servidor proxy que aceita as solicitações e as roteia (possivelmente usando as funções [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) ou uma interface privada) para o provedor de serviços, que os roteia para o comutador.

 

 



