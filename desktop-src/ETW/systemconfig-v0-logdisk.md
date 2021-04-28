---
description: Classe SystemConfig_V0_LogDisk-essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Classe SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb0ad959d637a38a03b77bd8d7a812ff608ddc04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105974"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="25f75-103">\_Classe SystemConfig V0 \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="25f75-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="25f75-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="25f75-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="25f75-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="25f75-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f75-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f75-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="25f75-107">Membros</span><span class="sxs-lookup"><span data-stu-id="25f75-107">Members</span></span>

<span data-ttu-id="25f75-108">A classe **SystemConfig \_ V0 \_ LogDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="25f75-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="25f75-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25f75-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25f75-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25f75-110">Properties</span></span>

<span data-ttu-id="25f75-111">A classe **SystemConfig \_ V0 \_ LogDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="25f75-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25f75-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="25f75-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-115">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="25f75-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-116">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="25f75-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="25f75-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-120">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="25f75-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-121">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="25f75-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="25f75-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-123">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="25f75-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="25f75-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-125">Qualificadores: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="25f75-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-126">Letra da unidade do disco no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="25f75-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="25f75-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="25f75-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-130">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="25f75-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-131">Tipo de unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="25f75-131">Type of disk drive.</span></span> <span data-ttu-id="25f75-132">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="25f75-132">Possible values are:</span></span>



| <span data-ttu-id="25f75-133">Valor</span><span class="sxs-lookup"><span data-stu-id="25f75-133">Value</span></span>                                                                        | <span data-ttu-id="25f75-134">Significado</span><span class="sxs-lookup"><span data-stu-id="25f75-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="25f75-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="25f75-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="25f75-136">Partição</span><span class="sxs-lookup"><span data-stu-id="25f75-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="25f75-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="25f75-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="25f75-138">Volume</span><span class="sxs-lookup"><span data-stu-id="25f75-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="25f75-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="25f75-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="25f75-140">Partição estendida em vários discos</span><span class="sxs-lookup"><span data-stu-id="25f75-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="25f75-141">**WPD**</span><span class="sxs-lookup"><span data-stu-id="25f75-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-142">Tipo de dados: **char16**</span><span class="sxs-lookup"><span data-stu-id="25f75-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-144">Qualificadores: **WmiDataId** (13), **máx** . (16)</span><span class="sxs-lookup"><span data-stu-id="25f75-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-145">Sistema de arquivos no disco lógico, por exemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="25f75-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="25f75-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-147">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="25f75-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-149">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="25f75-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-150">Número de clusters livres no volume especificado.</span><span class="sxs-lookup"><span data-stu-id="25f75-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-151">**Bloco**</span><span class="sxs-lookup"><span data-stu-id="25f75-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-154">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="25f75-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-155">Reservado.</span><span class="sxs-lookup"><span data-stu-id="25f75-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="25f75-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-159">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="25f75-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-160">Número de índice da partição.</span><span class="sxs-lookup"><span data-stu-id="25f75-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="25f75-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-162">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="25f75-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-164">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="25f75-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-165">Tamanho total da partição, em bytes.</span><span class="sxs-lookup"><span data-stu-id="25f75-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="25f75-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-169">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="25f75-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-170">Número de setores no volume.</span><span class="sxs-lookup"><span data-stu-id="25f75-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-171">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="25f75-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-174">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="25f75-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-175">Tamanho da unidade de disco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="25f75-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="25f75-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-177">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="25f75-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-179">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="25f75-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-180">Deslocamento inicial (em bytes) da partição desde o início do disco.</span><span class="sxs-lookup"><span data-stu-id="25f75-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="25f75-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-182">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="25f75-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-184">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="25f75-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-185">Número de clusters usados e livres no volume.</span><span class="sxs-lookup"><span data-stu-id="25f75-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="25f75-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="25f75-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f75-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25f75-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25f75-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25f75-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f75-189">Qualificadores: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="25f75-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="25f75-190">Reservado.</span><span class="sxs-lookup"><span data-stu-id="25f75-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25f75-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f75-191">Requirements</span></span>



| <span data-ttu-id="25f75-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f75-192">Requirement</span></span> | <span data-ttu-id="25f75-193">Valor</span><span class="sxs-lookup"><span data-stu-id="25f75-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25f75-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25f75-194">Minimum supported client</span></span><br/> | <span data-ttu-id="25f75-195">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="25f75-195">None supported</span></span><br/>                            |
| <span data-ttu-id="25f75-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25f75-196">Minimum supported server</span></span><br/> | <span data-ttu-id="25f75-197">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25f75-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25f75-198">Consulte também</span><span class="sxs-lookup"><span data-stu-id="25f75-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f75-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="25f75-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




