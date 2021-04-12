---
description: A \_ classe de associação CIM InstalledOS representa um link entre o sistema de computador e o sistema operacional instalado.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Classe CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500978"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="01f71-103">\_Classe CIM InstalledOS</span><span class="sxs-lookup"><span data-stu-id="01f71-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="01f71-104">A classe de associação **CIM \_ InstalledOS** representa um link entre o sistema de computador e o sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="01f71-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="01f71-105">Um sistema operacional é instalado quando está na extensão de armazenamento de um sistema de computador (por exemplo, copiado para uma unidade de disco ou baixado para memória).</span><span class="sxs-lookup"><span data-stu-id="01f71-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01f71-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="01f71-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01f71-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01f71-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01f71-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01f71-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01f71-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="01f71-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f71-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01f71-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="01f71-111">Membros</span><span class="sxs-lookup"><span data-stu-id="01f71-111">Members</span></span>

<span data-ttu-id="01f71-112">A classe **CIM \_ InstalledOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01f71-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="01f71-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01f71-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01f71-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01f71-114">Properties</span></span>

<span data-ttu-id="01f71-115">A classe **CIM \_ InstalledOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01f71-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01f71-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="01f71-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f71-117">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="01f71-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="01f71-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01f71-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f71-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="01f71-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="01f71-120">Um sistema de computadores [**CIM \_**](cim-computersystem.md) que descreve o computador.</span><span class="sxs-lookup"><span data-stu-id="01f71-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="01f71-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="01f71-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f71-122">Tipo de dados: sistema **\_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="01f71-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="01f71-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01f71-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f71-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01f71-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01f71-125">Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional instalado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="01f71-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="01f71-126">**PrimaryOS**</span><span class="sxs-lookup"><span data-stu-id="01f71-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f71-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01f71-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01f71-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01f71-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f71-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operacional DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="01f71-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="01f71-130">Se for **true**, o sistema operacional instalado será o sistema operacional padrão do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="01f71-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01f71-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="01f71-131">Remarks</span></span>

<span data-ttu-id="01f71-132">A classe **CIM \_ InstalledOS** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="01f71-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="01f71-133">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="01f71-133">WMI does not implement this class.</span></span> <span data-ttu-id="01f71-134">Para classes derivadas do **CIM \_ InstalledOS**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="01f71-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="01f71-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="01f71-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01f71-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="01f71-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f71-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f71-137">Requirements</span></span>



| <span data-ttu-id="01f71-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f71-138">Requirement</span></span> | <span data-ttu-id="01f71-139">Valor</span><span class="sxs-lookup"><span data-stu-id="01f71-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f71-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f71-140">Minimum supported client</span></span><br/> | <span data-ttu-id="01f71-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01f71-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01f71-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f71-142">Minimum supported server</span></span><br/> | <span data-ttu-id="01f71-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f71-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01f71-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="01f71-144">Namespace</span></span><br/>                | <span data-ttu-id="01f71-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01f71-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01f71-146">MOF</span><span class="sxs-lookup"><span data-stu-id="01f71-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f71-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f71-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01f71-148">DLL</span><span class="sxs-lookup"><span data-stu-id="01f71-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f71-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f71-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f71-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="01f71-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f71-151">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="01f71-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

