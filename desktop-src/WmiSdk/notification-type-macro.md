---
description: A macro do tipo de notificação contém os elementos a seguir.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro do tipo de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751763"
---
# <a name="notification-type-macro"></a><span data-ttu-id="86e0a-103">Macro do tipo de notificação</span><span class="sxs-lookup"><span data-stu-id="86e0a-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="86e0a-104">A macro do tipo de notificação contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="86e0a-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="86e0a-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="86e0a-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="86e0a-106">Componentes</span><span class="sxs-lookup"><span data-stu-id="86e0a-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="86e0a-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descritor de objeto</span><span class="sxs-lookup"><span data-stu-id="86e0a-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="86e0a-108">Anexa um nome a um evento SNMP em uma macro do tipo notificação.</span><span class="sxs-lookup"><span data-stu-id="86e0a-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="86e0a-109">A lista a seguir lista as regras para mapear o descritor de objeto.</span><span class="sxs-lookup"><span data-stu-id="86e0a-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="86e0a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="86e0a-110">Type</span></span>                        | <span data-ttu-id="86e0a-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="86e0a-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e0a-112">Nome da classe CIM encapsulada</span><span class="sxs-lookup"><span data-stu-id="86e0a-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="86e0a-113">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="86e0a-113">"SNMP\_"</span></span><br/> <span data-ttu-id="86e0a-114">Nome de identidade do módulo MIB</span><span class="sxs-lookup"><span data-stu-id="86e0a-114">MIB module identity name</span></span><br/> <span data-ttu-id="86e0a-115">sublinhado ( \_ )</span><span class="sxs-lookup"><span data-stu-id="86e0a-115">underscore (\_)</span></span><br/> <span data-ttu-id="86e0a-116">descritor de objeto</span><span class="sxs-lookup"><span data-stu-id="86e0a-116">object descriptor</span></span><br/> <span data-ttu-id="86e0a-117">" \_ Notificação"</span><span class="sxs-lookup"><span data-stu-id="86e0a-117">"\_Notification"</span></span><br/> <span data-ttu-id="86e0a-118">Exemplo: a notificação de **vtpServerDisabled** do **Cisco-VTP-MIB** é mapeada **para \_ \_ notificação de \_ \_ vtpServerDisabled de \_ MIB do Cisco VTP SNMP**.</span><span class="sxs-lookup"><span data-stu-id="86e0a-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="86e0a-119">Nome da classe CIM Referent</span><span class="sxs-lookup"><span data-stu-id="86e0a-119">Referent CIM class name</span></span>     | <span data-ttu-id="86e0a-120">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="86e0a-120">"SNMP\_"</span></span><br/> <span data-ttu-id="86e0a-121">Nome de identidade do módulo MIB</span><span class="sxs-lookup"><span data-stu-id="86e0a-121">MIB module identity name</span></span><br/> <span data-ttu-id="86e0a-122">sublinhado ( \_ )</span><span class="sxs-lookup"><span data-stu-id="86e0a-122">underscore (\_)</span></span><br/> <span data-ttu-id="86e0a-123">descritor de objeto</span><span class="sxs-lookup"><span data-stu-id="86e0a-123">object descriptor</span></span><br/> <span data-ttu-id="86e0a-124">" \_ ExtendedNotification"</span><span class="sxs-lookup"><span data-stu-id="86e0a-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="86e0a-125">Exemplo: a notificação de **vtpServerDisabled** do **Cisco-VTP-MIB** é mapeada para **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.</span><span class="sxs-lookup"><span data-stu-id="86e0a-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="86e0a-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Cláusula OBJECTs</span><span class="sxs-lookup"><span data-stu-id="86e0a-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="86e0a-127">Enumera o conjunto de objetos associados ao objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="86e0a-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="86e0a-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula de referência</span><span class="sxs-lookup"><span data-stu-id="86e0a-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="86e0a-129">Refere-se a outro documento que contém mais informações sobre o objeto.</span><span class="sxs-lookup"><span data-stu-id="86e0a-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="86e0a-130">Ele é mapeado para a **referência** de qualificador de classe CIM, que é do tipo cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="86e0a-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="86e0a-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula de descrição</span><span class="sxs-lookup"><span data-stu-id="86e0a-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="86e0a-132">Descreve o objeto em questão.</span><span class="sxs-lookup"><span data-stu-id="86e0a-132">Describes the object in question.</span></span> <span data-ttu-id="86e0a-133">Ele é mapeado para a **Descrição** do qualificador de classe CIM, que é do tipo cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="86e0a-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="86e0a-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Cláusula de STATUS</span><span class="sxs-lookup"><span data-stu-id="86e0a-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="86e0a-135">Indica se o objeto deve ter suporte.</span><span class="sxs-lookup"><span data-stu-id="86e0a-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="86e0a-136">Quando o status é **obsoleto** ou **preterido**, a notificação é descartada do mapeamento.</span><span class="sxs-lookup"><span data-stu-id="86e0a-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="86e0a-137">Caso contrário, essa cláusula é mapeada para o **status** do qualificador de classe CIM, que é do tipo **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="86e0a-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="86e0a-138">Para SNMPv1, o valor preferencial do **status** é **obrigatório** ou **opcional**, mas o qualificador pode conter algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="86e0a-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="86e0a-139">Para o SNMPv2C, o valor preferencial do **status** é **atual** ou **preterido**, mas o qualificador pode conter algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="86e0a-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86e0a-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="86e0a-140">Remarks</span></span>

<span data-ttu-id="86e0a-141">O provedor SNMP mapeia a macro do **tipo de notificação** para uma definição de classe encapsulada ou Referent.</span><span class="sxs-lookup"><span data-stu-id="86e0a-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="86e0a-142">Uma definição de classe encapsulada não expõe as informações de instância associadas ao objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="86e0a-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="86e0a-143">Em vez disso, a definição de classe codifica a cláusula OBJECTs como uma série de propriedades da classe de evento CIM.</span><span class="sxs-lookup"><span data-stu-id="86e0a-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="86e0a-144">Cada propriedade CIM reflete o nome, o tipo e o valor do objeto MIB correspondente na cláusula OBJECTs.</span><span class="sxs-lookup"><span data-stu-id="86e0a-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="86e0a-145">Se você precisar de informações de instância, será necessário mapear para uma classe Referent.</span><span class="sxs-lookup"><span data-stu-id="86e0a-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="86e0a-146">Uma definição de classe encapsulada é mapeada para a classe [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="86e0a-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="86e0a-147">Uma classe Referent define um objeto MIB e as informações de instância usadas para obter o objeto.</span><span class="sxs-lookup"><span data-stu-id="86e0a-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="86e0a-148">A definição de classe codifica a cláusula OBJECTs como uma série de propriedades da classe de evento CIM.</span><span class="sxs-lookup"><span data-stu-id="86e0a-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="86e0a-149">Cada propriedade CIM reflete o nome do objeto MIB correspondente na cláusula OBJECTs e o tipo como um objeto incorporado que reflete uma instância da classe associada a esse objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="86e0a-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="86e0a-150">Em seguida, o provedor gera uma classe associada ao objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="86e0a-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="86e0a-151">Por exemplo, **ifIndex** mapeia para uma classe incorporada chamada **SNMP \_ RFC1213 \_ MIB \_ ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="86e0a-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="86e0a-152">Para obter mais informações sobre esse tipo de classe, consulte [macro de tipo de objeto](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="86e0a-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




