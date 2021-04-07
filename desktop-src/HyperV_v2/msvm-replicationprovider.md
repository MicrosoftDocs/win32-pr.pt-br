---
description: Representa os provedores disponíveis para replicação.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Classe Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828590"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="056f5-103">\_Classe Msvm replicationprovider</span><span class="sxs-lookup"><span data-stu-id="056f5-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="056f5-104">Representa os provedores disponíveis para replicação.</span><span class="sxs-lookup"><span data-stu-id="056f5-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="056f5-105">A sintaxe a seguir é simplificada do código MOF e inclui essas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="056f5-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="056f5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="056f5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="056f5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="056f5-107">Members</span></span>

<span data-ttu-id="056f5-108">A classe **Msvm \_ replicationprovider** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="056f5-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="056f5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="056f5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="056f5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="056f5-110">Properties</span></span>

<span data-ttu-id="056f5-111">A classe **Msvm \_ replicationprovider** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="056f5-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="056f5-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="056f5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="056f5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="056f5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="056f5-115">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="056f5-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="056f5-116">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="056f5-116">A short description of the object.</span></span> <span data-ttu-id="056f5-117">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="056f5-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="056f5-118">Para esse objeto, o valor é:</span><span class="sxs-lookup"><span data-stu-id="056f5-118">For this object, the value is:</span></span>

<span data-ttu-id="056f5-119">"Provedor de replicação"</span><span class="sxs-lookup"><span data-stu-id="056f5-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="056f5-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="056f5-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="056f5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="056f5-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="056f5-123">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="056f5-123">A description of the object.</span></span> <span data-ttu-id="056f5-124">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="056f5-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="056f5-125">Para provedores externos, o valor é fornecido por eles.</span><span class="sxs-lookup"><span data-stu-id="056f5-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="056f5-126">Para o host para hospedar o provedor interno, o valor é:</span><span class="sxs-lookup"><span data-stu-id="056f5-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="056f5-127">"Provedor de replicação de máquina virtual para host Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="056f5-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="056f5-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="056f5-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="056f5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="056f5-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="056f5-131">Um nome de exibição para o provedor de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="056f5-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="056f5-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="056f5-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="056f5-133">Para o host para hospedar o provedor interno, essa propriedade é sempre definida como:</span><span class="sxs-lookup"><span data-stu-id="056f5-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="056f5-134">"Provedor de replicação de máquina virtual para host Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="056f5-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="056f5-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="056f5-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="056f5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="056f5-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="056f5-138">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="056f5-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="056f5-139">A ID da instância do WMI, que identifica o provedor.</span><span class="sxs-lookup"><span data-stu-id="056f5-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="056f5-140">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="056f5-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="056f5-141">O formato dessa propriedade é "Microsoft: <host-Machine-Name>\\ replicationprovider \\<provedor-Name>".</span><span class="sxs-lookup"><span data-stu-id="056f5-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="056f5-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="056f5-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="056f5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="056f5-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="056f5-145">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="056f5-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="056f5-146">O GUID (identificador global exclusivo) do provedor que identifica o provedor de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="056f5-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="056f5-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="056f5-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="056f5-148">No caso de um provedor externo, essa propriedade é o CLSID do objeto de classe COM do provedor.</span><span class="sxs-lookup"><span data-stu-id="056f5-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="056f5-149">Para o host para hospedar o provedor interno, essa propriedade é fixa como:</span><span class="sxs-lookup"><span data-stu-id="056f5-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="056f5-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="056f5-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="056f5-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="056f5-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="056f5-152">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="056f5-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="056f5-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="056f5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="056f5-154">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="056f5-154">The current statuses of the object.</span></span> <span data-ttu-id="056f5-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), e cada elemento da matriz é sempre definido como:</span><span class="sxs-lookup"><span data-stu-id="056f5-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="056f5-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)</span><span class="sxs-lookup"><span data-stu-id="056f5-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="056f5-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="056f5-157">Remarks</span></span>

<span data-ttu-id="056f5-158">Você pode usar qualquer um dos provedores disponíveis e a classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para habilitar uma relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="056f5-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="056f5-159">O Hyper-V, por padrão, escolhe o host interno ao provedor de host, que pode ser alterado durante a criação da replicação.</span><span class="sxs-lookup"><span data-stu-id="056f5-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="056f5-160">O serviço de gerenciamento do Hyper-V se comunica com um provedor externo usando COM.</span><span class="sxs-lookup"><span data-stu-id="056f5-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="056f5-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056f5-161">Requirements</span></span>



| <span data-ttu-id="056f5-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="056f5-162">Requirement</span></span> | <span data-ttu-id="056f5-163">Valor</span><span class="sxs-lookup"><span data-stu-id="056f5-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056f5-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="056f5-164">Minimum supported client</span></span><br/> | <span data-ttu-id="056f5-165">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="056f5-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="056f5-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="056f5-166">Minimum supported server</span></span><br/> | <span data-ttu-id="056f5-167">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="056f5-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="056f5-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="056f5-168">Namespace</span></span><br/>                | <span data-ttu-id="056f5-169">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="056f5-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="056f5-170">MOF</span><span class="sxs-lookup"><span data-stu-id="056f5-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="056f5-171"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="056f5-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="056f5-172">DLL</span><span class="sxs-lookup"><span data-stu-id="056f5-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="056f5-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="056f5-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="056f5-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="056f5-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056f5-175">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="056f5-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="056f5-176">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="056f5-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

