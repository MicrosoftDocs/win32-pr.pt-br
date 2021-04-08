---
description: Representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo discos DeviceID (chave).
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Classe CIM_LogicalDisk (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922258"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="8def3-103">Classe CIM_LogicalDisk (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8def3-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="8def3-104">Representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo **DeviceID** (chave) do disco.</span><span class="sxs-lookup"><span data-stu-id="8def3-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="8def3-105">Por exemplo, em um ambiente do Windows, o campo **DeviceID** contém uma letra da unidade; em um ambiente UNIX, ele contém o caminho de acesso; e em um ambiente do NetWare, ele contém o nome do volume.</span><span class="sxs-lookup"><span data-stu-id="8def3-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8def3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8def3-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="8def3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8def3-107">Members</span></span>

<span data-ttu-id="8def3-108">A classe do **\_ LogicalDisk CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8def3-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="8def3-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8def3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8def3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8def3-110">Properties</span></span>

<span data-ttu-id="8def3-111">A classe **CIM \_ LogicalDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8def3-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8def3-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="8def3-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8def3-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8def3-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8def3-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8def3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8def3-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="8def3-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="8def3-116">Indica se o dispositivo lógico usa o formato de nome do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8def3-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8def3-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8def3-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="8def3-118">**Nome do dispositivo do so** (12)</span><span class="sxs-lookup"><span data-stu-id="8def3-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8def3-119">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="8def3-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8def3-120">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8def3-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8def3-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8def3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8def3-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span><span class="sxs-lookup"><span data-stu-id="8def3-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="8def3-123">Indica se o dispositivo lógico tem o mesmo namespace que o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8def3-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8def3-124">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8def3-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="8def3-125">**Namespace de dispositivo do so** (8)</span><span class="sxs-lookup"><span data-stu-id="8def3-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="8def3-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8def3-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8def3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8def3-127">Requirements</span></span>



| <span data-ttu-id="8def3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8def3-128">Requirement</span></span> | <span data-ttu-id="8def3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8def3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8def3-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8def3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8def3-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8def3-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8def3-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8def3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8def3-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8def3-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8def3-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8def3-134">Namespace</span></span><br/>                | <span data-ttu-id="8def3-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8def3-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8def3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8def3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8def3-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8def3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8def3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8def3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8def3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8def3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8def3-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8def3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8def3-141">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8def3-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

