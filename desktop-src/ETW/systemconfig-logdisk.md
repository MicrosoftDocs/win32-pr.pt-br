---
description: Essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: Classe SystemConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967409"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="839d5-103">\_Classe SystemConfig LogDisk</span><span class="sxs-lookup"><span data-stu-id="839d5-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="839d5-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="839d5-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="839d5-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="839d5-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="839d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="839d5-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="839d5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="839d5-107">Members</span></span>

<span data-ttu-id="839d5-108">A classe **SystemConfig \_ LogDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="839d5-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="839d5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="839d5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="839d5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="839d5-110">Properties</span></span>

<span data-ttu-id="839d5-111">A classe **SystemConfig \_ LogDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="839d5-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="839d5-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="839d5-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-115">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="839d5-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-116">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="839d5-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="839d5-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-120">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="839d5-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-121">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="839d5-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="839d5-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="839d5-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="839d5-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-125">Qualificadores: **WmiDataId** (6), **Max** (4), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="839d5-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="839d5-126">Letra da unidade do disco no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="839d5-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="839d5-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="839d5-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-130">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="839d5-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-131">Tipo de unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="839d5-131">Type of disk drive.</span></span> <span data-ttu-id="839d5-132">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="839d5-132">Possible values are:</span></span>



| <span data-ttu-id="839d5-133">Valor</span><span class="sxs-lookup"><span data-stu-id="839d5-133">Value</span></span>                                                                        | <span data-ttu-id="839d5-134">Significado</span><span class="sxs-lookup"><span data-stu-id="839d5-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="839d5-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="839d5-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="839d5-136">Partition</span><span class="sxs-lookup"><span data-stu-id="839d5-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="839d5-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="839d5-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="839d5-138">Volume</span><span class="sxs-lookup"><span data-stu-id="839d5-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="839d5-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="839d5-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="839d5-140">Partição estendida em vários discos</span><span class="sxs-lookup"><span data-stu-id="839d5-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="839d5-141">**WPD**</span><span class="sxs-lookup"><span data-stu-id="839d5-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-142">Tipo de dados: **char16**</span><span class="sxs-lookup"><span data-stu-id="839d5-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-144">Qualificadores: **WmiDataId** (14), **Max** (16), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="839d5-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="839d5-145">Sistema de arquivos no disco lógico, por exemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="839d5-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="839d5-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-147">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="839d5-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-149">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="839d5-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-150">Número de clusters livres no volume especificado.</span><span class="sxs-lookup"><span data-stu-id="839d5-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="839d5-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-154">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="839d5-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-155">Não usado.</span><span class="sxs-lookup"><span data-stu-id="839d5-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="839d5-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-159">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="839d5-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-160">Não usado.</span><span class="sxs-lookup"><span data-stu-id="839d5-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="839d5-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-164">Qualificadores: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="839d5-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-165">Não usado.</span><span class="sxs-lookup"><span data-stu-id="839d5-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="839d5-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-169">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="839d5-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-170">Número de índice da partição.</span><span class="sxs-lookup"><span data-stu-id="839d5-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="839d5-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-172">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="839d5-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-174">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="839d5-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-175">Tamanho total da partição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="839d5-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="839d5-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-179">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="839d5-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-180">Número de setores no volume.</span><span class="sxs-lookup"><span data-stu-id="839d5-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-181">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="839d5-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-184">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="839d5-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-185">Tamanho da unidade de disco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="839d5-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="839d5-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-187">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="839d5-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-189">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="839d5-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-190">Deslocamento inicial (em bytes) da partição desde o início do disco.</span><span class="sxs-lookup"><span data-stu-id="839d5-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="839d5-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-192">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="839d5-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-194">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="839d5-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-195">Número de clusters usados e livres no volume.</span><span class="sxs-lookup"><span data-stu-id="839d5-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="839d5-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="839d5-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839d5-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="839d5-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="839d5-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839d5-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839d5-199">Qualificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="839d5-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="839d5-200">Reservado.</span><span class="sxs-lookup"><span data-stu-id="839d5-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="839d5-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839d5-201">Requirements</span></span>



| <span data-ttu-id="839d5-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="839d5-202">Requirement</span></span> | <span data-ttu-id="839d5-203">Valor</span><span class="sxs-lookup"><span data-stu-id="839d5-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="839d5-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839d5-204">Minimum supported client</span></span><br/> | <span data-ttu-id="839d5-205">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="839d5-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="839d5-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839d5-206">Minimum supported server</span></span><br/> | <span data-ttu-id="839d5-207">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="839d5-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="839d5-208">Confira também</span><span class="sxs-lookup"><span data-stu-id="839d5-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839d5-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="839d5-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




