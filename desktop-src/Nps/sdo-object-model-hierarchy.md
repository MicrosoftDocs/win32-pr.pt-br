---
title: Hierarquia do modelo de objeto
description: Os objetos no modelo de objeto SDO são organizados em uma hierarquia. Isso significa que os objetos no SDO fornecem acesso a outros objetos no SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f63b5692571bab49580251d6ef879adde8ae9a57af4c541404aabc48538e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063328"
---
# <a name="object-model-hierarchy"></a>Hierarquia do modelo de objeto

Os objetos no modelo de objeto SDO são organizados em uma hierarquia. Isso significa que os objetos no SDO fornecem acesso a outros objetos no SDO.

Os objetos fornecem acesso a outros objetos de duas maneiras. Uma maneira é que o objeto exponha uma interface que fornece métodos para recuperar outros objetos. Um exemplo dessa abordagem é o objeto Machine. O objeto Machine expõe a interface [**ISdoMachine.**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) O [**método ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera um objeto Service. O [**método ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera um Objeto de Usuário.

![machine object expondo a interface isdomachine](images/sdo01.png)

Para obter mais informações, consulte [Obtendo SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos)de serviço e usuário.

A segunda maneira como os objetos fornecem acesso a outros objetos é que uma coleção de objetos é representada como uma propriedade do objeto que a contém. Para recuperar uma coleção de objetos, chame [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) na propriedade de um objeto que representa a coleção. Por exemplo, para recuperar a coleção Políticas, chame **ISdo::GetProperty** na interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) exposta pelo objeto NPS.

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008.

 

![recuperando a coleção de políticas](images/sdo02.png)

Para obter o código de exemplo que recupera a coleção Políticas, consulte [Recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection).

O [**Objeto de Dados do Servidor NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) tem as seguintes propriedades que representam coleções:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Contas
</dt> <dd>

O único auditor na coleção Auditores é o Log [**de Eventos do NT.**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties)

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Políticas
</dt> <dd>

Cada [**objeto de política**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) tem uma propriedade que representa uma coleção de condições.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Perfis
</dt> <dd>

Cada [**objeto de perfil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) nas coleções perfis tem uma propriedade que representa uma coleção de atributos. Consulte [Atributos com suporte para SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) para ver uma lista dos atributos com suporte do SDO.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolos
</dt> <dd>

A coleção de protocolos contém o objeto de protocolo RADIUS, que contém uma coleção de clientes que representa clientes RADIUS. Consulte [Adicionando um cliente](/windows/desktop/Nps/sdo-adding-a-client) para obter um código de exemplo que mostra como recuperar a coleção de clientes.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Políticas de proxy
</dt> <dd>

Esta coleção contém políticas de acesso à rede usadas para processamento de solicitação de conexão.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Perfis de proxy
</dt> <dd>

Esta coleção contém perfis usados para processamento de solicitação de conexão.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Grupos de Servidores RADIUS
</dt> <dd>

Cada [**grupo de servidores RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) na coleção Grupos de Servidores RADIUS tem uma propriedade que representa a coleção de servidores nesse grupo de servidores.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Manipuladores de solicitação
</dt> <dd>

Esta coleção contém a coleção "Avaliador de Realms da Microsoft". As configurações "Autenticação SAM do Microsoft NT" e "Contabilidade da Microsoft" também estão disponíveis nesta coleção.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades e objetos SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Atributos com suporte para SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 