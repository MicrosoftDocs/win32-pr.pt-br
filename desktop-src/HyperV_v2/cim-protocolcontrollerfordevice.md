---
description: Representa uma associação entre um dispositivo lógico e um controlador de protocolo que está conectado ao dispositivo.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: Classe CIM_ProtocolControllerForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829197"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="ae986-103">\_Classe CIM ProtocolControllerForDevice</span><span class="sxs-lookup"><span data-stu-id="ae986-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="ae986-104">Representa uma associação entre um dispositivo lógico e um controlador de protocolo que está conectado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae986-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae986-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae986-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="ae986-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ae986-106">Members</span></span>

<span data-ttu-id="ae986-107">A classe **CIM \_ ProtocolControllerForDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae986-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ae986-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae986-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae986-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae986-109">Properties</span></span>

<span data-ttu-id="ae986-110">A classe **CIM \_ ProtocolControllerForDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae986-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae986-111">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="ae986-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae986-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae986-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae986-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae986-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae986-114">A prioridade de acesso dada ao dispositivo por meio do controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ae986-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="ae986-115">A prioridade mais alta tem o menor valor.</span><span class="sxs-lookup"><span data-stu-id="ae986-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="ae986-116">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="ae986-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae986-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae986-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae986-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae986-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae986-119">A acessibilidade do dispositivo lógico por meio do controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="ae986-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae986-120">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae986-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ae986-121">**Ativo** (2)</span><span class="sxs-lookup"><span data-stu-id="ae986-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ae986-122">**Inativo** (3)</span><span class="sxs-lookup"><span data-stu-id="ae986-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="ae986-123">**Replicação em andamento** (4)</span><span class="sxs-lookup"><span data-stu-id="ae986-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="ae986-124">**Mapeamento de inconsistência** (5)</span><span class="sxs-lookup"><span data-stu-id="ae986-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae986-125">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ae986-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae986-126">Tipo de dados: **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="ae986-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="ae986-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae986-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae986-128">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ae986-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ae986-129">O controlador de protocolo na associação.</span><span class="sxs-lookup"><span data-stu-id="ae986-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="ae986-130">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ae986-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae986-131">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="ae986-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ae986-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae986-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae986-133">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="ae986-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ae986-134">O dispositivo lógico na associação.</span><span class="sxs-lookup"><span data-stu-id="ae986-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="ae986-135">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="ae986-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae986-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae986-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae986-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae986-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae986-138">O endereço do dispositivo associado no contexto do controlador de controle de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ae986-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae986-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae986-139">Requirements</span></span>



| <span data-ttu-id="ae986-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae986-140">Requirement</span></span> | <span data-ttu-id="ae986-141">Valor</span><span class="sxs-lookup"><span data-stu-id="ae986-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae986-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae986-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ae986-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ae986-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ae986-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae986-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ae986-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae986-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ae986-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae986-146">Namespace</span></span><br/>                | <span data-ttu-id="ae986-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ae986-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae986-148">MOF</span><span class="sxs-lookup"><span data-stu-id="ae986-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae986-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae986-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae986-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ae986-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae986-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae986-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae986-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae986-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae986-153">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="ae986-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

