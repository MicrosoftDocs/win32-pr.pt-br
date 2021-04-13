---
description: O \_ relacionamento CIM DeviceSoftware identifica o software associado a um dispositivo, como drivers, configuração ou software de aplicativo ou firmware.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: Classe CIM_DeviceSoftware
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501009"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="252d8-103">\_Classe CIM DeviceSoftware</span><span class="sxs-lookup"><span data-stu-id="252d8-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="252d8-104">O relacionamento **CIM \_ DeviceSoftware** identifica o software associado a um dispositivo, como drivers, configuração ou software de aplicativo ou firmware.</span><span class="sxs-lookup"><span data-stu-id="252d8-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="252d8-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="252d8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="252d8-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="252d8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="252d8-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="252d8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="252d8-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="252d8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="252d8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="252d8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="252d8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="252d8-110">Members</span></span>

<span data-ttu-id="252d8-111">A classe **CIM \_ DeviceSoftware** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="252d8-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="252d8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="252d8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="252d8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="252d8-113">Properties</span></span>

<span data-ttu-id="252d8-114">A classe **CIM \_ DeviceSoftware** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="252d8-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="252d8-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="252d8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="252d8-116">Tipo de dados: **CIM \_ softwareelement**</span><span class="sxs-lookup"><span data-stu-id="252d8-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="252d8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="252d8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="252d8-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="252d8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="252d8-119">Um [**\_ software CIM**](cim-softwareelement.md) que descreve o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="252d8-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="252d8-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="252d8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="252d8-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="252d8-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="252d8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="252d8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="252d8-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="252d8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="252d8-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico que exige ou usa o software.</span><span class="sxs-lookup"><span data-stu-id="252d8-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="252d8-125">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="252d8-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="252d8-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="252d8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="252d8-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="252d8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="252d8-128">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="252d8-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="252d8-129">Função que o software assume com relação a seu dispositivo associado.</span><span class="sxs-lookup"><span data-stu-id="252d8-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="252d8-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="252d8-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-131">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="252d8-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="252d8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="252d8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-133">Outros.</span><span class="sxs-lookup"><span data-stu-id="252d8-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="252d8-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span><span class="sxs-lookup"><span data-stu-id="252d8-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-135">Driver.</span><span class="sxs-lookup"><span data-stu-id="252d8-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="252d8-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Software de configuração** (3)</span><span class="sxs-lookup"><span data-stu-id="252d8-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-137">Software de configuração.</span><span class="sxs-lookup"><span data-stu-id="252d8-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="252d8-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Software de aplicativo** (4)</span><span class="sxs-lookup"><span data-stu-id="252d8-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-139">Software de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="252d8-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="252d8-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentação** (5)</span><span class="sxs-lookup"><span data-stu-id="252d8-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-141">Instrumentação.</span><span class="sxs-lookup"><span data-stu-id="252d8-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="252d8-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="252d8-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-143">Firmware.</span><span class="sxs-lookup"><span data-stu-id="252d8-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="252d8-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="252d8-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-145">BIOS.</span><span class="sxs-lookup"><span data-stu-id="252d8-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="252d8-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span><span class="sxs-lookup"><span data-stu-id="252d8-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="252d8-147">Boot ROM.</span><span class="sxs-lookup"><span data-stu-id="252d8-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="252d8-148">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="252d8-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="252d8-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="252d8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="252d8-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="252d8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="252d8-151">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**Finalidade**")</span><span class="sxs-lookup"><span data-stu-id="252d8-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="252d8-152">Cadeia de caracteres de forma livre que fornece mais informações para a propriedade **purpose** , por exemplo, "software de aplicativo".</span><span class="sxs-lookup"><span data-stu-id="252d8-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="252d8-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="252d8-153">Remarks</span></span>

<span data-ttu-id="252d8-154">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="252d8-154">WMI does not implement this class.</span></span>

<span data-ttu-id="252d8-155">A classe **CIM \_ DeviceSoftware** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="252d8-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="252d8-156">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="252d8-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="252d8-157">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="252d8-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="252d8-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="252d8-158">Requirements</span></span>



| <span data-ttu-id="252d8-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="252d8-159">Requirement</span></span> | <span data-ttu-id="252d8-160">Valor</span><span class="sxs-lookup"><span data-stu-id="252d8-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="252d8-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="252d8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="252d8-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="252d8-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="252d8-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="252d8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="252d8-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="252d8-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="252d8-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="252d8-165">Namespace</span></span><br/>                | <span data-ttu-id="252d8-166">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="252d8-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="252d8-167">MOF</span><span class="sxs-lookup"><span data-stu-id="252d8-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="252d8-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="252d8-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="252d8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="252d8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="252d8-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="252d8-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252d8-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="252d8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252d8-172">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="252d8-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

