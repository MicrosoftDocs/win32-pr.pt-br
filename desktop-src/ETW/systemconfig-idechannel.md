---
description: Essa classe é a classe de tipo de evento para eventos de canal do IDE. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Classe SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501765"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="87568-104">\_Classe SystemConfig IDEChannel</span><span class="sxs-lookup"><span data-stu-id="87568-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="87568-105">Essa classe é a classe de tipo de evento para eventos de canal do IDE.</span><span class="sxs-lookup"><span data-stu-id="87568-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="87568-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="87568-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87568-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87568-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="87568-108">Membros</span><span class="sxs-lookup"><span data-stu-id="87568-108">Members</span></span>

<span data-ttu-id="87568-109">A classe **SystemConfig \_ IDEChannel** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="87568-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="87568-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87568-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87568-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="87568-111">Properties</span></span>

<span data-ttu-id="87568-112">A classe **SystemConfig \_ IDEChannel** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="87568-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87568-113">**DeviceTimingMode**</span><span class="sxs-lookup"><span data-stu-id="87568-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87568-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87568-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87568-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87568-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87568-116">Qualificadores: WmiDataId (3), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="87568-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="87568-117">O modo no qual o IDE pode funcionar.</span><span class="sxs-lookup"><span data-stu-id="87568-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="87568-118">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="87568-118">The following are the possible values:</span></span>

-   <span data-ttu-id="87568-119">PIO \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="87568-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="87568-120">PIO \_ mode1 (0x2)</span><span class="sxs-lookup"><span data-stu-id="87568-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="87568-121">PIO \_ Mode2 (0x4)</span><span class="sxs-lookup"><span data-stu-id="87568-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="87568-122">PIO \_ MODE3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="87568-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="87568-123">PIO \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="87568-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="87568-124">SWDMA \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="87568-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="87568-125">SWDMA \_ mode1 (0x40)</span><span class="sxs-lookup"><span data-stu-id="87568-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="87568-126">SWDMA \_ Mode2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="87568-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="87568-127">MWDMA \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="87568-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="87568-128">MWDMA \_ Mode2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="87568-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="87568-129">MWDMA \_ MODE3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="87568-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="87568-130">UDMA \_ MODE0 (0x800)</span><span class="sxs-lookup"><span data-stu-id="87568-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="87568-131">UDMA \_ mode1 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="87568-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="87568-132">UDMA \_ Mode2 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="87568-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="87568-133">UDMA \_ MODE3 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="87568-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="87568-134">UDMA \_ MODE4 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="87568-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="87568-135">UDMA \_ MODE5 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="87568-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="87568-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="87568-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87568-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87568-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87568-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87568-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87568-139">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="87568-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="87568-140">O tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87568-140">The device type.</span></span> <span data-ttu-id="87568-141">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="87568-141">The following are the possible values:</span></span>

-   <span data-ttu-id="87568-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="87568-142">ATA (1)</span></span>
-   <span data-ttu-id="87568-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="87568-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="87568-144">**LocationInformation**</span><span class="sxs-lookup"><span data-stu-id="87568-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87568-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="87568-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87568-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87568-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87568-147">Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="87568-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="87568-148">O canal IDE (por exemplo, canal primário, canal secundário e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="87568-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="87568-149">**LocationInformationLen**</span><span class="sxs-lookup"><span data-stu-id="87568-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87568-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87568-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87568-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87568-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87568-152">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="87568-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="87568-153">Comprimento da cadeia de caracteres **LocationInformation** .</span><span class="sxs-lookup"><span data-stu-id="87568-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="87568-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="87568-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87568-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87568-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87568-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="87568-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87568-157">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="87568-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="87568-158">O identificador do disco.</span><span class="sxs-lookup"><span data-stu-id="87568-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87568-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87568-159">Requirements</span></span>



| <span data-ttu-id="87568-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="87568-160">Requirement</span></span> | <span data-ttu-id="87568-161">Valor</span><span class="sxs-lookup"><span data-stu-id="87568-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87568-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87568-162">Minimum supported client</span></span><br/> | <span data-ttu-id="87568-163">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87568-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87568-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87568-164">Minimum supported server</span></span><br/> | <span data-ttu-id="87568-165">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87568-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87568-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="87568-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87568-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="87568-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




