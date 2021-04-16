---
description: Conecta uma porta de comutador ao ponto de extremidade de Fibre Channel ao qual a porta está conectada.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759241"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="8b953-103">\_Classe Msvm FcActiveConnection</span><span class="sxs-lookup"><span data-stu-id="8b953-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="8b953-104">Conecta uma porta de comutador ao ponto de extremidade de Fibre Channel ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="8b953-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="8b953-105">A existência desse objeto significa que a porta do comutador e o ponto de extremidade de Fibre Channel estão ativamente conectados, e a porta de Fibre Channel associada ao ponto de extremidade Fibre Channel pode se comunicar com a rede por meio da porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="8b953-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="8b953-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8b953-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b953-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b953-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="8b953-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8b953-108">Members</span></span>

<span data-ttu-id="8b953-109">A classe **Msvm \_ FcActiveConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b953-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="8b953-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b953-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b953-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b953-111">Properties</span></span>

<span data-ttu-id="8b953-112">A classe **Msvm \_ FcActiveConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b953-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b953-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="8b953-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b953-114">Tipo de dados: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8b953-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="8b953-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b953-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b953-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="8b953-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8b953-117">Uma referência a uma instância da classe [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) que representa o SAP (ponto de acesso a serviços) configurado para comunicação ou que está se comunicando ativamente com o SAP dependente.</span><span class="sxs-lookup"><span data-stu-id="8b953-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="8b953-118">Em uma conexão unidirecional, esse SAP é aquele que está transmitindo.</span><span class="sxs-lookup"><span data-stu-id="8b953-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="8b953-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="8b953-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b953-120">Tipo de dados: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8b953-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="8b953-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b953-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b953-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="8b953-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8b953-123">Uma referência a uma instância da classe [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) que representa o SAP que está configurado para se comunicar ou que está se comunicando ativamente com o SAP Antecedent.</span><span class="sxs-lookup"><span data-stu-id="8b953-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="8b953-124">Em uma conexão unidirecional, esse SAP é aquele que está recebendo.</span><span class="sxs-lookup"><span data-stu-id="8b953-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="8b953-125">**Unidirecional**</span><span class="sxs-lookup"><span data-stu-id="8b953-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b953-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b953-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b953-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b953-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b953-128">Se essa propriedade for **true**, essa conexão será unidirecional; caso contrário, essa conexão será bidirecional.</span><span class="sxs-lookup"><span data-stu-id="8b953-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="8b953-129">Quando uma conexão é unidirecional, o "alto-falante" deve ser definido como referência **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="8b953-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="8b953-130">Em uma conexão bidirecional, não importa se o ponto de acesso selecionado é o **Antecedent** ou **dependente**.</span><span class="sxs-lookup"><span data-stu-id="8b953-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="8b953-131">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b953-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b953-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="8b953-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b953-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b953-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b953-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b953-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b953-135">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8b953-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b953-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="8b953-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b953-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b953-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b953-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b953-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b953-139">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8b953-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b953-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b953-140">Requirements</span></span>



| <span data-ttu-id="8b953-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b953-141">Requirement</span></span> | <span data-ttu-id="8b953-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8b953-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b953-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b953-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8b953-144">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8b953-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b953-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b953-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8b953-146">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8b953-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b953-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b953-147">Namespace</span></span><br/>                | <span data-ttu-id="8b953-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8b953-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b953-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8b953-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b953-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b953-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b953-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8b953-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b953-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b953-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

