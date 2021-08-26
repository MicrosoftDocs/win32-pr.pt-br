---
description: Os qualificadores contêm informações de contexto específicas da implementação e propriedades de transporte que definem como o Provedor SNMP acessa um agente SNMP. O exemplo a seguir lista os qualificadores exclusivos para o Provedor SNMP.
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
ms.openlocfilehash: 3b05e2d6994bd0bee1a1f0e30287169c23b69ef574ba47fab1f3d8b5db5abedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996086"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Qualificadores específicos para o provedor SNMP

Os qualificadores contêm informações de contexto específicas da implementação e propriedades de transporte que definem como o Provedor SNMP acessa um agente SNMP. O exemplo a seguir lista os qualificadores exclusivos para o Provedor SNMP.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Tipo de dados: **CIM \_ STRING**

Endereço de transporte associado ao agente SNMP, como um endereço IP ou um nome DNS. Você deve definir **AgentAddress** como um endereço de host unicast válido ou um nome de host de domínio que pode ser resolvido por meio do processo de resolução de nome de domínio do sistema operacional. **AgentAddress** não tem nenhum valor padrão.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Tipo de dados: **CIM \_ SINT32**

Número máximo de solicitações SNMP pendentes simultaneamente que podem ser enviadas a esse agente enquanto uma resposta ainda não foi recebida. Uma solicitação SNMP é considerada pendente até que uma resposta pdu tenha sido recebida ou tenha o tempo de vida. Um tamanho de janela grande geralmente melhora o desempenho, mas alguns agentes podem não funcionar bem sob uma carga pesada. **AgentFlowControlWindowSize** pode ser definido como 0 para indicar um tamanho de janela infinito ou um inteiro entre 1 e 2^32-1. O valor padrão é 10. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Tipo de dados: **CIM \_ STRING**

Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (Unidade de Dados de Protocolo SNMP) durante uma operação de leitura (solicitações SNMP GET/GET NEXT). O nome da comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos. O valor padrão é público. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Tipo de dados: **CIM \_ SINT32**

Número de vezes que uma única solicitação SNMP pode ser recuperada quando não há resposta do agente SNMP antes que a solicitação seja considerada com falha. **AgentRetryCount** deve ser definido como um inteiro entre 0 e 2^32-1. O valor padrão é 1. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Tipo de dados: **CIM \_ SINT32**

Tempo em milissegundos antes que a PDU (Unidade de Dados do Protocolo SNMP) seja considerada como sendo descartado. Esse é o número de milissegundos para aguardar uma resposta a uma solicitação SNMP enviada ao agente SNMP. **AgentRetryTimeout** deve ser definido como um inteiro entre 0 e 2^32-1. O valor padrão é 500. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Tipo de dados: **CIM \_ STRING**

Versão do protocolo SNMP a ser usada ao se comunicar com o agente SNMP. Atualmente, os únicos valores válidos são 1 (para SNMPv1) e 2C (para SNMPv2C). O valor padrão é 1. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Tipo de dados: **CIM \_ STRING**

Protocolo de transporte usado para se comunicar com o agente SNMP. Atualmente, os únicos valores válidos são IP (Internet Protocol) e IPX (Internet Packet Exchange). O valor padrão é IP. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Tipo de dados: **CIM \_ SINT32**

Número máximo de vinculações variáveis contidas em uma única PDU SNMP. Cada solicitação SNMP enviada ao agente SNMP contém uma ou mais variáveis SNMP. Esse parâmetro especifica o maior número de variáveis que podem ser incluídas em uma única solicitação. **AgentVarBindsPerPdu** pode ser definido como 0 (zero) para fazer com que a implementação determine as vinculações de variáveis ideais ou um inteiro entre 1 e 2^32-1. Observe que, ao aumentar esse valor pode melhorar o desempenho, alguns agentes e redes não podem lidar com a solicitação resultante. O valor padrão é 10. Esse qualificador é opcional.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Tipo de dados: **CIM \_ STRING**

Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (Unidade de Dados de Protocolo SNMP) durante uma operação de gravação (solicitação SET SNMP). O nome da comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos. O valor padrão é público. Esse qualificador é opcional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

 




