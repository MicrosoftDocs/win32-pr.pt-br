---
description: A classe SnmpNotification é mapeada da macro do tipo de notificação para uma classe CIM encapsulada.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Classe SnmpNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506246"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="41a27-103">Classe SnmpNotification</span><span class="sxs-lookup"><span data-stu-id="41a27-103">SnmpNotification class</span></span>

<span data-ttu-id="41a27-104">A classe **SnmpNotification** é mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM encapsulada.</span><span class="sxs-lookup"><span data-stu-id="41a27-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="41a27-105">É uma classe base usada pelo [provedor SNMP](snmp-provider.md) para qualquer classe mapeada da macro do [tipo de notificação](notification-type-macro.md) para uma classe CIM encapsulada pelo provedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="41a27-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="41a27-106">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="41a27-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="41a27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41a27-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="41a27-108">Membros</span><span class="sxs-lookup"><span data-stu-id="41a27-108">Members</span></span>

<span data-ttu-id="41a27-109">A classe **SnmpNotification** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41a27-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="41a27-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41a27-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41a27-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41a27-111">Properties</span></span>

<span data-ttu-id="41a27-112">A classe **SnmpNotification** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41a27-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41a27-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="41a27-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-116">Endereço de rede da entidade que criou a notificação.</span><span class="sxs-lookup"><span data-stu-id="41a27-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="41a27-117">Esse é o endereço real do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41a27-117">This is the actual address of the device.</span></span> <span data-ttu-id="41a27-118">Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="41a27-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="41a27-119">Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte é definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="41a27-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="41a27-120">Esta propriedade é válida somente para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="41a27-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-121">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="41a27-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-124">Protocolo de transporte usado pela entidade de envio.</span><span class="sxs-lookup"><span data-stu-id="41a27-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="41a27-125">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="41a27-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-126">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="41a27-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-129">Endereço de rede da entidade que enviou a notificação.</span><span class="sxs-lookup"><span data-stu-id="41a27-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="41a27-130">Este é o endereço da última entidade que encaminhou a notificação.</span><span class="sxs-lookup"><span data-stu-id="41a27-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="41a27-131">Quando a entidade de gerenciamento usa SNMP sobre UDP, o endereço de transporte se refere a um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="41a27-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="41a27-132">Quando a entidade de gerenciamento usa SNMP sobre IPX, o endereço de transporte se refere a um Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="41a27-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="41a27-133">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="41a27-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-134">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="41a27-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-137">O protocolo de transporte usado pela entidade de envio.</span><span class="sxs-lookup"><span data-stu-id="41a27-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-138">**Comunidade**</span><span class="sxs-lookup"><span data-stu-id="41a27-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-141">Nome da Comunidade associado a uma instância do PDU.</span><span class="sxs-lookup"><span data-stu-id="41a27-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="41a27-142">O nome da Comunidade autentica o originador da PDU.</span><span class="sxs-lookup"><span data-stu-id="41a27-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="41a27-143">Essa propriedade é válida para SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="41a27-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-144">**Identificação**</span><span class="sxs-lookup"><span data-stu-id="41a27-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41a27-147">Qualificadores: **\_ Convenção de texto** ("objectidentifier"), **codificação** ("objectidentifier") **, \_ sintaxe de objeto** ("objectidentifier"), **\_ identificador de objeto** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="41a27-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="41a27-148">Identificação autoritativa desta notificação.</span><span class="sxs-lookup"><span data-stu-id="41a27-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="41a27-149">Mapeia diretamente para a associação de variável SnmpTrapOID.</span><span class="sxs-lookup"><span data-stu-id="41a27-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="41a27-150">Esta propriedade é válida somente para o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="41a27-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="41a27-151">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="41a27-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-152">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="41a27-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="41a27-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-154">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="41a27-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="41a27-155">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="41a27-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="41a27-156">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="41a27-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="41a27-157">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="41a27-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-158">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41a27-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41a27-160">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="41a27-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="41a27-161">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="41a27-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="41a27-162">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="41a27-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="41a27-163">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="41a27-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="41a27-164">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="41a27-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="41a27-165">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="41a27-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41a27-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41a27-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41a27-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41a27-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41a27-168">Qualificadores: **\_ Convenção de texto** ("timetiques"), **codificação** ("timetiques") **, \_ sintaxe de objeto** ("timetiques"), **\_ identificador de objeto** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="41a27-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="41a27-169">Tempo em centésimos de um segundo desde que a parte de gerenciamento de rede do agente foi reinicializada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="41a27-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="41a27-170">A variável MIB sysUptime. 0, que é do tipo **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="41a27-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="41a27-171">Essa propriedade é mapeada para o carimbo de **data/hora** da propriedade de classe CIM, que é do tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="41a27-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="41a27-172">Esta propriedade é válida somente para o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="41a27-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41a27-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="41a27-173">Remarks</span></span>

<span data-ttu-id="41a27-174">Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **timestamp** ou **Identification** causa um conflito de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="41a27-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="41a27-175">Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.</span><span class="sxs-lookup"><span data-stu-id="41a27-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="41a27-176">Uma macro [de tipo de notificação](notification-type-macro.md) que contém referências a uma macro de [tipo de objeto](object-type-macro.md) chamada **Community** causa um conflito de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="41a27-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="41a27-177">Se esse conflito ocorrer, as propriedades obrigatórias terão precedência e as referências conflitantes deverão ser renomeadas.</span><span class="sxs-lookup"><span data-stu-id="41a27-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a27-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41a27-178">Requirements</span></span>



| <span data-ttu-id="41a27-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a27-179">Requirement</span></span> | <span data-ttu-id="41a27-180">Valor</span><span class="sxs-lookup"><span data-stu-id="41a27-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="41a27-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41a27-181">Minimum supported client</span></span><br/> | <span data-ttu-id="41a27-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41a27-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="41a27-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41a27-183">Minimum supported server</span></span><br/> | <span data-ttu-id="41a27-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41a27-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="41a27-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="41a27-185">Namespace</span></span><br/>                | <span data-ttu-id="41a27-186">\\Localhost SNMP \\ raiz</span><span class="sxs-lookup"><span data-stu-id="41a27-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41a27-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="41a27-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a27-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="41a27-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="41a27-189">Macro do tipo de notificação</span><span class="sxs-lookup"><span data-stu-id="41a27-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

