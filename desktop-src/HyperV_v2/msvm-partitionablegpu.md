---
description: Representa uma GPU particionável. Cada GPU pode ser segmentada em várias partições GPU, que podem ser atribuídas a uma máquina virtual como uma vGPU.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Classe Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837127"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="fe44c-104">\_Classe Msvm PartitionableGpu</span><span class="sxs-lookup"><span data-stu-id="fe44c-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="fe44c-105">Representa uma GPU particionável.</span><span class="sxs-lookup"><span data-stu-id="fe44c-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="fe44c-106">Cada GPU pode ser segmentada em várias partições GPU, que podem ser atribuídas a uma máquina virtual como uma vGPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="fe44c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fe44c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe44c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe44c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="fe44c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fe44c-109">Members</span></span>

<span data-ttu-id="fe44c-110">A classe **Msvm \_ PartitionableGpu** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fe44c-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="fe44c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe44c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe44c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe44c-112">Properties</span></span>

<span data-ttu-id="fe44c-113">A classe **Msvm \_ PartitionableGpu** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fe44c-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe44c-114">**AvailableCompute**</span><span class="sxs-lookup"><span data-stu-id="fe44c-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-115">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-117">A quantidade disponível de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-118">**AvailableDecode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-119">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-121">A quantidade disponível de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-122">**AvailableEncode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-125">A quantidade disponível de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-126">**AvailableVRAM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-127">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-129">A quantidade disponível de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-130">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="fe44c-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-131">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-133">A quantidade máxima de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-134">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-137">A quantidade máxima de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-138">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-139">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-141">A quantidade máxima de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-142">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-145">A quantidade máxima de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-146">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="fe44c-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-147">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-149">A quantidade mínima de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-150">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-151">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-153">A quantidade mínima de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-154">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-155">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-157">A quantidade mínima de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-158">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-159">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-161">A quantidade mínima de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-162">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="fe44c-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-163">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-165">A quantidade ideal de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-166">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-167">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-169">A quantidade ideal de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-170">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-171">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-173">A quantidade ideal de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-174">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-175">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-177">A quantidade ideal de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="fe44c-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe44c-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe44c-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-181">A quantidade de partições GPU na qual a GPU física é segmentada.</span><span class="sxs-lookup"><span data-stu-id="fe44c-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-182">**TotalCompute**</span><span class="sxs-lookup"><span data-stu-id="fe44c-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-183">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-185">A quantidade total de mecanismos de computação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-186">**TotalDecode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-187">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-189">A quantidade total de mecanismos de decodificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-190">**TotalEncode**</span><span class="sxs-lookup"><span data-stu-id="fe44c-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-191">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-193">A quantidade total de mecanismos de codificação que serão exibidos na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-194">**TotalVRAM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-195">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe44c-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fe44c-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-197">A quantidade total de VRAM que será exibida na partição GPU.</span><span class="sxs-lookup"><span data-stu-id="fe44c-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="fe44c-198">**ValidPartitionCounts**</span><span class="sxs-lookup"><span data-stu-id="fe44c-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe44c-199">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fe44c-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fe44c-200">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fe44c-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fe44c-201">Uma matriz de opções de partição GPU válidas na qual a GPU física pode ser dividida.</span><span class="sxs-lookup"><span data-stu-id="fe44c-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe44c-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe44c-202">Requirements</span></span>



| <span data-ttu-id="fe44c-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe44c-203">Requirement</span></span> | <span data-ttu-id="fe44c-204">Valor</span><span class="sxs-lookup"><span data-stu-id="fe44c-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe44c-205">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe44c-205">Minimum supported client</span></span><br/> | <span data-ttu-id="fe44c-206">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="fe44c-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe44c-207">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe44c-207">Minimum supported server</span></span><br/> | <span data-ttu-id="fe44c-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe44c-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fe44c-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe44c-209">Namespace</span></span><br/>                | <span data-ttu-id="fe44c-210">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fe44c-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fe44c-211">MOF</span><span class="sxs-lookup"><span data-stu-id="fe44c-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe44c-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe44c-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe44c-213">DLL</span><span class="sxs-lookup"><span data-stu-id="fe44c-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe44c-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe44c-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe44c-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe44c-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe44c-216">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fe44c-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




