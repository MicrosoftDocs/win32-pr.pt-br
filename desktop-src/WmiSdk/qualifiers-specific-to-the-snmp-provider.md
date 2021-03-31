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
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="163b6-104">Qualificadores específicos para o provedor SNMP</span><span class="sxs-lookup"><span data-stu-id="163b6-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="163b6-105">Os qualificadores contêm informações de contexto específicas de implementação e propriedades de transporte que definem como o provedor SNMP acessa um agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="163b6-106">O a seguir lista os qualificadores exclusivos para o provedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="163b6-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="163b6-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-108">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="163b6-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="163b6-109">Endereço de transporte associado ao agente SNMP, como um endereço IP ou nome DNS.</span><span class="sxs-lookup"><span data-stu-id="163b6-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="163b6-110">Você deve definir **AgentAddress** como um endereço de host unicast válido ou um nome de host de domínio que possa ser resolvido por meio do processo de resolução de nome de domínio do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="163b6-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="163b6-111">**AgentAddress** não tem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="163b6-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span><span class="sxs-lookup"><span data-stu-id="163b6-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-113">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="163b6-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="163b6-114">Número máximo de solicitações SNMP pendentes simultâneas que podem ser enviadas a este agente, enquanto uma resposta ainda não foi recebida.</span><span class="sxs-lookup"><span data-stu-id="163b6-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="163b6-115">Uma solicitação SNMP é considerada pendente até que uma resposta de PDU tenha sido recebida ou tenha atingido o tempo limite. Um tamanho de janela grande geralmente melhora o desempenho, mas alguns agentes podem não funcionar bem em uma carga pesada.</span><span class="sxs-lookup"><span data-stu-id="163b6-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="163b6-116">**AgentFlowControlWindowSize** pode ser definido como 0 para indicar um tamanho de janela infinito ou um inteiro entre 1 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="163b6-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="163b6-117">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="163b6-117">The default value is 10.</span></span> <span data-ttu-id="163b6-118">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span><span class="sxs-lookup"><span data-stu-id="163b6-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-120">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="163b6-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="163b6-121">Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (unidade de dados de protocolo SNMP) durante uma operação de leitura (SNMP GET/obter próximas solicitações).</span><span class="sxs-lookup"><span data-stu-id="163b6-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="163b6-122">O nome da Comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="163b6-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="163b6-123">O valor padrão é público.</span><span class="sxs-lookup"><span data-stu-id="163b6-123">The default value is public.</span></span> <span data-ttu-id="163b6-124">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span><span class="sxs-lookup"><span data-stu-id="163b6-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-126">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="163b6-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="163b6-127">Número de vezes que uma única solicitação SNMP pode ser repetida quando não há resposta do agente SNMP antes que a solicitação seja considerada como falha.</span><span class="sxs-lookup"><span data-stu-id="163b6-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="163b6-128">**AgentRetryCount** deve ser definido como um inteiro entre 0 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="163b6-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="163b6-129">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="163b6-129">The default value is 1.</span></span> <span data-ttu-id="163b6-130">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="163b6-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-132">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="163b6-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="163b6-133">Tempo em milissegundos antes que a PDU (unidade de dados) do protocolo SNMP seja considerada descartada.</span><span class="sxs-lookup"><span data-stu-id="163b6-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="163b6-134">Este é o número de milissegundos para aguardar uma resposta a uma solicitação SNMP enviada ao agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="163b6-135">**AgentRetryTimeout** deve ser definido como um inteiro entre 0 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="163b6-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="163b6-136">O valor padrão é 500.</span><span class="sxs-lookup"><span data-stu-id="163b6-136">The default value is 500.</span></span> <span data-ttu-id="163b6-137">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span><span class="sxs-lookup"><span data-stu-id="163b6-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-139">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="163b6-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="163b6-140">Versão do protocolo SNMP a ser usada ao se comunicar com o agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="163b6-141">Atualmente, os únicos valores válidos são 1 (para SNMPv1) e 2C (para SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="163b6-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="163b6-142">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="163b6-142">The default value is 1.</span></span> <span data-ttu-id="163b6-143">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="163b6-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-145">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="163b6-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="163b6-146">Protocolo de transporte usado para se comunicar com o agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="163b6-147">Atualmente, os únicos valores válidos são IP (Internet Protocol) e Internet Packet Exchange (IPX).</span><span class="sxs-lookup"><span data-stu-id="163b6-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="163b6-148">O valor padrão é IP.</span><span class="sxs-lookup"><span data-stu-id="163b6-148">The default value is IP.</span></span> <span data-ttu-id="163b6-149">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span><span class="sxs-lookup"><span data-stu-id="163b6-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-151">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="163b6-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="163b6-152">Número máximo de associações de variáveis contidas em um único PDU de SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="163b6-153">Cada solicitação SNMP enviada ao agente SNMP contém uma ou mais variáveis SNMP.</span><span class="sxs-lookup"><span data-stu-id="163b6-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="163b6-154">Esse parâmetro especifica o maior número de variáveis que podem ser incluídas em uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="163b6-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="163b6-155">**AgentVarBindsPerPdu** pode ser definido como 0 (zero) para fazer com que a implementação determine as associações de variável ideais ou um número inteiro entre 1 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="163b6-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="163b6-156">Observe que, embora o aumento desse valor possa melhorar o desempenho, alguns agentes e redes não podem lidar com a solicitação resultante.</span><span class="sxs-lookup"><span data-stu-id="163b6-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="163b6-157">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="163b6-157">The default value is 10.</span></span> <span data-ttu-id="163b6-158">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="163b6-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span><span class="sxs-lookup"><span data-stu-id="163b6-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="163b6-160">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="163b6-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="163b6-161">Cadeia de caracteres de octeto de comprimento variável usada pelo agente SNMP para autenticar uma PDU (unidade de dados de protocolo SNMP) durante uma operação de gravação (solicitação de definição de SNMP).</span><span class="sxs-lookup"><span data-stu-id="163b6-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="163b6-162">O nome da Comunidade deve ser mapeado para uma cadeia de caracteres Unicode e é limitado a caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="163b6-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="163b6-163">O valor padrão é público.</span><span class="sxs-lookup"><span data-stu-id="163b6-163">The default value is public.</span></span> <span data-ttu-id="163b6-164">Esse qualificador é opcional.</span><span class="sxs-lookup"><span data-stu-id="163b6-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="163b6-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="163b6-165">Requirements</span></span>



| <span data-ttu-id="163b6-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="163b6-166">Requirement</span></span> | <span data-ttu-id="163b6-167">Valor</span><span class="sxs-lookup"><span data-stu-id="163b6-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="163b6-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="163b6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="163b6-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="163b6-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="163b6-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="163b6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="163b6-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="163b6-171">Windows Server 2008</span></span><br/> |



 

 




