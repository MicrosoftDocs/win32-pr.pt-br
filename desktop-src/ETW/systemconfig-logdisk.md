---
description: Classe SystemConfig_LogDisk-essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.
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
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106104"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="4c5f7-103">\_Classe SystemConfig LogDisk</span><span class="sxs-lookup"><span data-stu-id="4c5f7-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="4c5f7-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="4c5f7-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5f7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c5f7-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4c5f7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4c5f7-107">Members</span></span>

<span data-ttu-id="4c5f7-108">A classe **SystemConfig \_ LogDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c5f7-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="4c5f7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c5f7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c5f7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c5f7-110">Properties</span></span>

<span data-ttu-id="4c5f7-111">A classe **SystemConfig \_ LogDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c5f7-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-115">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-116">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-120">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-121">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-125">Qualificadores: **WmiDataId** (6), **Max** (4), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-126">Letra da unidade do disco no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="4c5f7-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-130">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-131">Tipo de unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-131">Type of disk drive.</span></span> <span data-ttu-id="4c5f7-132">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="4c5f7-132">Possible values are:</span></span>



| <span data-ttu-id="4c5f7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4c5f7-133">Value</span></span>                                                                        | <span data-ttu-id="4c5f7-134">Significado</span><span class="sxs-lookup"><span data-stu-id="4c5f7-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="4c5f7-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c5f7-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4c5f7-136">Partição</span><span class="sxs-lookup"><span data-stu-id="4c5f7-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="4c5f7-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4c5f7-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4c5f7-138">Volume</span><span class="sxs-lookup"><span data-stu-id="4c5f7-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="4c5f7-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4c5f7-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4c5f7-140">Partição estendida em vários discos</span><span class="sxs-lookup"><span data-stu-id="4c5f7-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4c5f7-141">**WPD**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-142">Tipo de dados: **char16**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-144">Qualificadores: **WmiDataId** (14), **Max** (16), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-145">Sistema de arquivos no disco lógico, por exemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-147">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-149">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-150">Número de clusters livres no volume especificado.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-154">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-155">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-159">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-160">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-164">Qualificadores: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-165">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-169">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-170">Número de índice da partição.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-172">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-174">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-175">Tamanho total da partição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-179">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-180">Número de setores no volume.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-181">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-184">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-185">Tamanho da unidade de disco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-187">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-189">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-190">Deslocamento inicial (em bytes) da partição desde o início do disco.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-192">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-194">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-195">Número de clusters usados e livres no volume.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="4c5f7-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f7-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c5f7-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f7-199">Qualificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="4c5f7-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="4c5f7-200">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c5f7-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c5f7-201">Requirements</span></span>



| <span data-ttu-id="4c5f7-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5f7-202">Requirement</span></span> | <span data-ttu-id="4c5f7-203">Valor</span><span class="sxs-lookup"><span data-stu-id="4c5f7-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c5f7-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c5f7-204">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5f7-205">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c5f7-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c5f7-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c5f7-206">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5f7-207">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c5f7-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c5f7-208">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4c5f7-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5f7-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="4c5f7-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




