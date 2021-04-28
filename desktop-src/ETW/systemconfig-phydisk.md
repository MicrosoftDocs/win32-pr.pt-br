---
description: Classe SystemConfig_PhyDisk-essa classe é a classe de tipo de evento para eventos de configuração de disco físico.
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
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106094"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="c7296-103">\_Classe SystemConfig PhyDisk</span><span class="sxs-lookup"><span data-stu-id="c7296-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="c7296-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="c7296-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="c7296-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c7296-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7296-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7296-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c7296-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7296-107">Members</span></span>

<span data-ttu-id="c7296-108">A classe **SystemConfig \_ PhyDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7296-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="c7296-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7296-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7296-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7296-110">Properties</span></span>

<span data-ttu-id="c7296-111">A classe **SystemConfig \_ PhyDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7296-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7296-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="c7296-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-113">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="c7296-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7296-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-115">Qualificadores: **WmiDataId** (14), **Max** (3), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="c7296-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c7296-116">Letra da unidade da unidade de inicialização no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="c7296-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="c7296-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="c7296-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-120">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="c7296-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-121">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="c7296-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="c7296-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7296-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-125">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="c7296-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-126">Número total de cilindros na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="c7296-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="c7296-127">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="c7296-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="c7296-128">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="c7296-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="c7296-129">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="c7296-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="c7296-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-133">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="c7296-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-134">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="c7296-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c7296-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-136">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="c7296-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7296-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-138">Qualificadores: **WmiDataId** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="c7296-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c7296-139">Nome do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="c7296-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-140">**Bloco**</span><span class="sxs-lookup"><span data-stu-id="c7296-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-141">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c7296-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-143">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="c7296-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-144">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c7296-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="c7296-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-148">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="c7296-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-149">Número de partições nesta unidade de disco físico que são reconhecidas pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c7296-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="c7296-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-153">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="c7296-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-154">LUN (número de unidade lógica) SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="c7296-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="c7296-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-158">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="c7296-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-159">Número do barramento SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="c7296-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="c7296-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-163">Qualificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="c7296-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-164">Número de SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="c7296-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="c7296-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-168">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="c7296-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-169">Contém o número do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c7296-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="c7296-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-173">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="c7296-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-174">Número de setores em cada faixa para esta unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="c7296-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-175">**Livre**</span><span class="sxs-lookup"><span data-stu-id="c7296-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-176">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="c7296-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7296-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-178">Qualificadores: **WmiDataId** (15), **Max** (2), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="c7296-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c7296-179">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c7296-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-180">**TrackPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="c7296-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7296-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-183">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="c7296-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-184">Número de faixas em cada cilindro na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="c7296-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="c7296-185">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="c7296-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="c7296-186">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="c7296-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="c7296-187">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="c7296-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="c7296-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="c7296-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7296-189">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c7296-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c7296-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7296-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7296-191">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="c7296-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="c7296-192">True se o cache de gravação estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c7296-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7296-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7296-193">Requirements</span></span>



| <span data-ttu-id="c7296-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7296-194">Requirement</span></span> | <span data-ttu-id="c7296-195">Valor</span><span class="sxs-lookup"><span data-stu-id="c7296-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7296-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7296-196">Minimum supported client</span></span><br/> | <span data-ttu-id="c7296-197">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7296-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c7296-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7296-198">Minimum supported server</span></span><br/> | <span data-ttu-id="c7296-199">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7296-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7296-200">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c7296-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7296-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c7296-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




