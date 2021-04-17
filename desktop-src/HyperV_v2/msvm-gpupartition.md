---
description: Representa o estado da partição GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Classe Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759405"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="32781-103">\_Classe Msvm GpuPartition</span><span class="sxs-lookup"><span data-stu-id="32781-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="32781-104">Representa o estado da partição GPU.</span><span class="sxs-lookup"><span data-stu-id="32781-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="32781-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="32781-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32781-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32781-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="32781-107">Membros</span><span class="sxs-lookup"><span data-stu-id="32781-107">Members</span></span>

<span data-ttu-id="32781-108">A classe **Msvm \_ GpuPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="32781-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="32781-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32781-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32781-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32781-110">Properties</span></span>

<span data-ttu-id="32781-111">A classe **Msvm \_ GpuPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="32781-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32781-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="32781-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32781-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="32781-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32781-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32781-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32781-115">Uma cadeia de caracteres que contém o caminho da instância do dispositivo que identifica o dispositivo de partição GPU.</span><span class="sxs-lookup"><span data-stu-id="32781-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="32781-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="32781-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32781-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32781-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32781-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32781-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32781-119">A ID da partição do dispositivo de partição GPU.</span><span class="sxs-lookup"><span data-stu-id="32781-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="32781-120">**PartitionVfLuid**</span><span class="sxs-lookup"><span data-stu-id="32781-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32781-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="32781-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32781-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32781-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32781-123">A LUID da função virtual, que representa uma partição GPU.</span><span class="sxs-lookup"><span data-stu-id="32781-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32781-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32781-124">Requirements</span></span>



| <span data-ttu-id="32781-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="32781-125">Requirement</span></span> | <span data-ttu-id="32781-126">Valor</span><span class="sxs-lookup"><span data-stu-id="32781-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32781-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32781-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32781-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="32781-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32781-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32781-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32781-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="32781-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="32781-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="32781-131">Namespace</span></span><br/>                | <span data-ttu-id="32781-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="32781-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="32781-133">MOF</span><span class="sxs-lookup"><span data-stu-id="32781-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32781-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32781-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32781-135">DLL</span><span class="sxs-lookup"><span data-stu-id="32781-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32781-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32781-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32781-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="32781-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32781-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="32781-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




