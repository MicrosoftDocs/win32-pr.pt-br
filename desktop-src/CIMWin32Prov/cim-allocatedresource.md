---
description: A \_ classe CIM AllocatedResource representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso está atribuído ao dispositivo.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: Classe CIM_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089405"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="1c9c0-103">\_Classe CIM AllocatedResource</span><span class="sxs-lookup"><span data-stu-id="1c9c0-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="1c9c0-104">A classe **CIM \_ AllocatedResource** representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso está atribuído ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c9c0-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c9c0-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c9c0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c9c0-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9c0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c9c0-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1c9c0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1c9c0-109">Members</span></span>

<span data-ttu-id="1c9c0-110">A classe **CIM \_ AllocatedResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c9c0-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="1c9c0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c9c0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c9c0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c9c0-112">Properties</span></span>

<span data-ttu-id="1c9c0-113">A classe **CIM \_ AllocatedResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c9c0-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1c9c0-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c0-115">Tipo de dados: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="1c9c0-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c0-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c9c0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c9c0-117">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1c9c0-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1c9c0-118">Um [**\_ SystemResource CIM**](cim-systemresource.md) que descreve o recurso.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1c9c0-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1c9c0-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9c0-120">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="1c9c0-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1c9c0-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c9c0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c9c0-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="1c9c0-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1c9c0-123">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que contém o dispositivo lógico ao qual o recurso é atribuído.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c9c0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c9c0-124">Remarks</span></span>

<span data-ttu-id="1c9c0-125">A classe **CIM \_ AllocatedResource** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1c9c0-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="1c9c0-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-126">WMI does not implement this class.</span></span> <span data-ttu-id="1c9c0-127">Para obter mais informações sobre classes derivadas de **CIM \_ AllocatedResource**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1c9c0-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1c9c0-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c9c0-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1c9c0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9c0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c9c0-130">Requirements</span></span>



| <span data-ttu-id="1c9c0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c9c0-131">Requirement</span></span> | <span data-ttu-id="1c9c0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1c9c0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9c0-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c9c0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9c0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c9c0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c9c0-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c9c0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9c0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c9c0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c9c0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c9c0-137">Namespace</span></span><br/>                | <span data-ttu-id="1c9c0-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1c9c0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c9c0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1c9c0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c9c0-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c9c0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c9c0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1c9c0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c9c0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c9c0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c9c0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c9c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9c0-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1c9c0-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

