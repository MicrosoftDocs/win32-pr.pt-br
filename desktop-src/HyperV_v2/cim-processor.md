---
description: Representa os recursos e o gerenciamento de um processador.
ms.assetid: 70cf9776-eeda-42c2-90c4-704ecf1cdafe
title: Classe CIM_Processor (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.Role
- CIM_Processor.Family
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.UpgradeMethod
- CIM_Processor.MaxClockSpeed
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.AddressWidth
- CIM_Processor.LoadPercentage
- CIM_Processor.Stepping
- CIM_Processor.UniqueID
- CIM_Processor.CPUStatus
- CIM_Processor.ExternalBusClockSpeed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00e78834c0a3a782c5fdc48cd52a67b85aa2a241
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646685"
---
# <a name="cim_processor-class-hyper-v-management"></a><span data-ttu-id="776cd-103">Classe CIM_Processor (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="776cd-103">CIM_Processor class (Hyper-V management)</span></span>

<span data-ttu-id="776cd-104">Representa os recursos e o gerenciamento de um processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-104">Represents the capabilities and management of a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="776cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="776cd-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.1"), UMLPackagePath("CIM::Device::Processor"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  string Role;
  uint16 Family;
  string OtherFamilyDescription;
  uint16 UpgradeMethod;
  uint32 MaxClockSpeed;
  uint32 CurrentClockSpeed;
  uint16 DataWidth;
  uint16 AddressWidth;
  uint16 LoadPercentage;
  string Stepping;
  string UniqueID;
  uint16 CPUStatus;
  uint32 ExternalBusClockSpeed;
};
```

## <a name="members"></a><span data-ttu-id="776cd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="776cd-106">Members</span></span>

<span data-ttu-id="776cd-107">A classe de **\_ processador CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="776cd-107">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="776cd-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="776cd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="776cd-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="776cd-109">Properties</span></span>

<span data-ttu-id="776cd-110">A classe de **\_ processador CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="776cd-110">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="776cd-111">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="776cd-111">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-114">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), **PUnit** ("bit")</span><span class="sxs-lookup"><span data-stu-id="776cd-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-115">A largura do endereço do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="776cd-115">The processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-116">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="776cd-116">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776cd-119">O status atual do processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-119">The current status of the processor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="776cd-120">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="776cd-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Enabled"></span><span id="cpu_enabled"></span><span id="CPU_ENABLED"></span>

<span data-ttu-id="776cd-121">**CPU habilitada** (1)</span><span class="sxs-lookup"><span data-stu-id="776cd-121">**CPU Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_by_User"></span><span id="cpu_disabled_by_user"></span><span id="CPU_DISABLED_BY_USER"></span>

<span data-ttu-id="776cd-122">**CPU desabilitada pelo usuário** (2)</span><span class="sxs-lookup"><span data-stu-id="776cd-122">**CPU Disabled by User** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_By_BIOS__POST_Error_"></span><span id="cpu_disabled_by_bios__post_error_"></span><span id="CPU_DISABLED_BY_BIOS__POST_ERROR_"></span>

<span data-ttu-id="776cd-123">**CPU desabilitada pelo BIOS (erro post)** (3)</span><span class="sxs-lookup"><span data-stu-id="776cd-123">**CPU Disabled By BIOS (POST Error)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Is_Idle"></span><span id="cpu_is_idle"></span><span id="CPU_IS_IDLE"></span>

<span data-ttu-id="776cd-124">A **CPU está ociosa** (4)</span><span class="sxs-lookup"><span data-stu-id="776cd-124">**CPU Is Idle** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="776cd-125">**Outro** (7)</span><span class="sxs-lookup"><span data-stu-id="776cd-125">**Other** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="776cd-126">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="776cd-126">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="776cd-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-129">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 17,6 "), **PUnit** (" Hertz \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="776cd-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.6"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-130">A velocidade atual, em MHz, do processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-130">The current speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-131">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="776cd-131">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-134">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), **PUnit** ("bit")</span><span class="sxs-lookup"><span data-stu-id="776cd-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-135">A largura dos dados do processador, em bits.</span><span class="sxs-lookup"><span data-stu-id="776cd-135">The processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-136">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="776cd-136">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="776cd-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-139">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz"), **PUnit** ("Hertz \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="776cd-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-140">A velocidade, em MHz, da interface de barramento externa (também conhecida como o barramento frontal).</span><span class="sxs-lookup"><span data-stu-id="776cd-140">The speed, in MHz, of the external bus interface (also known as the front side bus).</span></span>

</dd> <dt>

<span data-ttu-id="776cd-141">**Família**</span><span class="sxs-lookup"><span data-stu-id="776cd-141">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 17,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="776cd-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-145">O tipo de família do processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-145">The processor family type.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="776cd-146">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="776cd-146">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="776cd-147">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="776cd-147">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="776cd-148">**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="776cd-148">**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="776cd-149">**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="776cd-149">**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="776cd-150">**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="776cd-150">**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="776cd-151">**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="776cd-151">**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="776cd-152">**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="776cd-152">**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="776cd-153">**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="776cd-153">**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="776cd-154">**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="776cd-154">**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="776cd-155">**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="776cd-155">**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="776cd-156">**Marca Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="776cd-156">**Pentium(R) brand** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="776cd-157">**Pentium (R) pro** (12)</span><span class="sxs-lookup"><span data-stu-id="776cd-157">**Pentium(R) Pro** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="776cd-158">**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="776cd-158">**Pentium(R) II** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="776cd-159">**Processador Pentium (R) com tecnologia MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="776cd-159">**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="776cd-160">**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="776cd-160">**Celeron(TM)** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="776cd-161">**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="776cd-161">**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="776cd-162">**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="776cd-162">**Pentium(R) III** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="776cd-163">**Família M1** (18)</span><span class="sxs-lookup"><span data-stu-id="776cd-163">**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="776cd-164">**Família m2** (19)</span><span class="sxs-lookup"><span data-stu-id="776cd-164">**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__M_processor"></span><span id="intel_r__celeron_r__m_processor"></span><span id="INTEL_R__CELERON_R__M_PROCESSOR"></span>

<span data-ttu-id="776cd-165">**Processador Intel (r) Celeron (r) M** (20)</span><span class="sxs-lookup"><span data-stu-id="776cd-165">**Intel(R) Celeron(R) M processor** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__4_HT_processor"></span><span id="intel_r__pentium_r__4_ht_processor"></span><span id="INTEL_R__PENTIUM_R__4_HT_PROCESSOR"></span>

<span data-ttu-id="776cd-166">**Processador Intel (r) Pentium (r) 4 HT** (21)</span><span class="sxs-lookup"><span data-stu-id="776cd-166">**Intel(R) Pentium(R) 4 HT processor** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="776cd-167">**Família K5** (24)</span><span class="sxs-lookup"><span data-stu-id="776cd-167">**K5 Family** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="776cd-168">**Família K6** (25)</span><span class="sxs-lookup"><span data-stu-id="776cd-168">**K6 Family** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="776cd-169">**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="776cd-169">**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="776cd-170">**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="776cd-170">**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-171">**Família de processadores AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="776cd-171">**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="776cd-172">**Processador AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="776cd-172">**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="776cd-173">**Família AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="776cd-173">**AMD29000 Family** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="776cd-174">**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="776cd-174">**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="776cd-175">**Família Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="776cd-175">**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="776cd-176">**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="776cd-176">**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="776cd-177">**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="776cd-177">**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="776cd-178">**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="776cd-178">**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="776cd-179">**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="776cd-179">**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="776cd-180">**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="776cd-180">**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="776cd-181">**X704 do Power PC** (38)</span><span class="sxs-lookup"><span data-stu-id="776cd-181">**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="776cd-182">**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="776cd-182">**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_processor"></span><span id="intel_r__core_tm__duo_processor"></span><span id="INTEL_R__CORE_TM__DUO_PROCESSOR"></span>

<span data-ttu-id="776cd-183">**Processador Intel (R) Core (TM) Duo** (40)</span><span class="sxs-lookup"><span data-stu-id="776cd-183">**Intel(R) Core(TM) Duo processor** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_mobile_processor"></span><span id="intel_r__core_tm__duo_mobile_processor"></span><span id="INTEL_R__CORE_TM__DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="776cd-184">**Processador móvel Intel (R) Core (TM) Duo** (41)</span><span class="sxs-lookup"><span data-stu-id="776cd-184">**Intel(R) Core(TM) Duo mobile processor** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_mobile_processor"></span><span id="intel_r__core_tm__solo_mobile_processor"></span><span id="INTEL_R__CORE_TM__SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="776cd-185">**Processador móvel Intel (R) Core (TM) solo** (42)</span><span class="sxs-lookup"><span data-stu-id="776cd-185">**Intel(R) Core(TM) Solo mobile processor** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Atom_TM__processor"></span><span id="intel_r__atom_tm__processor"></span><span id="INTEL_R__ATOM_TM__PROCESSOR"></span>

<span data-ttu-id="776cd-186">**Processador Intel (R) Atom (TM)** (43)</span><span class="sxs-lookup"><span data-stu-id="776cd-186">**Intel(R) Atom(TM) processor** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="776cd-187">**Família alfa** (48)</span><span class="sxs-lookup"><span data-stu-id="776cd-187">**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="776cd-188">**Alfa 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="776cd-188">**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="776cd-189">**Alfa 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="776cd-189">**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="776cd-190">**Alfa 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="776cd-190">**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="776cd-191">**21164PC alfa** (52)</span><span class="sxs-lookup"><span data-stu-id="776cd-191">**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="776cd-192">**21164A alfa** (53)</span><span class="sxs-lookup"><span data-stu-id="776cd-192">**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="776cd-193">**Alfa 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="776cd-193">**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="776cd-194">**Alfa 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="776cd-194">**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Ultra_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_ultra_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_ULTRA_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-195">**Família de processadores AMD Turion (TM) II Ultra Dual-Core Mobile M** (56)</span><span class="sxs-lookup"><span data-stu-id="776cd-195">**AMD Turion(TM) II Ultra Dual-Core Mobile M Processor Family** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-196">**Família de processadores AMD Turion (TM) II Dual-Core Mobile M** (57)</span><span class="sxs-lookup"><span data-stu-id="776cd-196">**AMD Turion(TM) II Dual-Core Mobile M Processor Family** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_athlon_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_ATHLON_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-197">**Família de processadores AMD Athlon (TM) II Dual-Core Mobile M** (58)</span><span class="sxs-lookup"><span data-stu-id="776cd-197">**AMD Athlon(TM) II Dual-Core Mobile M Processor Family** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__6100_Series_Processor"></span><span id="amd_opteron_tm__6100_series_processor"></span><span id="AMD_OPTERON_TM__6100_SERIES_PROCESSOR"></span>

<span data-ttu-id="776cd-198">**Processador AMD Opteron (TM) 6100 Series** (59)</span><span class="sxs-lookup"><span data-stu-id="776cd-198">**AMD Opteron(TM) 6100 Series Processor** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__4100_Series_Processor"></span><span id="amd_opteron_tm__4100_series_processor"></span><span id="AMD_OPTERON_TM__4100_SERIES_PROCESSOR"></span>

<span data-ttu-id="776cd-199">**Processador AMD Opteron (TM) 4100 Series** (60)</span><span class="sxs-lookup"><span data-stu-id="776cd-199">**AMD Opteron(TM) 4100 Series Processor** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="776cd-200">**Família MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="776cd-200">**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="776cd-201">**MIPS R4000** (65)</span><span class="sxs-lookup"><span data-stu-id="776cd-201">**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="776cd-202">**MIPS R4200** (66)</span><span class="sxs-lookup"><span data-stu-id="776cd-202">**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="776cd-203">**MIPS R4400** (67)</span><span class="sxs-lookup"><span data-stu-id="776cd-203">**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="776cd-204">**MIPS R4600** (68)</span><span class="sxs-lookup"><span data-stu-id="776cd-204">**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="776cd-205">**MIPS R10000** (69)</span><span class="sxs-lookup"><span data-stu-id="776cd-205">**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="776cd-206">**Família SPARC** (80)</span><span class="sxs-lookup"><span data-stu-id="776cd-206">**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="776cd-207">**Supersparc** (81)</span><span class="sxs-lookup"><span data-stu-id="776cd-207">**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="776cd-208">**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="776cd-208">**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="776cd-209">**IIep de microsparc** (83)</span><span class="sxs-lookup"><span data-stu-id="776cd-209">**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="776cd-210">**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="776cd-210">**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="776cd-211">**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="776cd-211">**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="776cd-212">**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="776cd-212">**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="776cd-213">**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="776cd-213">**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="776cd-214">**UltraSPARC iiii** (88)</span><span class="sxs-lookup"><span data-stu-id="776cd-214">**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="776cd-215">**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="776cd-215">**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="776cd-216">**família 68XXX** (97)</span><span class="sxs-lookup"><span data-stu-id="776cd-216">**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="776cd-217">**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="776cd-217">**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="776cd-218">**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="776cd-218">**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="776cd-219">**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="776cd-219">**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="776cd-220">**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="776cd-220">**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="776cd-221">**Família Hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="776cd-221">**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="776cd-222">**Crusoe (TM) TM5000 Family** (120)</span><span class="sxs-lookup"><span data-stu-id="776cd-222">**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="776cd-223">**Crusoe (TM) TM3000 Family** (121)</span><span class="sxs-lookup"><span data-stu-id="776cd-223">**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="776cd-224">**Efficeon (TM) TM8000 Family** (122)</span><span class="sxs-lookup"><span data-stu-id="776cd-224">**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="776cd-225">**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="776cd-225">**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="776cd-226">**Processador Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="776cd-226">**Itanium(TM) Processor** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-227">**Família de processadores AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="776cd-227">**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__Processor_Family"></span><span id="amd_opteron_tm__processor_family"></span><span id="AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-228">**Família de processadores AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="776cd-228">**AMD Opteron(TM) Processor Family** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__Processor_Family"></span><span id="amd_sempron_tm__processor_family"></span><span id="AMD_SEMPRON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-229">**Família de processadores AMD Sempron (TM)** (133)</span><span class="sxs-lookup"><span data-stu-id="776cd-229">**AMD Sempron(TM) Processor Family** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_Mobile_Technology"></span><span id="amd_turion_tm__64_mobile_technology"></span><span id="AMD_TURION_TM__64_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="776cd-230">**Tecnologia móvel AMD Turion (TM) 64** (134)</span><span class="sxs-lookup"><span data-stu-id="776cd-230">**AMD Turion(TM) 64 Mobile Technology** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_AMD_Opteron_TM__Processor_Family"></span><span id="dual-core_amd_opteron_tm__processor_family"></span><span id="DUAL-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-231">**Família de processadores dual-core AMD Opteron (TM)** (135)</span><span class="sxs-lookup"><span data-stu-id="776cd-231">**Dual-Core AMD Opteron(TM) Processor Family** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__64_x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__64_X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-232">**Família de processadores AMD Athlon (TM) 64 X2 Dual-Core** (136)</span><span class="sxs-lookup"><span data-stu-id="776cd-232">**AMD Athlon(TM) 64 X2 Dual-Core Processor Family** (136)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_X2_Mobile_Technology"></span><span id="amd_turion_tm__64_x2_mobile_technology"></span><span id="AMD_TURION_TM__64_X2_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="776cd-233">**Tecnologia móvel AMD Turion (TM) 64 X2** (137)</span><span class="sxs-lookup"><span data-stu-id="776cd-233">**AMD Turion(TM) 64 X2 Mobile Technology** (137)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_AMD_Opteron_TM__Processor_Family"></span><span id="quad-core_amd_opteron_tm__processor_family"></span><span id="QUAD-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-234">**Família de processadores quad-core AMD Opteron (TM)** (138)</span><span class="sxs-lookup"><span data-stu-id="776cd-234">**Quad-Core AMD Opteron(TM) Processor Family** (138)</span></span>


</dt> <dd></dd> <dt>

<span id="Third-Generation_AMD_Opteron_TM__Processor_Family"></span><span id="third-generation_amd_opteron_tm__processor_family"></span><span id="THIRD-GENERATION_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-235">**Família de processadores AMD Opteron (TM) de terceira geração** (139)</span><span class="sxs-lookup"><span data-stu-id="776cd-235">**Third-Generation AMD Opteron(TM) Processor Family** (139)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__FX_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__fx_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__FX_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-236">**AMD Phenom (TM) FX Quad-Core família de processadores** (140)</span><span class="sxs-lookup"><span data-stu-id="776cd-236">**AMD Phenom(TM) FX Quad-Core Processor Family** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X4_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__x4_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__X4_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-237">**Família de processadores AMD Phenom (TM) X4 Quad-Core** (141)</span><span class="sxs-lookup"><span data-stu-id="776cd-237">**AMD Phenom(TM) X4 Quad-Core Processor Family** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_phenom_tm__x2_dual-core_processor_family"></span><span id="AMD_PHENOM_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-238">**Família de processadores AMD Phenom (TM) X2 Dual-Core** (142)</span><span class="sxs-lookup"><span data-stu-id="776cd-238">**AMD Phenom(TM) X2 Dual-Core Processor Family** (142)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-239">**Família de processadores AMD Athlon (TM) X2 Dual-Core** (143)</span><span class="sxs-lookup"><span data-stu-id="776cd-239">**AMD Athlon(TM) X2 Dual-Core Processor Family** (143)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="776cd-240">**Família PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="776cd-240">**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="776cd-241">**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="776cd-241">**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="776cd-242">**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="776cd-242">**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="776cd-243">**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="776cd-243">**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="776cd-244">**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="776cd-244">**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="776cd-245">**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="776cd-245">**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="776cd-246">**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="776cd-246">**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="776cd-247">**Família V30** (160)</span><span class="sxs-lookup"><span data-stu-id="776cd-247">**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3200_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3200_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3200_SERIES"></span>

<span data-ttu-id="776cd-248">**Processador Quad-Core Intel (r) Xeon (r) processor 3200 série** (161)</span><span class="sxs-lookup"><span data-stu-id="776cd-248">**Quad-Core Intel(R) Xeon(R) processor 3200 Series** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3000_SERIES"></span>

<span data-ttu-id="776cd-249">**Processador dual-core Intel (r) Xeon (r) série 3000** (162)</span><span class="sxs-lookup"><span data-stu-id="776cd-249">**Dual-Core Intel(R) Xeon(R) processor 3000 Series** (162)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5300_SERIES"></span>

<span data-ttu-id="776cd-250">**Processador Quad-Core Intel (r) Xeon (r) processor 5300 série** (163)</span><span class="sxs-lookup"><span data-stu-id="776cd-250">**Quad-Core Intel(R) Xeon(R) processor 5300 Series** (163)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5100_SERIES"></span>

<span data-ttu-id="776cd-251">**Processador dual-core Intel (r) Xeon (r) série 5100** (164)</span><span class="sxs-lookup"><span data-stu-id="776cd-251">**Dual-Core Intel(R) Xeon(R) processor 5100 Series** (164)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5000_SERIES"></span>

<span data-ttu-id="776cd-252">**Processador dual-core Intel (r) Xeon (r) série 5000** (165)</span><span class="sxs-lookup"><span data-stu-id="776cd-252">**Dual-Core Intel(R) Xeon(R) processor 5000 Series** (165)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_LV"></span><span id="dual-core_intel_r__xeon_r__processor_lv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_LV"></span>

<span data-ttu-id="776cd-253">**Processador dual-core Intel (r) Xeon (r) LV** (166)</span><span class="sxs-lookup"><span data-stu-id="776cd-253">**Dual-Core Intel(R) Xeon(R) processor LV** (166)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_ULV"></span><span id="dual-core_intel_r__xeon_r__processor_ulv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_ULV"></span>

<span data-ttu-id="776cd-254">**Processador dual-core Intel (r) Xeon (r) ULV** (167)</span><span class="sxs-lookup"><span data-stu-id="776cd-254">**Dual-Core Intel(R) Xeon(R) processor ULV** (167)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7100_SERIES"></span>

<span data-ttu-id="776cd-255">**Processador dual-core Intel (r) Xeon (r) série 7100** (168)</span><span class="sxs-lookup"><span data-stu-id="776cd-255">**Dual-Core Intel(R) Xeon(R) processor 7100 Series** (168)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5400_SERIES"></span>

<span data-ttu-id="776cd-256">**Processador Quad-Core Intel (r) Xeon (r) processor 5400 série** (169)</span><span class="sxs-lookup"><span data-stu-id="776cd-256">**Quad-Core Intel(R) Xeon(R) processor 5400 Series** (169)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor"></span><span id="quad-core_intel_r__xeon_r__processor"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="776cd-257">**Processador Quad-Core Intel (r) Xeon (r)** (170)</span><span class="sxs-lookup"><span data-stu-id="776cd-257">**Quad-Core Intel(R) Xeon(R) processor** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5200_SERIES"></span>

<span data-ttu-id="776cd-258">**Processador dual-core Intel (r) Xeon (r) série 5200** (171)</span><span class="sxs-lookup"><span data-stu-id="776cd-258">**Dual-Core Intel(R) Xeon(R) processor 5200 Series** (171)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7200_SERIES"></span>

<span data-ttu-id="776cd-259">**Processador dual-core Intel (r) Xeon (r) série 7200** (172)</span><span class="sxs-lookup"><span data-stu-id="776cd-259">**Dual-Core Intel(R) Xeon(R) processor 7200 Series** (172)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7300_SERIES"></span>

<span data-ttu-id="776cd-260">**Processador Quad-Core Intel (r) Xeon (r) processor 7300 série** (173)</span><span class="sxs-lookup"><span data-stu-id="776cd-260">**Quad-Core Intel(R) Xeon(R) processor 7300 Series** (173)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="776cd-261">**Processador Quad-Core Intel (r) Xeon (r) processor 7400 série** (174)</span><span class="sxs-lookup"><span data-stu-id="776cd-261">**Quad-Core Intel(R) Xeon(R) processor 7400 Series** (174)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="776cd-262">**Processador Intel (r) Xeon (r) série 7400 de vários núcleos** (175)</span><span class="sxs-lookup"><span data-stu-id="776cd-262">**Multi-Core Intel(R) Xeon(R) processor 7400 Series** (175)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="776cd-263">**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="776cd-263">**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="776cd-264">**Processador Pentium (r) III com tecnologia Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="776cd-264">**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="776cd-265">**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="776cd-265">**Pentium(R) 4** (178)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="776cd-266">**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="776cd-266">**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd></dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="776cd-267">**Família AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="776cd-267">**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="776cd-268">**Processador Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="776cd-268">**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__XP_Family"></span><span id="amd_athlon_tm__xp_family"></span><span id="AMD_ATHLON_TM__XP_FAMILY"></span>

<span data-ttu-id="776cd-269">**Família AMD Athlon (TM) XP** (182)</span><span class="sxs-lookup"><span data-stu-id="776cd-269">**AMD Athlon(TM) XP Family** (182)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__MP_Family"></span><span id="amd_athlon_tm__mp_family"></span><span id="AMD_ATHLON_TM__MP_FAMILY"></span>

<span data-ttu-id="776cd-270">**Família de MP AMD Athlon (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="776cd-270">**AMD Athlon(TM) MP Family** (183)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="776cd-271">**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="776cd-271">**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__M_processor"></span><span id="intel_r__pentium_r__m_processor"></span><span id="INTEL_R__PENTIUM_R__M_PROCESSOR"></span>

<span data-ttu-id="776cd-272">**Processador Intel (r) Pentium (r) M** (185)</span><span class="sxs-lookup"><span data-stu-id="776cd-272">**Intel(R) Pentium(R) M processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__D_processor"></span><span id="intel_r__celeron_r__d_processor"></span><span id="INTEL_R__CELERON_R__D_PROCESSOR"></span>

<span data-ttu-id="776cd-273">**Processador Intel (r) Celeron (r) D** (186)</span><span class="sxs-lookup"><span data-stu-id="776cd-273">**Intel(R) Celeron(R) D processor** (186)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__D_processor"></span><span id="intel_r__pentium_r__d_processor"></span><span id="INTEL_R__PENTIUM_R__D_PROCESSOR"></span>

<span data-ttu-id="776cd-274">**Processador Intel (r) Pentium (r) D** (187)</span><span class="sxs-lookup"><span data-stu-id="776cd-274">**Intel(R) Pentium(R) D processor** (187)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__Processor_Extreme_Edition"></span><span id="intel_r__pentium_r__processor_extreme_edition"></span><span id="INTEL_R__PENTIUM_R__PROCESSOR_EXTREME_EDITION"></span>

<span data-ttu-id="776cd-275">**Processador Intel (r) Pentium (r) Extreme Edition** (188)</span><span class="sxs-lookup"><span data-stu-id="776cd-275">**Intel(R) Pentium(R) Processor Extreme Edition** (188)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_Processor"></span><span id="intel_r__core_tm__solo_processor"></span><span id="INTEL_R__CORE_TM__SOLO_PROCESSOR"></span>

<span data-ttu-id="776cd-276">**Processador Intel (R) Core (TM) solo** (189)</span><span class="sxs-lookup"><span data-stu-id="776cd-276">**Intel(R) Core(TM) Solo Processor** (189)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="776cd-277">**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="776cd-277">**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_Processor"></span><span id="intel_r__core_tm_2_duo_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_PROCESSOR"></span>

<span data-ttu-id="776cd-278">**Processador Intel (R) Core (TM) 2 Duo** (191)</span><span class="sxs-lookup"><span data-stu-id="776cd-278">**Intel(R) Core(TM)2 Duo Processor** (191)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_processor"></span><span id="intel_r__core_tm_2_solo_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_PROCESSOR"></span>

<span data-ttu-id="776cd-279">**Processador Intel (R) Core (TM) 2 solo** (192)</span><span class="sxs-lookup"><span data-stu-id="776cd-279">**Intel(R) Core(TM)2 Solo processor** (192)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_processor"></span><span id="intel_r__core_tm_2_extreme_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_PROCESSOR"></span>

<span data-ttu-id="776cd-280">**Processador Intel (R) Core (TM) 2 Extreme** (193)</span><span class="sxs-lookup"><span data-stu-id="776cd-280">**Intel(R) Core(TM)2 Extreme processor** (193)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Quad_processor"></span><span id="intel_r__core_tm_2_quad_processor"></span><span id="INTEL_R__CORE_TM_2_QUAD_PROCESSOR"></span>

<span data-ttu-id="776cd-281">**Processador Intel (R) Core (TM) 2 Quad** (194)</span><span class="sxs-lookup"><span data-stu-id="776cd-281">**Intel(R) Core(TM)2 Quad processor** (194)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_mobile_processor"></span><span id="intel_r__core_tm_2_extreme_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_MOBILE_PROCESSOR"></span>

<span data-ttu-id="776cd-282">**Processador Intel (R) Core (TM) 2 Extreme Mobile** (195)</span><span class="sxs-lookup"><span data-stu-id="776cd-282">**Intel(R) Core(TM)2 Extreme mobile processor** (195)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_mobile_processor"></span><span id="intel_r__core_tm_2_duo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="776cd-283">**Processador móvel Intel (R) Core (TM) 2 Duo** (196)</span><span class="sxs-lookup"><span data-stu-id="776cd-283">**Intel(R) Core(TM)2 Duo mobile processor** (196)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_mobile_processor"></span><span id="intel_r__core_tm_2_solo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="776cd-284">**Processador móvel Intel (R) Core (TM) 2 solo** (197)</span><span class="sxs-lookup"><span data-stu-id="776cd-284">**Intel(R) Core(TM)2 Solo mobile processor** (197)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i7_processor"></span><span id="intel_r__core_tm__i7_processor"></span><span id="INTEL_R__CORE_TM__I7_PROCESSOR"></span>

<span data-ttu-id="776cd-285">**Processador Intel (R) Core (TM) i7** (198)</span><span class="sxs-lookup"><span data-stu-id="776cd-285">**Intel(R) Core(TM) i7 processor** (198)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Celeron_R__Processor"></span><span id="dual-core_intel_r__celeron_r__processor"></span><span id="DUAL-CORE_INTEL_R__CELERON_R__PROCESSOR"></span>

<span data-ttu-id="776cd-286">**Processador Intel (r) Celeron (r) Dual-Core** (199)</span><span class="sxs-lookup"><span data-stu-id="776cd-286">**Dual-Core Intel(R) Celeron(R) Processor** (199)</span></span>


</dt> <dd></dd> <dt>

<span id="S_390_and_zSeries_Family"></span><span id="s_390_and_zseries_family"></span><span id="S_390_AND_ZSERIES_FAMILY"></span>

<span data-ttu-id="776cd-287">**S/390 e família zSeries** (200)</span><span class="sxs-lookup"><span data-stu-id="776cd-287">**S/390 and zSeries Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G4"></span><span id="esa_390_g4"></span>

<span data-ttu-id="776cd-288">**ESA/390 G4** (201)</span><span class="sxs-lookup"><span data-stu-id="776cd-288">**ESA/390 G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G5"></span><span id="esa_390_g5"></span>

<span data-ttu-id="776cd-289">**ESA/390 G5** (202)</span><span class="sxs-lookup"><span data-stu-id="776cd-289">**ESA/390 G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G6"></span><span id="esa_390_g6"></span>

<span data-ttu-id="776cd-290">**ESA/390 G6** (203)</span><span class="sxs-lookup"><span data-stu-id="776cd-290">**ESA/390 G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architectur_base"></span><span id="z_architectur_base"></span><span id="Z_ARCHITECTUR_BASE"></span>

<span data-ttu-id="776cd-291">**base z/Architectur** (204)</span><span class="sxs-lookup"><span data-stu-id="776cd-291">**z/Architectur base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i5_processor"></span><span id="intel_r__core_tm__i5_processor"></span><span id="INTEL_R__CORE_TM__I5_PROCESSOR"></span>

<span data-ttu-id="776cd-292">**Processador Intel (R) Core (TM) i5** (205)</span><span class="sxs-lookup"><span data-stu-id="776cd-292">**Intel(R) Core(TM) i5 processor** (205)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i3_processor"></span><span id="intel_r__core_tm__i3_processor"></span><span id="INTEL_R__CORE_TM__I3_PROCESSOR"></span>

<span data-ttu-id="776cd-293">**Processador Intel (R) Core (TM) i3** (206)</span><span class="sxs-lookup"><span data-stu-id="776cd-293">**Intel(R) Core(TM) i3 processor** (206)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-M_Processor_Family"></span><span id="via_c7_tm_-m_processor_family"></span><span id="VIA_C7_TM_-M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-294">**Via C7 (TM)-família de processadores M** (210)</span><span class="sxs-lookup"><span data-stu-id="776cd-294">**VIA C7(TM)-M Processor Family** (210)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-D_Processor_Family"></span><span id="via_c7_tm_-d_processor_family"></span><span id="VIA_C7_TM_-D_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-295">**Via C7 (TM) – família de processadores D** (211)</span><span class="sxs-lookup"><span data-stu-id="776cd-295">**VIA C7(TM)-D Processor Family** (211)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM__Processor_Family"></span><span id="via_c7_tm__processor_family"></span><span id="VIA_C7_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-296">**Via família de processador de C7 (TM)** (212)</span><span class="sxs-lookup"><span data-stu-id="776cd-296">**VIA C7(TM) Processor Family** (212)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Eden_TM__Processor_Family"></span><span id="via_eden_tm__processor_family"></span><span id="VIA_EDEN_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-297">**Por meio da família de processadores Eden (TM)** (213)</span><span class="sxs-lookup"><span data-stu-id="776cd-297">**VIA Eden(TM) Processor Family** (213)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor"></span><span id="multi-core_intel_r__xeon_r__processor"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="776cd-298">**Processador Intel (r) Xeon (r) de vários núcleos** (214)</span><span class="sxs-lookup"><span data-stu-id="776cd-298">**Multi-Core Intel(R) Xeon(R) processor** (214)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="776cd-299">**Processador dual-core Intel (r) Xeon (r) 3Xxx Series** (215)</span><span class="sxs-lookup"><span data-stu-id="776cd-299">**Dual-Core Intel(R) Xeon(R) processor 3xxx Series** (215)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="776cd-300">**Processador Quad-Core Intel (r) Xeon (r) 3Xxx Series** (216)</span><span class="sxs-lookup"><span data-stu-id="776cd-300">**Quad-Core Intel(R) Xeon(R) processor 3xxx Series** (216)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Nano_TM__Processor_Family"></span><span id="via_nano_tm__processor_family"></span><span id="VIA_NANO_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-301">**Por meio da família de processadores nano (TM)** (217)</span><span class="sxs-lookup"><span data-stu-id="776cd-301">**VIA Nano(TM) Processor Family** (217)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="776cd-302">**Processador dual-core Intel (r) Xeon (r) 5Xxx Series** (218)</span><span class="sxs-lookup"><span data-stu-id="776cd-302">**Dual-Core Intel(R) Xeon(R) processor 5xxx Series** (218)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="776cd-303">**Processador Quad-Core Intel (r) Xeon (r) 5Xxx Series** (219)</span><span class="sxs-lookup"><span data-stu-id="776cd-303">**Quad-Core Intel(R) Xeon(R) processor 5xxx Series** (219)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="776cd-304">**Processador dual-core Intel (r) Xeon (r) 7Xxx Series** (221)</span><span class="sxs-lookup"><span data-stu-id="776cd-304">**Dual-Core Intel(R) Xeon(R) processor 7xxx Series** (221)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="776cd-305">**Processador Quad-Core Intel (r) Xeon (r) 7Xxx Series** (222)</span><span class="sxs-lookup"><span data-stu-id="776cd-305">**Quad-Core Intel(R) Xeon(R) processor 7xxx Series** (222)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="776cd-306">**Série de processador Intel (r) Xeon (r) 7xxx de vários núcleos** (223)</span><span class="sxs-lookup"><span data-stu-id="776cd-306">**Multi-Core Intel(R) Xeon(R) processor 7xxx Series** (223)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_3400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_3400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_3400_SERIES"></span>

<span data-ttu-id="776cd-307">**Processador Intel (r) Xeon (r) série 3400 de vários núcleos** (224)</span><span class="sxs-lookup"><span data-stu-id="776cd-307">**Multi-Core Intel(R) Xeon(R) processor 3400 Series** (224)</span></span>


</dt> <dd></dd> <dt>

<span id="Embedded_AMD_Opteron_TM__Quad-Core_Processor_Family"></span><span id="embedded_amd_opteron_tm__quad-core_processor_family"></span><span id="EMBEDDED_AMD_OPTERON_TM__QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-308">**Família integrada de processador de Quad-Core AMD Opteron (TM)** (230)</span><span class="sxs-lookup"><span data-stu-id="776cd-308">**Embedded AMD Opteron(TM) Quad-Core Processor Family** (230)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__Triple-Core_Processor_Family"></span><span id="amd_phenom_tm__triple-core_processor_family"></span><span id="AMD_PHENOM_TM__TRIPLE-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-309">**AMD Phenom (TM) Triple-Core família de processadores** (231)</span><span class="sxs-lookup"><span data-stu-id="776cd-309">**AMD Phenom(TM) Triple-Core Processor Family** (231)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Ultra_Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__ultra_dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__ULTRA_DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-310">**Família AMD Turion (TM) Ultra Dual-Core Mobile Processor** (232)</span><span class="sxs-lookup"><span data-stu-id="776cd-310">**AMD Turion(TM) Ultra Dual-Core Mobile Processor Family** (232)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-311">**Família AMD Turion (TM) Dual-Core Mobile Processor** (233)</span><span class="sxs-lookup"><span data-stu-id="776cd-311">**AMD Turion(TM) Dual-Core Mobile Processor Family** (233)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__dual-core_processor_family"></span><span id="AMD_ATHLON_TM__DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-312">**Família de processadores AMD Athlon (TM) Dual-Core** (234)</span><span class="sxs-lookup"><span data-stu-id="776cd-312">**AMD Athlon(TM) Dual-Core Processor Family** (234)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__SI_Processor_Family"></span><span id="amd_sempron_tm__si_processor_family"></span><span id="AMD_SEMPRON_TM__SI_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-313">**Família de processadores de si do AMD Sempron (TM)** (235)</span><span class="sxs-lookup"><span data-stu-id="776cd-313">**AMD Sempron(TM) SI Processor Family** (235)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__II_Processor_Family"></span><span id="amd_phenom_tm__ii_processor_family"></span><span id="AMD_PHENOM_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-314">**Família de processadores AMD Phenom (TM) II** (236)</span><span class="sxs-lookup"><span data-stu-id="776cd-314">**AMD Phenom(TM) II Processor Family** (236)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Processor_Family"></span><span id="amd_athlon_tm__ii_processor_family"></span><span id="AMD_ATHLON_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-315">**Família de processadores AMD Athlon (TM) II** (237)</span><span class="sxs-lookup"><span data-stu-id="776cd-315">**AMD Athlon(TM) II Processor Family** (237)</span></span>


</dt> <dd></dd> <dt>

<span id="Six-Core_AMD_Opteron_TM__Processor_Family"></span><span id="six-core_amd_opteron_tm__processor_family"></span><span id="SIX-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-316">**Família de processadores AMD Opteron (TM) de seis núcleos** (238)</span><span class="sxs-lookup"><span data-stu-id="776cd-316">**Six-Core AMD Opteron(TM) Processor Family** (238)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__M_Processor_Family"></span><span id="amd_sempron_tm__m_processor_family"></span><span id="AMD_SEMPRON_TM__M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="776cd-317">**Família de processadores AMD Sempron (TM) M** (239)</span><span class="sxs-lookup"><span data-stu-id="776cd-317">**AMD Sempron(TM) M Processor Family** (239)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="776cd-318">**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="776cd-318">**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="776cd-319">**i960** (251)</span><span class="sxs-lookup"><span data-stu-id="776cd-319">**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__SMBIOS_Extension_"></span><span id="reserved__smbios_extension_"></span><span id="RESERVED__SMBIOS_EXTENSION_"></span>

<span data-ttu-id="776cd-320">**Reservado (extensão SMBIOS)** (254)</span><span class="sxs-lookup"><span data-stu-id="776cd-320">**Reserved (SMBIOS Extension)** (254)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Lo_"></span><span id="reserved__un-initialized_flash_content_-_lo_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_LO_"></span>

<span data-ttu-id="776cd-321">**Reservado (conteúdo Flash não inicializado-lo)** (255)</span><span class="sxs-lookup"><span data-stu-id="776cd-321">**Reserved (Un-initialized Flash Content - Lo)** (255)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="776cd-322">**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="776cd-322">**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="776cd-323">**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="776cd-323">**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="776cd-324">**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="776cd-324">**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="776cd-325">**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="776cd-325">**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="776cd-326">**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="776cd-326">**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="776cd-327">**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="776cd-327">**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="776cd-328">**MiI** (302)</span><span class="sxs-lookup"><span data-stu-id="776cd-328">**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="776cd-329">**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="776cd-329">**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="776cd-330">**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="776cd-330">**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="776cd-331">**Processador de vídeo** (500)</span><span class="sxs-lookup"><span data-stu-id="776cd-331">**Video Processor** (500)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__For_Future_Special_Purpose_Assignment_"></span><span id="reserved__for_future_special_purpose_assignment_"></span><span id="RESERVED__FOR_FUTURE_SPECIAL_PURPOSE_ASSIGNMENT_"></span>

<span data-ttu-id="776cd-332">**Reservado (para atribuição de finalidade especial futura)** (65534)</span><span class="sxs-lookup"><span data-stu-id="776cd-332">**Reserved (For Future Special Purpose Assignment)** (65534)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Hi_"></span><span id="reserved__un-initialized_flash_content_-_hi_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_HI_"></span>

<span data-ttu-id="776cd-333">**Reservado (conteúdo Flash não inicializado-Hi)** (65535)</span><span class="sxs-lookup"><span data-stu-id="776cd-333">**Reserved (Un-initialized Flash Content - Hi)** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="776cd-334">**Loadpercentual**</span><span class="sxs-lookup"><span data-stu-id="776cd-334">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-335">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-337">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent"), [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrProcessorLoad "), **PUnit** (" percent ")</span><span class="sxs-lookup"><span data-stu-id="776cd-337">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-338">O carregamento do processador, com a média do último minuto, como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="776cd-338">The loading of the processor, averaged over the last minute, as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-339">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="776cd-339">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-340">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="776cd-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-342">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 17,5 "), **PUnit** (" Hertz \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="776cd-342">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.5"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-343">A velocidade máxima, em MHz, do processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-343">The maximum speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-344">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="776cd-344">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776cd-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-347">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**Família**")</span><span class="sxs-lookup"><span data-stu-id="776cd-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-348">O tipo de família de processador quando a propriedade **Family** é definida como **Other** ("1").</span><span class="sxs-lookup"><span data-stu-id="776cd-348">The processor family type when the **Family** property is set to **Other** ("1").</span></span> <span data-ttu-id="776cd-349">Essa cadeia de caracteres deve ser definida como NULL quando a propriedade Family é qualquer valor diferente de **outro**.</span><span class="sxs-lookup"><span data-stu-id="776cd-349">This string should be set to NULL when the Family property is any value other than **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-350">**Função**</span><span class="sxs-lookup"><span data-stu-id="776cd-350">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776cd-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776cd-353">A função do processador, por exemplo, "processador central" ou "processador matemático".</span><span class="sxs-lookup"><span data-stu-id="776cd-353">The role of the processor, for example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="776cd-354">**Depuração**</span><span class="sxs-lookup"><span data-stu-id="776cd-354">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776cd-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-357">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processador CIM**.**Família**")</span><span class="sxs-lookup"><span data-stu-id="776cd-357">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-358">O nível de revisão do processador na família do processador.</span><span class="sxs-lookup"><span data-stu-id="776cd-358">The revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-359">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="776cd-359">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776cd-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776cd-362">Um identificador global exclusivo para o processador, dentro do escopo da família de processadores.</span><span class="sxs-lookup"><span data-stu-id="776cd-362">A globally unique identifier for the processor, within the scope of the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="776cd-363">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="776cd-363">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776cd-364">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="776cd-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="776cd-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776cd-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776cd-366">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processador DMTF \| 17,7 ")</span><span class="sxs-lookup"><span data-stu-id="776cd-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.7")</span></span>
</dt> </dl>

<span data-ttu-id="776cd-367">As informações de soquete da CPU que incluem dados sobre como o processador pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="776cd-367">The CPU socket information that includes data on how the processor can be upgraded.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="776cd-368">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="776cd-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="776cd-369">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="776cd-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="776cd-370">**Placa-filha** (3)</span><span class="sxs-lookup"><span data-stu-id="776cd-370">**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="776cd-371">**Soquete ZIF** (4)</span><span class="sxs-lookup"><span data-stu-id="776cd-371">**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="776cd-372">**Substituição/transportado de volta** (5)</span><span class="sxs-lookup"><span data-stu-id="776cd-372">**Replacement/Piggy Back** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="776cd-373">**Nenhum** (6)</span><span class="sxs-lookup"><span data-stu-id="776cd-373">**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="776cd-374">**Soquete LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="776cd-374">**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="776cd-375">**Slot 1** (8)</span><span class="sxs-lookup"><span data-stu-id="776cd-375">**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="776cd-376">**Slot 2** (9)</span><span class="sxs-lookup"><span data-stu-id="776cd-376">**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="776cd-377">**soquete 370 PIN** (10)</span><span class="sxs-lookup"><span data-stu-id="776cd-377">**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="776cd-378">**Slot A** (11)</span><span class="sxs-lookup"><span data-stu-id="776cd-378">**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="776cd-379">**Slot M** (12)</span><span class="sxs-lookup"><span data-stu-id="776cd-379">**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="776cd-380">**Soquete 423** (13)</span><span class="sxs-lookup"><span data-stu-id="776cd-380">**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="776cd-381">**Soquete A (soquete 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="776cd-381">**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="776cd-382">**Soquete 478** (15)</span><span class="sxs-lookup"><span data-stu-id="776cd-382">**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="776cd-383">**Soquete 754** (16)</span><span class="sxs-lookup"><span data-stu-id="776cd-383">**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="776cd-384">**Soquete 940** (17)</span><span class="sxs-lookup"><span data-stu-id="776cd-384">**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="776cd-385">**Soquete 939** (18)</span><span class="sxs-lookup"><span data-stu-id="776cd-385">**Socket 939** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_mPGA604"></span><span id="socket_mpga604"></span><span id="SOCKET_MPGA604"></span>

<span data-ttu-id="776cd-386">**Soquete mPGA604** (19)</span><span class="sxs-lookup"><span data-stu-id="776cd-386">**Socket mPGA604** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA771"></span><span id="socket_lga771"></span><span id="SOCKET_LGA771"></span>

<span data-ttu-id="776cd-387">**Soquete LGA771** (20)</span><span class="sxs-lookup"><span data-stu-id="776cd-387">**Socket LGA771** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA775"></span><span id="socket_lga775"></span><span id="SOCKET_LGA775"></span>

<span data-ttu-id="776cd-388">**Soquete LGA775** (21)</span><span class="sxs-lookup"><span data-stu-id="776cd-388">**Socket LGA775** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_S1"></span><span id="socket_s1"></span><span id="SOCKET_S1"></span>

<span data-ttu-id="776cd-389">**Soquete S1** (22)</span><span class="sxs-lookup"><span data-stu-id="776cd-389">**Socket S1** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM2"></span><span id="socket_am2"></span><span id="SOCKET_AM2"></span>

<span data-ttu-id="776cd-390">**Soquete AM2** (23)</span><span class="sxs-lookup"><span data-stu-id="776cd-390">**Socket AM2** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_F__1207_"></span><span id="socket_f__1207_"></span><span id="SOCKET_F__1207_"></span>

<span data-ttu-id="776cd-391">**Soquete F (1207)** (24)</span><span class="sxs-lookup"><span data-stu-id="776cd-391">**Socket F (1207)** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1366"></span><span id="socket_lga1366"></span><span id="SOCKET_LGA1366"></span>

<span data-ttu-id="776cd-392">**Soquete LGA1366** (25)</span><span class="sxs-lookup"><span data-stu-id="776cd-392">**Socket LGA1366** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_G34"></span><span id="socket_g34"></span><span id="SOCKET_G34"></span>

<span data-ttu-id="776cd-393">**Soquete G34** (26)</span><span class="sxs-lookup"><span data-stu-id="776cd-393">**Socket G34** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM3"></span><span id="socket_am3"></span><span id="SOCKET_AM3"></span>

<span data-ttu-id="776cd-394">**Soquete AM3** (27)</span><span class="sxs-lookup"><span data-stu-id="776cd-394">**Socket AM3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_C32"></span><span id="socket_c32"></span><span id="SOCKET_C32"></span>

<span data-ttu-id="776cd-395">**Soquete C32** (28)</span><span class="sxs-lookup"><span data-stu-id="776cd-395">**Socket C32** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1156"></span><span id="socket_lga1156"></span><span id="SOCKET_LGA1156"></span>

<span data-ttu-id="776cd-396">**Soquete LGA1156** (29)</span><span class="sxs-lookup"><span data-stu-id="776cd-396">**Socket LGA1156** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1567"></span><span id="socket_lga1567"></span><span id="SOCKET_LGA1567"></span>

<span data-ttu-id="776cd-397">**Soquete LGA1567** (30)</span><span class="sxs-lookup"><span data-stu-id="776cd-397">**Socket LGA1567** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_PGA988A"></span><span id="socket_pga988a"></span><span id="SOCKET_PGA988A"></span>

<span data-ttu-id="776cd-398">**Soquete PGA988A** (31)</span><span class="sxs-lookup"><span data-stu-id="776cd-398">**Socket PGA988A** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_BGA1288"></span><span id="socket_bga1288"></span><span id="SOCKET_BGA1288"></span>

<span data-ttu-id="776cd-399">**Soquete BGA1288** (32)</span><span class="sxs-lookup"><span data-stu-id="776cd-399">**Socket BGA1288** (32)</span></span>


<span data-ttu-id="776cd-400"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="776cd-400"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="776cd-401">Requisitos</span><span class="sxs-lookup"><span data-stu-id="776cd-401">Requirements</span></span>



| <span data-ttu-id="776cd-402">Requisito</span><span class="sxs-lookup"><span data-stu-id="776cd-402">Requirement</span></span> | <span data-ttu-id="776cd-403">Valor</span><span class="sxs-lookup"><span data-stu-id="776cd-403">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776cd-404">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776cd-404">Minimum supported client</span></span><br/> | <span data-ttu-id="776cd-405">Windows 8</span><span class="sxs-lookup"><span data-stu-id="776cd-405">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="776cd-406">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776cd-406">Minimum supported server</span></span><br/> | <span data-ttu-id="776cd-407">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="776cd-407">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="776cd-408">Namespace</span><span class="sxs-lookup"><span data-stu-id="776cd-408">Namespace</span></span><br/>                | <span data-ttu-id="776cd-409">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="776cd-409">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="776cd-410">MOF</span><span class="sxs-lookup"><span data-stu-id="776cd-410">MOF</span></span><br/>                      | <dl> <span data-ttu-id="776cd-411"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="776cd-411"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="776cd-412">DLL</span><span class="sxs-lookup"><span data-stu-id="776cd-412">DLL</span></span><br/>                      | <dl> <span data-ttu-id="776cd-413"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="776cd-413"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="776cd-414">Confira também</span><span class="sxs-lookup"><span data-stu-id="776cd-414">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776cd-415">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="776cd-415">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

