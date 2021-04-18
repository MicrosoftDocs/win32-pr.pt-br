---
description: Define uma conexão que está atualmente ativada e configurada para fornecer comunicação entre dois \_ objetos CIM ServiceAccessPoint.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767649"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="d81b3-103">\_Classe de ACTIVECONNECTION CIM</span><span class="sxs-lookup"><span data-stu-id="d81b3-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="d81b3-104">Define uma conexão que está atualmente ativada e configurada para fornecer comunicação entre dois objetos **CIM \_ ServiceAccessPoint** .</span><span class="sxs-lookup"><span data-stu-id="d81b3-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="d81b3-105">**CIM \_ O ActiveConnection** é usado quando a conexão não é tratada como um objeto **\_ managedelement CIM** .</span><span class="sxs-lookup"><span data-stu-id="d81b3-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="d81b3-106">Pontos de acesso de serviço conectados por uma conexão ativa normalmente estão na mesma camada de rede ou de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d81b3-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d81b3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d81b3-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="d81b3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d81b3-108">Members</span></span>

<span data-ttu-id="d81b3-109">A classe **CIM \_ ActiveConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d81b3-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="d81b3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d81b3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d81b3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d81b3-111">Properties</span></span>

<span data-ttu-id="d81b3-112">A classe **CIM \_ ActiveConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d81b3-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d81b3-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d81b3-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d81b3-114">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="d81b3-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d81b3-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d81b3-117">O ponto de acesso de serviço que está conectado ao outro ponto de acesso de serviço por meio da conexão ativa.</span><span class="sxs-lookup"><span data-stu-id="d81b3-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="d81b3-118">**CIM \_ Objeto ServiceAccessPoint** .</span><span class="sxs-lookup"><span data-stu-id="d81b3-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="d81b3-119">Em uma conexão unidirecional, esse ponto de acesso é aquele que está transmitindo dados.</span><span class="sxs-lookup"><span data-stu-id="d81b3-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="d81b3-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d81b3-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d81b3-121">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="d81b3-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d81b3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d81b3-124">O ponto de acesso de serviço configurado para se comunicar ou está se comunicando ativamente com o ponto de acesso de serviço especificado na propriedade **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="d81b3-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="d81b3-125">Em uma conexão unidirecional, esse ponto de acesso é aquele que está recebendo dados.</span><span class="sxs-lookup"><span data-stu-id="d81b3-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="d81b3-126">**Unidirecional**</span><span class="sxs-lookup"><span data-stu-id="d81b3-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d81b3-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d81b3-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d81b3-129">True se a conexão for unidirecional; false se a conexão for bidirecional.</span><span class="sxs-lookup"><span data-stu-id="d81b3-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="d81b3-130">Quando a conexão é unidirecional, a propriedade **Antecedent** especifica o ponto de acesso que está transmitindo dados.</span><span class="sxs-lookup"><span data-stu-id="d81b3-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="d81b3-131">Em uma conexão bidirecional, o **Antecedent** pode especificar o ponto de acesso atribuído à conexão.</span><span class="sxs-lookup"><span data-stu-id="d81b3-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d81b3-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="d81b3-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d81b3-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d81b3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-135">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Traffictype**")</span><span class="sxs-lookup"><span data-stu-id="d81b3-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="d81b3-136">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="d81b3-136">This property is deprecated.</span></span> <span data-ttu-id="d81b3-137">Em vez disso, recomendamos que você especifique essas informações no endereçamento, protocolo e funcionalidade básica dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d81b3-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="d81b3-138">Uma descrição do tipo de tráfego que é especificado quando a propriedade **traffictype** é definida como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="d81b3-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="d81b3-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="d81b3-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d81b3-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d81b3-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d81b3-142">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("no value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")</span><span class="sxs-lookup"><span data-stu-id="d81b3-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="d81b3-143">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="d81b3-143">This property is deprecated.</span></span> <span data-ttu-id="d81b3-144">Em vez disso, recomendamos que você especifique essas informações no endereçamento, protocolo e funcionalidade básica dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d81b3-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="d81b3-145">O tipo de tráfego transmitido por essa conexão.</span><span class="sxs-lookup"><span data-stu-id="d81b3-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d81b3-146">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d81b3-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d81b3-147">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d81b3-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="d81b3-148">**Unicast** (2)</span><span class="sxs-lookup"><span data-stu-id="d81b3-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="d81b3-149">**Difusão** (3)</span><span class="sxs-lookup"><span data-stu-id="d81b3-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="d81b3-150">**Multicast** (4)</span><span class="sxs-lookup"><span data-stu-id="d81b3-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="d81b3-151">**Anycast** (5)</span><span class="sxs-lookup"><span data-stu-id="d81b3-151">**Anycast** (5)</span></span>


<span data-ttu-id="d81b3-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d81b3-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d81b3-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d81b3-153">Requirements</span></span>



| <span data-ttu-id="d81b3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="d81b3-154">Requirement</span></span> | <span data-ttu-id="d81b3-155">Valor</span><span class="sxs-lookup"><span data-stu-id="d81b3-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81b3-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d81b3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d81b3-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d81b3-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d81b3-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d81b3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d81b3-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d81b3-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d81b3-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="d81b3-160">Namespace</span></span><br/>                | <span data-ttu-id="d81b3-161">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d81b3-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d81b3-162">MOF</span><span class="sxs-lookup"><span data-stu-id="d81b3-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d81b3-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d81b3-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d81b3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d81b3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d81b3-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d81b3-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d81b3-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="d81b3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d81b3-167">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="d81b3-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

