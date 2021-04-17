---
description: A \_ classe WMI de associação do Win32 CIMLogicalDeviceCIMDataFile relaciona os dispositivos lógicos e os arquivos de dados, indicando os arquivos de driver usados pelo dispositivo. Essa classe é usada para descobrir quais drivers de dispositivo um dispositivo usa.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Classe Win32_CIMLogicalDeviceCIMDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501037"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="85db9-104">\_Classe Win32 CIMLogicalDeviceCIMDataFile</span><span class="sxs-lookup"><span data-stu-id="85db9-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="85db9-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ CIMLogicalDeviceCIMDataFile** relaciona os dispositivos lógicos e os arquivos de dados, indicando os arquivos de driver usados pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85db9-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="85db9-106">Essa classe é usada para descobrir quais drivers de dispositivo um dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="85db9-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="85db9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="85db9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="85db9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="85db9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85db9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85db9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="85db9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="85db9-110">Members</span></span>

<span data-ttu-id="85db9-111">A classe **Win32 \_ CIMLogicalDeviceCIMDataFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="85db9-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="85db9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="85db9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85db9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="85db9-113">Properties</span></span>

<span data-ttu-id="85db9-114">A classe **Win32 \_ CIMLogicalDeviceCIMDataFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="85db9-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85db9-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="85db9-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85db9-116">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="85db9-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="85db9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85db9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85db9-118">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="85db9-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="85db9-119">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico que está sendo usado pelo arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="85db9-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="85db9-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="85db9-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85db9-121">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="85db9-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="85db9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85db9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85db9-123">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="85db9-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="85db9-124">Um [**\_ DataFile CIM**](cim-datafile.md) que representa as propriedades do arquivo de dados atribuído ao dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85db9-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="85db9-125">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="85db9-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85db9-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85db9-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85db9-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85db9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85db9-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="85db9-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="85db9-129">Função que o arquivo de dados desempenha em relação ao seu dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="85db9-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="85db9-130">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="85db9-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="85db9-131">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="85db9-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="85db9-132">**Driver** (2)</span><span class="sxs-lookup"><span data-stu-id="85db9-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="85db9-133">**Software de configuração** (3)</span><span class="sxs-lookup"><span data-stu-id="85db9-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="85db9-134">**Software de aplicativo** (4)</span><span class="sxs-lookup"><span data-stu-id="85db9-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="85db9-135">**Instrumentação** (5)</span><span class="sxs-lookup"><span data-stu-id="85db9-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="85db9-136">**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="85db9-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85db9-137">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="85db9-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85db9-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85db9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85db9-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85db9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85db9-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="85db9-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="85db9-141">Estende o valor da propriedade **purpose** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="85db9-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="85db9-142">Exemplo: "driver de disquete"</span><span class="sxs-lookup"><span data-stu-id="85db9-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85db9-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="85db9-143">Remarks</span></span>

<span data-ttu-id="85db9-144">A classe **Win32 \_ CIMLogicalDeviceCIMDataFile** é derivada da [**\_ dependência CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="85db9-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85db9-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85db9-145">Requirements</span></span>



| <span data-ttu-id="85db9-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="85db9-146">Requirement</span></span> | <span data-ttu-id="85db9-147">Valor</span><span class="sxs-lookup"><span data-stu-id="85db9-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85db9-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85db9-148">Minimum supported client</span></span><br/> | <span data-ttu-id="85db9-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85db9-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85db9-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85db9-150">Minimum supported server</span></span><br/> | <span data-ttu-id="85db9-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85db9-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85db9-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="85db9-152">Namespace</span></span><br/>                | <span data-ttu-id="85db9-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="85db9-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85db9-154">MOF</span><span class="sxs-lookup"><span data-stu-id="85db9-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85db9-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85db9-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85db9-156">DLL</span><span class="sxs-lookup"><span data-stu-id="85db9-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85db9-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85db9-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85db9-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="85db9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85db9-159">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="85db9-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="85db9-160">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85db9-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

