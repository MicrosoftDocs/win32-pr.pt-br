---
description: Representa o estado configurado de um dispositivo de partição GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Classe Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921021"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="3409e-103">\_Classe Msvm GpuPartitionSettingData</span><span class="sxs-lookup"><span data-stu-id="3409e-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="3409e-104">Representa o estado configurado de um dispositivo de partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="3409e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3409e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3409e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3409e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="3409e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3409e-107">Members</span></span>

<span data-ttu-id="3409e-108">A classe **Msvm \_ GpuPartitionSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3409e-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3409e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3409e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3409e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3409e-110">Properties</span></span>

<span data-ttu-id="3409e-111">A classe **Msvm \_ GpuPartitionSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3409e-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3409e-112">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="3409e-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-115">A quantidade máxima de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-116">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="3409e-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-117">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-119">A quantidade máxima de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-120">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="3409e-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-121">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-123">A quantidade máxima de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-124">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="3409e-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-127">A quantidade máxima de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-128">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="3409e-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-131">A quantidade mínima de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-132">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="3409e-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-135">A quantidade mínima de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-136">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="3409e-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-137">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-139">A quantidade mínima de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-140">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="3409e-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-143">A quantidade mínima de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-144">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="3409e-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-145">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-147">A quantidade ideal de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-148">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="3409e-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-149">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-151">A quantidade ideal de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-152">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="3409e-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-155">A quantidade ideal de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="3409e-156">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="3409e-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3409e-157">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3409e-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3409e-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3409e-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3409e-159">A quantidade ideal de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="3409e-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3409e-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3409e-160">Requirements</span></span>



| <span data-ttu-id="3409e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="3409e-161">Requirement</span></span> | <span data-ttu-id="3409e-162">Valor</span><span class="sxs-lookup"><span data-stu-id="3409e-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3409e-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3409e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="3409e-164">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="3409e-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3409e-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3409e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="3409e-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3409e-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3409e-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="3409e-167">Namespace</span></span><br/>                | <span data-ttu-id="3409e-168">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3409e-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3409e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="3409e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3409e-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3409e-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3409e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="3409e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3409e-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3409e-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3409e-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="3409e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3409e-174">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3409e-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




