---
description: Conecta uma porta de comutador ao ponto de extremidade da LAN ao qual a porta está conectada.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829483"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="81bbb-103">\_Classe Msvm ActiveConnection</span><span class="sxs-lookup"><span data-stu-id="81bbb-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="81bbb-104">Conecta uma porta de comutador ao ponto de extremidade da LAN ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="81bbb-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="81bbb-105">A existência desse objeto significa que a porta do comutador e o ponto de extremidade da LAN estão ativamente conectados e a porta Ethernet associada ao ponto de extremidade da LAN pode se comunicar com a rede por meio da porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="81bbb-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="81bbb-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81bbb-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bbb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81bbb-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="81bbb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="81bbb-108">Members</span></span>

<span data-ttu-id="81bbb-109">A classe **Msvm \_ ActiveConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81bbb-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="81bbb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81bbb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81bbb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81bbb-111">Properties</span></span>

<span data-ttu-id="81bbb-112">A classe **Msvm \_ ActiveConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81bbb-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81bbb-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="81bbb-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbb-114">Tipo de dados: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="81bbb-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bbb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="81bbb-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="81bbb-117">Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) que representa o SAP (ponto de acesso a serviços) configurado para comunicação ou que está se comunicando ativamente com o SAP dependente.</span><span class="sxs-lookup"><span data-stu-id="81bbb-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="81bbb-118">Em uma conexão unidirecional, esse SAP é aquele que está transmitindo.</span><span class="sxs-lookup"><span data-stu-id="81bbb-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="81bbb-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="81bbb-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbb-120">Tipo de dados: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="81bbb-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bbb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="81bbb-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="81bbb-123">Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](cim-lanendpoint.md) que representa o SAP que está configurado para se comunicar ou que está se comunicando ativamente com o SAP Antecedent.</span><span class="sxs-lookup"><span data-stu-id="81bbb-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="81bbb-124">Em uma conexão unidirecional, esse SAP é aquele que está recebendo.</span><span class="sxs-lookup"><span data-stu-id="81bbb-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="81bbb-125">**Unidirecional**</span><span class="sxs-lookup"><span data-stu-id="81bbb-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbb-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81bbb-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bbb-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbb-128">Se essa propriedade for **true**, essa conexão será unidirecional; caso contrário, essa conexão será bidirecional.</span><span class="sxs-lookup"><span data-stu-id="81bbb-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="81bbb-129">Quando uma conexão é unidirecional, o "alto-falante" deve ser definido como referência **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="81bbb-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="81bbb-130">Em uma conexão bidirecional, não importa se o ponto de acesso selecionado é o **Antecedent** ou **dependente**.</span><span class="sxs-lookup"><span data-stu-id="81bbb-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="81bbb-131">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81bbb-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81bbb-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="81bbb-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbb-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bbb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bbb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbb-135">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="81bbb-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81bbb-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="81bbb-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bbb-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bbb-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bbb-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bbb-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bbb-139">Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="81bbb-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81bbb-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="81bbb-140">Remarks</span></span>

<span data-ttu-id="81bbb-141">O acesso à classe **Msvm \_ ActiveConnection** pode ser restringido pela filtragem UAC.</span><span class="sxs-lookup"><span data-stu-id="81bbb-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="81bbb-142">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="81bbb-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="81bbb-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81bbb-143">Examples</span></span>

<span data-ttu-id="81bbb-144">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="81bbb-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81bbb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bbb-145">Requirements</span></span>



| <span data-ttu-id="81bbb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="81bbb-146">Requirement</span></span> | <span data-ttu-id="81bbb-147">Valor</span><span class="sxs-lookup"><span data-stu-id="81bbb-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81bbb-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bbb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="81bbb-149">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81bbb-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81bbb-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bbb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="81bbb-151">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81bbb-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81bbb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="81bbb-152">Namespace</span></span><br/>                | <span data-ttu-id="81bbb-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="81bbb-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81bbb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="81bbb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81bbb-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81bbb-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81bbb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="81bbb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81bbb-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81bbb-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81bbb-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="81bbb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bbb-159">**ActiveConnection do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="81bbb-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="81bbb-160">[**ActiveConnection do CIM \_**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81bbb-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

