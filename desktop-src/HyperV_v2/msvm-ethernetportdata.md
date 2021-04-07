---
description: Uma classe abstrata que representa os dados de tempo de execução de porta coletados por uma extensão de comutador Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Classe Msvm_EthernetPortData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828598"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="41df8-103">\_Classe Msvm EthernetPortData</span><span class="sxs-lookup"><span data-stu-id="41df8-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="41df8-104">Uma classe abstrata que representa os dados de tempo de execução de porta coletados por uma extensão de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="41df8-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="41df8-105">Todas as classes de dados de porta Ethernet devem derivar dessa classe abstrata.</span><span class="sxs-lookup"><span data-stu-id="41df8-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="41df8-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="41df8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41df8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41df8-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="41df8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="41df8-108">Members</span></span>

<span data-ttu-id="41df8-109">A classe **Msvm \_ EthernetPortData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41df8-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="41df8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41df8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41df8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41df8-111">Properties</span></span>

<span data-ttu-id="41df8-112">A classe **Msvm \_ EthernetPortData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41df8-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41df8-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="41df8-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41df8-116">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="41df8-116">A short description of the object.</span></span> <span data-ttu-id="41df8-117">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41df8-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41df8-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41df8-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41df8-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-122">O nome da subclasse usada na criação desta instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="41df8-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="41df8-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41df8-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41df8-126">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="41df8-126">A description of the object.</span></span> <span data-ttu-id="41df8-127">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41df8-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41df8-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41df8-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-131">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice CIM**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41df8-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-132">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="41df8-132">The scoping system's creation class name.</span></span> <span data-ttu-id="41df8-133">Essa propriedade é sempre definida como "Msvm \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="41df8-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="41df8-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="41df8-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-137">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice CIM**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41df8-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-138">A ID do dispositivo da porta que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="41df8-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="41df8-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="41df8-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41df8-142">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="41df8-142">A display name for the object.</span></span> <span data-ttu-id="41df8-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41df8-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41df8-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="41df8-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-147">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="41df8-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41df8-148">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="41df8-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="41df8-149">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41df8-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41df8-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="41df8-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-153">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41df8-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-154">Uma cadeia de caracteres que identifica exclusivamente essa instância de dados de porta dentro do escopo do comutador e da porta.</span><span class="sxs-lookup"><span data-stu-id="41df8-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="41df8-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41df8-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-158">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41df8-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-159">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="41df8-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="41df8-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="41df8-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41df8-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41df8-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41df8-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41df8-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41df8-163">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41df8-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41df8-164">O nome do comutador virtual que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="41df8-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41df8-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41df8-165">Requirements</span></span>



| <span data-ttu-id="41df8-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="41df8-166">Requirement</span></span> | <span data-ttu-id="41df8-167">Valor</span><span class="sxs-lookup"><span data-stu-id="41df8-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41df8-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41df8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="41df8-169">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="41df8-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41df8-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41df8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="41df8-171">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="41df8-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41df8-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="41df8-172">Namespace</span></span><br/>                | <span data-ttu-id="41df8-173">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="41df8-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41df8-174">MOF</span><span class="sxs-lookup"><span data-stu-id="41df8-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41df8-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41df8-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41df8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="41df8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41df8-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41df8-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

