---
description: A \_ classe HWConfig PhyDisk é a classe de tipo de evento para eventos de configuração de disco físico. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Classe HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967426"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="64952-104">\_Classe HWConfig PhyDisk</span><span class="sxs-lookup"><span data-stu-id="64952-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="64952-105">A classe **HWConfig \_ PhyDisk** é a classe de tipo de evento para eventos de configuração de disco físico.</span><span class="sxs-lookup"><span data-stu-id="64952-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="64952-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="64952-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="64952-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64952-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="64952-108">Membros</span><span class="sxs-lookup"><span data-stu-id="64952-108">Members</span></span>

<span data-ttu-id="64952-109">A classe **HWConfig \_ PhyDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="64952-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="64952-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64952-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64952-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64952-111">Properties</span></span>

<span data-ttu-id="64952-112">A classe **HWConfig \_ PhyDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="64952-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64952-113">BytesPerSector</span><span class="sxs-lookup"><span data-stu-id="64952-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-116">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="64952-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="64952-117">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="64952-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="64952-118">Cilindros</span><span class="sxs-lookup"><span data-stu-id="64952-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-119">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="64952-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="64952-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-121">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="64952-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="64952-122">Número total de cilindros na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="64952-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="64952-123">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="64952-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="64952-124">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="64952-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="64952-125">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="64952-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="64952-126">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="64952-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-129">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="64952-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="64952-130">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="64952-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="64952-131">Fabricante</span><span class="sxs-lookup"><span data-stu-id="64952-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="64952-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64952-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-134">Qualificadores: WmiDataId (10), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="64952-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="64952-135">Nome do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="64952-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="64952-136">SCSILun</span><span class="sxs-lookup"><span data-stu-id="64952-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-139">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="64952-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="64952-140">LUN (número de unidade lógica) SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="64952-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64952-141">SCSIPath</span><span class="sxs-lookup"><span data-stu-id="64952-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-144">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="64952-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="64952-145">Número do barramento SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="64952-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64952-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="64952-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-149">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="64952-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="64952-150">Número de SCSI do adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="64952-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64952-151">SCSITarget</span><span class="sxs-lookup"><span data-stu-id="64952-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-154">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="64952-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="64952-155">Contém o número do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="64952-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="64952-156">SectorsPerTrack</span><span class="sxs-lookup"><span data-stu-id="64952-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-159">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="64952-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="64952-160">Número de setores em cada faixa para esta unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="64952-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="64952-161">TrackPerCylinder</span><span class="sxs-lookup"><span data-stu-id="64952-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64952-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64952-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64952-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64952-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64952-164">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="64952-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="64952-165">Número de faixas em cada cilindro na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="64952-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="64952-166">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="64952-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="64952-167">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="64952-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="64952-168">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="64952-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64952-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64952-169">Requirements</span></span>



| <span data-ttu-id="64952-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="64952-170">Requirement</span></span> | <span data-ttu-id="64952-171">Valor</span><span class="sxs-lookup"><span data-stu-id="64952-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="64952-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64952-172">Minimum supported client</span></span><br/> | <span data-ttu-id="64952-173">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="64952-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="64952-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64952-174">Minimum supported server</span></span><br/> | <span data-ttu-id="64952-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="64952-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="64952-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="64952-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64952-177">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="64952-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




