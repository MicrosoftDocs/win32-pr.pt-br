---
description: A \_ classe CIM InstalledSoftwareElement associa um sistema de computador a um elemento de software instalado.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: Classe CIM_InstalledSoftwareElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089276"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="8921d-103">\_Classe CIM InstalledSoftwareElement</span><span class="sxs-lookup"><span data-stu-id="8921d-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="8921d-104">A classe **CIM \_ InstalledSoftwareElement** associa um sistema de computador a um elemento de software instalado.</span><span class="sxs-lookup"><span data-stu-id="8921d-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8921d-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8921d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8921d-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8921d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8921d-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8921d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8921d-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8921d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8921d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8921d-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="8921d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8921d-110">Members</span></span>

<span data-ttu-id="8921d-111">A classe **CIM \_ InstalledSoftwareElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8921d-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="8921d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8921d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8921d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8921d-113">Properties</span></span>

<span data-ttu-id="8921d-114">A classe **CIM \_ InstalledSoftwareElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8921d-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8921d-115">**Software**</span><span class="sxs-lookup"><span data-stu-id="8921d-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8921d-116">Tipo de dados: **CIM \_ softwareelement**</span><span class="sxs-lookup"><span data-stu-id="8921d-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="8921d-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8921d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8921d-118">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="8921d-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="8921d-119">Referência ao elemento de software que está instalado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="8921d-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="8921d-120">**System**</span><span class="sxs-lookup"><span data-stu-id="8921d-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8921d-121">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="8921d-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8921d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8921d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8921d-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="8921d-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="8921d-124">Referência ao sistema de computador que hospeda um determinado elemento de software.</span><span class="sxs-lookup"><span data-stu-id="8921d-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8921d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8921d-125">Remarks</span></span>

<span data-ttu-id="8921d-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8921d-126">WMI does not implement this class.</span></span> <span data-ttu-id="8921d-127">Para classes derivadas do **CIM \_ InstalledSoftwareElement**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8921d-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8921d-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8921d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8921d-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8921d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8921d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8921d-130">Requirements</span></span>



| <span data-ttu-id="8921d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8921d-131">Requirement</span></span> | <span data-ttu-id="8921d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8921d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8921d-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8921d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8921d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8921d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8921d-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8921d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8921d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8921d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8921d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8921d-137">Namespace</span></span><br/>                | <span data-ttu-id="8921d-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8921d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8921d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8921d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8921d-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8921d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8921d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8921d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

