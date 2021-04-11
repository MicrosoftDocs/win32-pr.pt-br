---
description: A \_ classe CIM MemoryCapacity representa a memória que pode ser instalada em um elemento físico e suas configurações mínimas e máximas.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: Classe CIM_MemoryCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163942"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="63888-103">\_Classe CIM MemoryCapacity</span><span class="sxs-lookup"><span data-stu-id="63888-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="63888-104">A classe **CIM \_ MemoryCapacity** representa a memória que pode ser instalada em um elemento físico e suas configurações mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="63888-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="63888-105">Informações sobre a memória que está atualmente instalada e os requisitos mínimos e máximos de um elemento estão localizados em instâncias da classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="63888-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63888-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="63888-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63888-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63888-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63888-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="63888-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="63888-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="63888-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63888-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63888-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="63888-111">Membros</span><span class="sxs-lookup"><span data-stu-id="63888-111">Members</span></span>

<span data-ttu-id="63888-112">A classe **CIM \_ MemoryCapacity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="63888-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="63888-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63888-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63888-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63888-114">Properties</span></span>

<span data-ttu-id="63888-115">A classe **CIM \_ MemoryCapacity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63888-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63888-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="63888-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63888-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63888-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63888-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="63888-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="63888-120">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="63888-120">Short textual description of the object.</span></span>

<span data-ttu-id="63888-121">Essa propriedade é herdada do [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="63888-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="63888-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63888-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63888-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63888-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63888-125">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="63888-125">Textual description of the object.</span></span>

<span data-ttu-id="63888-126">Essa propriedade é herdada do [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="63888-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="63888-127">**MaximumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="63888-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63888-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63888-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63888-130">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="63888-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="63888-131">Quantidade máxima de memória, em quilobytes, que pode ser suportada pelo elemento físico associado.</span><span class="sxs-lookup"><span data-stu-id="63888-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="63888-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63888-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63888-133">**Memorytype**</span><span class="sxs-lookup"><span data-stu-id="63888-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63888-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63888-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63888-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMemory**](cim-physicalmemory.md).**Memorytype**")</span><span class="sxs-lookup"><span data-stu-id="63888-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="63888-137">Tipo de memória, que faz parte da chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="63888-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="63888-138">Os valores correspondem à lista de possíveis tipos de memória na classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="63888-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63888-139">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="63888-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63888-140">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="63888-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="63888-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="63888-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="63888-142">**DRAM síncrona** (3)</span><span class="sxs-lookup"><span data-stu-id="63888-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="63888-143">**DRAM de cache** (4)</span><span class="sxs-lookup"><span data-stu-id="63888-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="63888-144">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="63888-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="63888-145">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="63888-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="63888-146">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="63888-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="63888-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="63888-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="63888-148">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="63888-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="63888-149">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="63888-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="63888-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="63888-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="63888-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="63888-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="63888-152">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="63888-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="63888-153">**(14** )</span><span class="sxs-lookup"><span data-stu-id="63888-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="63888-154">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="63888-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="63888-155">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="63888-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="63888-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="63888-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="63888-157">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="63888-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="63888-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="63888-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="63888-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="63888-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="63888-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="63888-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63888-161">**MinimumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="63888-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-162">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63888-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63888-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63888-164">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="63888-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="63888-165">Quantidade mínima de memória, em quilobytes, necessária para que o elemento físico associado opere corretamente.</span><span class="sxs-lookup"><span data-stu-id="63888-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="63888-166">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63888-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63888-167">**Nome**</span><span class="sxs-lookup"><span data-stu-id="63888-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63888-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63888-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63888-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63888-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63888-170">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63888-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63888-171">O nome do objeto; serve como parte da chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="63888-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63888-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="63888-172">Remarks</span></span>

<span data-ttu-id="63888-173">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="63888-173">WMI does not implement this class.</span></span>

<span data-ttu-id="63888-174">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="63888-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63888-175">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="63888-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63888-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63888-176">Requirements</span></span>



| <span data-ttu-id="63888-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="63888-177">Requirement</span></span> | <span data-ttu-id="63888-178">Valor</span><span class="sxs-lookup"><span data-stu-id="63888-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63888-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63888-179">Minimum supported client</span></span><br/> | <span data-ttu-id="63888-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63888-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63888-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63888-181">Minimum supported server</span></span><br/> | <span data-ttu-id="63888-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63888-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63888-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="63888-183">Namespace</span></span><br/>                | <span data-ttu-id="63888-184">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="63888-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63888-185">MOF</span><span class="sxs-lookup"><span data-stu-id="63888-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63888-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63888-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63888-187">DLL</span><span class="sxs-lookup"><span data-stu-id="63888-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63888-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63888-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63888-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="63888-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63888-190">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="63888-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

