---
description: Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: Classe SystemConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967382"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="8d0df-103">\_Classe SystemConfig PhyDisk</span><span class="sxs-lookup"><span data-stu-id="8d0df-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="8d0df-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8d0df-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="8d0df-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="8d0df-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0df-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d0df-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="8d0df-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8d0df-107">Members</span></span>

<span data-ttu-id="8d0df-108">A classe **SystemConfig \_ PhyDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8d0df-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="8d0df-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d0df-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d0df-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d0df-110">Properties</span></span>

<span data-ttu-id="8d0df-111">A classe **SystemConfig \_ PhyDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d0df-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d0df-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="8d0df-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-113">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="8d0df-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-115">Qualificadores: **WmiDataId** (14), **Max** (3), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="8d0df-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-116">Letra da unidade da unidade de inicialização no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="8d0df-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="8d0df-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-120">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="8d0df-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-121">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8d0df-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="8d0df-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d0df-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-125">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="8d0df-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-126">Número total de cilindros na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8d0df-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="8d0df-127">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="8d0df-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="8d0df-128">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="8d0df-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="8d0df-129">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="8d0df-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="8d0df-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-133">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="8d0df-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-134">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="8d0df-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="8d0df-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-136">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="8d0df-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-138">Qualificadores: **WmiDataId** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="8d0df-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-139">Nome do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="8d0df-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-140">**Bloco**</span><span class="sxs-lookup"><span data-stu-id="8d0df-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-141">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="8d0df-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-143">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="8d0df-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-144">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8d0df-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="8d0df-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-148">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="8d0df-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-149">Número de partições nesta unidade de disco físico que são reconhecidas pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8d0df-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="8d0df-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-153">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="8d0df-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-154">LUN (número de unidade lógica) SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="8d0df-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="8d0df-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-158">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="8d0df-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-159">Número do barramento SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="8d0df-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="8d0df-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-163">Qualificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="8d0df-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-164">Número de SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="8d0df-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="8d0df-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-168">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="8d0df-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-169">Contém o número do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="8d0df-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="8d0df-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-173">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="8d0df-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-174">Número de setores em cada faixa para esta unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8d0df-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-175">**Livre**</span><span class="sxs-lookup"><span data-stu-id="8d0df-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-176">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="8d0df-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-178">Qualificadores: **WmiDataId** (15), **Max** (2), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="8d0df-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-179">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8d0df-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-180">**TrackPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="8d0df-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0df-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-183">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="8d0df-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-184">Número de faixas em cada cilindro na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8d0df-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="8d0df-185">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="8d0df-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="8d0df-186">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="8d0df-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="8d0df-187">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="8d0df-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="8d0df-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="8d0df-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0df-189">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="8d0df-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d0df-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0df-191">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="8d0df-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="8d0df-192">True se o cache de gravação estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="8d0df-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d0df-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d0df-193">Requirements</span></span>



| <span data-ttu-id="8d0df-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d0df-194">Requirement</span></span> | <span data-ttu-id="8d0df-195">Valor</span><span class="sxs-lookup"><span data-stu-id="8d0df-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8d0df-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d0df-196">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0df-197">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d0df-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8d0df-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d0df-198">Minimum supported server</span></span><br/> | <span data-ttu-id="8d0df-199">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d0df-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d0df-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d0df-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0df-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8d0df-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




