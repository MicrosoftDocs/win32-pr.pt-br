---
description: Classe SystemConfig_V0_PhyDisk-essa classe é a classe de tipo de evento para eventos de configuração de disco físico.
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Classe SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105954"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="cce9b-103">\_Classe SystemConfig V0 \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="cce9b-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="cce9b-104">Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cce9b-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="cce9b-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="cce9b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce9b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cce9b-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="cce9b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cce9b-107">Members</span></span>

<span data-ttu-id="cce9b-108">A classe **SystemConfig \_ V0 \_ PhyDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cce9b-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="cce9b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cce9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cce9b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cce9b-110">Properties</span></span>

<span data-ttu-id="cce9b-111">A classe **SystemConfig \_ V0 \_ PhyDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cce9b-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cce9b-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="cce9b-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-113">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="cce9b-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-115">Qualificadores: **WmiDataId** (13), **máx** . (3)</span><span class="sxs-lookup"><span data-stu-id="cce9b-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-116">Letra da unidade da unidade de inicialização no formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="cce9b-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="cce9b-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-120">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="cce9b-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-121">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cce9b-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="cce9b-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cce9b-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-125">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="cce9b-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-126">Número total de cilindros na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cce9b-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="cce9b-127">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="cce9b-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="cce9b-128">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="cce9b-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="cce9b-129">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="cce9b-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="cce9b-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-133">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="cce9b-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-134">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="cce9b-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="cce9b-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-136">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="cce9b-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-138">Qualificadores: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="cce9b-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-139">Nome do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="cce9b-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="cce9b-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-143">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="cce9b-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-144">Número de partições nesta unidade de disco físico que são reconhecidas pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cce9b-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="cce9b-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-148">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="cce9b-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-149">LUN (número de unidade lógica) SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="cce9b-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="cce9b-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-153">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="cce9b-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-154">Número do barramento SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="cce9b-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="cce9b-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-158">Qualificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="cce9b-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-159">Número de SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="cce9b-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="cce9b-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-163">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="cce9b-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-164">Contém o número do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="cce9b-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="cce9b-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-168">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="cce9b-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-169">Número de setores em cada faixa para esta unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cce9b-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-170">**TrackPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="cce9b-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cce9b-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-173">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="cce9b-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-174">Número de faixas em cada cilindro na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cce9b-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="cce9b-175">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="cce9b-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="cce9b-176">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="cce9b-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="cce9b-177">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="cce9b-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="cce9b-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="cce9b-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce9b-179">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cce9b-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cce9b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce9b-181">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="cce9b-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="cce9b-182">True se o cache de gravação estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="cce9b-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cce9b-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce9b-183">Requirements</span></span>



| <span data-ttu-id="cce9b-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce9b-184">Requirement</span></span> | <span data-ttu-id="cce9b-185">Valor</span><span class="sxs-lookup"><span data-stu-id="cce9b-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cce9b-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce9b-186">Minimum supported client</span></span><br/> | <span data-ttu-id="cce9b-187">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cce9b-187">None supported</span></span><br/>                            |
| <span data-ttu-id="cce9b-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce9b-188">Minimum supported server</span></span><br/> | <span data-ttu-id="cce9b-189">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cce9b-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cce9b-190">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cce9b-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce9b-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="cce9b-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




