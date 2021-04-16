---
description: Classe abstrata que representa um recurso para uma determinada instância de um comutador Ethernet.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Classe Msvm_EthernetSwitchData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768508"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="e387b-103">\_Classe Msvm EthernetSwitchData</span><span class="sxs-lookup"><span data-stu-id="e387b-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="e387b-104">Classe abstrata que representa um recurso para uma determinada instância de um comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e387b-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="e387b-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e387b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e387b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e387b-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="e387b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e387b-107">Members</span></span>

<span data-ttu-id="e387b-108">A classe **Msvm \_ EthernetSwitchData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e387b-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="e387b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e387b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e387b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e387b-110">Properties</span></span>

<span data-ttu-id="e387b-111">A classe **Msvm \_ EthernetSwitchData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e387b-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e387b-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e387b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e387b-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e387b-115">A short description of the object.</span></span> <span data-ttu-id="e387b-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e387b-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e387b-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e387b-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e387b-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e387b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e387b-121">O nome da classe ou subclasse usada na criação dessa instância.</span><span class="sxs-lookup"><span data-stu-id="e387b-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="e387b-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e387b-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e387b-125">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e387b-125">A description of the object.</span></span> <span data-ttu-id="e387b-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e387b-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e387b-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e387b-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e387b-130">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e387b-130">A display name for the object.</span></span> <span data-ttu-id="e387b-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e387b-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e387b-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e387b-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e387b-135">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e387b-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e387b-136">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e387b-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e387b-137">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e387b-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e387b-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e387b-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e387b-141">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e387b-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e387b-142">O nome exclusivo do recurso.</span><span class="sxs-lookup"><span data-stu-id="e387b-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e387b-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e387b-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e387b-146">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e387b-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e387b-147">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="e387b-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="e387b-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e387b-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e387b-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e387b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e387b-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e387b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e387b-151">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e387b-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e387b-152">O nome do comutador virtual ao qual a instância de recurso associada está associada.</span><span class="sxs-lookup"><span data-stu-id="e387b-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e387b-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e387b-153">Requirements</span></span>



| <span data-ttu-id="e387b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e387b-154">Requirement</span></span> | <span data-ttu-id="e387b-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e387b-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e387b-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e387b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e387b-157">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e387b-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e387b-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e387b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e387b-159">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e387b-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e387b-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="e387b-160">Namespace</span></span><br/>                | <span data-ttu-id="e387b-161">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e387b-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e387b-162">MOF</span><span class="sxs-lookup"><span data-stu-id="e387b-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e387b-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e387b-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e387b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="e387b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e387b-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e387b-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

