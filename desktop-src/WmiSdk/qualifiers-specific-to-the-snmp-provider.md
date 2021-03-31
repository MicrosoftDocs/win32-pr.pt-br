---
description: Os qualificadores contêm informações de contexto específicas de implementação e propriedades de transporte que definem como o provedor SNMP acessa um agente SNMP. O a seguir lista os qualificadores exclusivos para o provedor SNMP.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Qualificadores específicos para o provedor SNMP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647693"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Qualificadores específicos para o provedor SNMP

Os qualificadores contêm informações de contexto específicas de implementação e propriedades de transporte que definem como o provedor SNMP acessa um agente SNMP. O a seguir lista os qualificadores exclusivos para o provedor SNMP.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Endereço de transporte associado ao agente SNMP, como um endereço IP ou nome DNS. Você deve definir **AgentAddress** como um endereço de host unicast válido ou um nome de host de domínio que possa ser resolvido por meio do processo de resolução de nome de domínio do sistema operacional. **AgentAddress** não tem valor padrão.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Número máximo de solicitações SNMP pendentes simultâneas que podem ser enviadas a este agente, enquanto uma resposta ainda não foi recebida. Uma solicitação SNMP é considerada pendente até que uma resposta de PDU tenha sido recebida ou tenha atingido o tempo limite. Um tamanho de janela grande geralmente melhora o desempenho, mas alguns agentes podem não funcionar bem em uma carga pesada. **AgentFlowControlWindowSize** pode ser definido como 0 para indicar um tamanho de janela infinito ou um inteiro entre 1 e 2 ^ 32-1. O valor padrão é 10. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (unidade de dados de protocolo SNMP) durante uma operação de leitura (SNMP GET/obter próximas solicitações). O nome da Comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos. O valor padrão é público. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Número de vezes que uma única solicitação SNMP pode ser repetida quando não há resposta do agente SNMP antes que a solicitação seja considerada como falha. **AgentRetryCount** deve ser definido como um inteiro entre 0 e 2 ^ 32-1. O valor padrão é 1. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Tempo em milissegundos antes que a PDU (unidade de dados) do protocolo SNMP seja considerada descartada. Este é o número de milissegundos para aguardar uma resposta a uma solicitação SNMP enviada ao agente SNMP. **AgentRetryTimeout** deve ser definido como um inteiro entre 0 e 2 ^ 32-1. O valor padrão é 500. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Versão do protocolo SNMP a ser usada ao se comunicar com o agente SNMP. Atualmente, os únicos valores válidos são 1 (para SNMPv1) e 2C (para SNMPv2C). O valor padrão é 1. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Protocolo de transporte usado para se comunicar com o agente SNMP. Atualmente, os únicos valores válidos são IP (Internet Protocol) e Internet Packet Exchange (IPX). O valor padrão é IP. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Número máximo de associações de variáveis contidas em um único PDU de SNMP. Cada solicitação SNMP enviada ao agente SNMP contém uma ou mais variáveis SNMP. Esse parâmetro especifica o maior número de variáveis que podem ser incluídas em uma única solicitação. **AgentVarBindsPerPdu** pode ser definido como 0 (zero) para fazer com que a implementação determine as associações de variável ideais ou um número inteiro entre 1 e 2 ^ 32-1. Observe que, embora o aumento desse valor possa melhorar o desempenho, alguns agentes e redes não podem lidar com a solicitação resultante. O valor padrão é 10. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (unidade de dados de protocolo SNMP) durante uma operação de gravação (solicitação de definição de SNMP). O nome da Comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos. O valor padrão é público. Esse qualificador é opcional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

 




