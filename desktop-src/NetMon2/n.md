---
description: Glossário de Monitor de Rede termos que começam com a letra N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881fb15f4432f6d2bb4b92025c28fc88c1862fa018e9e01df06c5ea8e79ced53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555786"
---
# <a name="n-network-monitor"></a>N (Monitor de Rede)

<dl> <dt>

<span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**Ndis**
</dt> <dd>

Confira Especificação da interface do driver de rede.

</dd> <dt>

<span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**NDIS (especificação de interface de driver de rede)**
</dt> <dd>

A especificação para a interface entre drivers de dispositivo e uma rede. Todos os transportes chamam a interface NDIS para acessar e trabalhar com cartões de interface de rede.

</dd> <dt>

<span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Monitor de Rede agente**
</dt> <dd>

Um Monitor de Rede componente. O agente permite que um computador remoto capture dados da rede. Quando uma Monitor de Rede se conecta remotamente ao agente Monitor de Rede e inicia uma captura, as estatísticas da captura são transferidas pela rede para o computador de gerenciamento. A transferência continua em intervalos especificados quando a conexão é feita.

</dd> <dt>

<span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**provedor de pacotes de rede (NPP)**
</dt> <dd>

O Monitor de Rede que coleta o tráfego de rede em quadros e, em seguida, passa os quadros para um especialista e para o aplicativo NPP. Um NPP usa o Nmnt.sys (driver do sistema) do Monitor de Rede para obter os quadros coletados da rede e fornece várias interfaces COM que passam os quadros para um aplicativo especialista, monitor e provedor de pacotes de rede (NPP), em que eles podem ser exibidos e analisados.

</dd> <dt>

<span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**Npp**
</dt> <dd>

Consulte provedor de pacotes de rede.

</dd> <dt>

<span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Aplicativo NPP**
</dt> <dd>

Um aplicativo que ignora a interface do usuário Monitor de Rede Monitor e a Ferramenta de Controle de Monitor e conecta-se diretamente ao NPP (provedor de pacotes de rede). Um aplicativo NPP pode se conectar ao componente NPP com qualquer uma das cinco interfaces COM do NPP.

</dd> <dt>

<span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**
</dt> <dd>

O Monitor de Rede que se comunica com NPPs.

</dd> </dl>

 

 



