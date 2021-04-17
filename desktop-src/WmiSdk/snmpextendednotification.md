---
description: A classe SnmpExtendedNotification é a classe base para qualquer classe mapeada da macro do tipo de notificação para uma classe CIM pelo provedor SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Classe SnmpExtendedNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798482"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="3904d-103">Classe SnmpExtendedNotification</span><span class="sxs-lookup"><span data-stu-id="3904d-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="3904d-104">A classe **SnmpExtendedNotification** é a classe base para qualquer classe mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM pelo [provedor SNMP](snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3904d-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="3904d-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3904d-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="3904d-106">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3904d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3904d-107">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="3904d-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3904d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3904d-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="3904d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3904d-109">Members</span></span>

<span data-ttu-id="3904d-110">A classe **SnmpExtendedNotification** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3904d-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="3904d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3904d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3904d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3904d-112">Properties</span></span>

<span data-ttu-id="3904d-113">A classe **SnmpExtendedNotification** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3904d-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3904d-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="3904d-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-117">Endereço de rede da entidade que criou a notificação.</span><span class="sxs-lookup"><span data-stu-id="3904d-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="3904d-118">Esse é o endereço real do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3904d-118">This is the actual address of the device.</span></span> <span data-ttu-id="3904d-119">Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="3904d-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="3904d-120">Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte é definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3904d-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="3904d-121">Esta propriedade é válida somente para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="3904d-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-122">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="3904d-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-125">Protocolo de transporte usado pela entidade de envio.</span><span class="sxs-lookup"><span data-stu-id="3904d-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="3904d-126">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3904d-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-127">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="3904d-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-130">Endereço de rede da entidade que enviou a notificação.</span><span class="sxs-lookup"><span data-stu-id="3904d-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="3904d-131">Este é o endereço da última entidade que encaminhou a notificação.</span><span class="sxs-lookup"><span data-stu-id="3904d-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="3904d-132">Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="3904d-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="3904d-133">Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte se refere a um Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="3904d-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="3904d-134">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3904d-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-135">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="3904d-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-138">O protocolo de transporte usado pela entidade de envio.</span><span class="sxs-lookup"><span data-stu-id="3904d-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-139">**Comunidade**</span><span class="sxs-lookup"><span data-stu-id="3904d-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-142">Nome da Comunidade associado a uma instância do PDU.</span><span class="sxs-lookup"><span data-stu-id="3904d-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="3904d-143">O nome da Comunidade autentica o originador da PDU.</span><span class="sxs-lookup"><span data-stu-id="3904d-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="3904d-144">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3904d-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-145">**Identificação**</span><span class="sxs-lookup"><span data-stu-id="3904d-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3904d-148">Qualificadores: **\_ Convenção de texto** ("objectidentifier"), **codificação** ("objectidentifier") **, \_ sintaxe de objeto** ("objectidentifier"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="3904d-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="3904d-149">Identificação autoritativa desta notificação.</span><span class="sxs-lookup"><span data-stu-id="3904d-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="3904d-150">Mapeia diretamente para a associação de variável SnmpTrapOID de entrada MIB.</span><span class="sxs-lookup"><span data-stu-id="3904d-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="3904d-151">Esta propriedade é válida somente para o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3904d-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="3904d-152">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="3904d-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-153">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="3904d-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3904d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-155">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="3904d-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="3904d-156">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3904d-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="3904d-157">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3904d-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3904d-158">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="3904d-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-159">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3904d-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3904d-161">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="3904d-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="3904d-162">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="3904d-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="3904d-163">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="3904d-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="3904d-164">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3904d-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="3904d-165">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3904d-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3904d-166">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="3904d-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3904d-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3904d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3904d-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3904d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3904d-169">Qualificadores: **\_ Convenção de texto** ("timetiques"), **codificação** ("timetiques") **, \_ sintaxe de objeto** ("timetiques"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="3904d-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="3904d-170">Tempo em centésimos de um segundo desde que a parte de gerenciamento de rede do agente foi reinicializada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="3904d-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="3904d-171">Isso é mapeado para a variável MIB sysUptime. 0, que é do tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="3904d-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="3904d-172">Essa propriedade é mapeada para o carimbo de **data/hora** da propriedade de classe CIM, que é do tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="3904d-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="3904d-173">Esta propriedade é válida somente para o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3904d-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3904d-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="3904d-174">Remarks</span></span>

<span data-ttu-id="3904d-175">Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **timestamp** ou **Identification** causa um conflito de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="3904d-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="3904d-176">Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.</span><span class="sxs-lookup"><span data-stu-id="3904d-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="3904d-177">Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **Community** causa um conflito de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="3904d-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="3904d-178">Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.</span><span class="sxs-lookup"><span data-stu-id="3904d-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3904d-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3904d-179">Requirements</span></span>



| <span data-ttu-id="3904d-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="3904d-180">Requirement</span></span> | <span data-ttu-id="3904d-181">Valor</span><span class="sxs-lookup"><span data-stu-id="3904d-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3904d-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3904d-182">Minimum supported client</span></span><br/> | <span data-ttu-id="3904d-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3904d-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3904d-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3904d-184">Minimum supported server</span></span><br/> | <span data-ttu-id="3904d-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3904d-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3904d-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="3904d-186">Namespace</span></span><br/>                | <span data-ttu-id="3904d-187">Raiz \\ SNMP \\ Smir</span><span class="sxs-lookup"><span data-stu-id="3904d-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="3904d-188">MOF</span><span class="sxs-lookup"><span data-stu-id="3904d-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3904d-189"><dt>SnmpSmiR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3904d-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3904d-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="3904d-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3904d-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="3904d-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="3904d-192">Macro do tipo de notificação</span><span class="sxs-lookup"><span data-stu-id="3904d-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

