---
description: A \_ classe CIM ResidesOnExtent representa uma associação entre um sistema de arquivos e a extensão de armazenamento onde ele está localizado. Normalmente, um sistema de arquivos reside em um disco lógico.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: Classe CIM_ResidesOnExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089622"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="b663e-104">\_Classe CIM ResidesOnExtent</span><span class="sxs-lookup"><span data-stu-id="b663e-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="b663e-105">A classe **CIM \_ ResidesOnExtent** representa uma associação entre um sistema de arquivos e a extensão de armazenamento onde ele está localizado.</span><span class="sxs-lookup"><span data-stu-id="b663e-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="b663e-106">Normalmente, um sistema de arquivos reside em um disco lógico.</span><span class="sxs-lookup"><span data-stu-id="b663e-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b663e-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b663e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b663e-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b663e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b663e-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b663e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b663e-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b663e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b663e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b663e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b663e-112">Membros</span><span class="sxs-lookup"><span data-stu-id="b663e-112">Members</span></span>

<span data-ttu-id="b663e-113">A classe **CIM \_ ResidesOnExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b663e-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="b663e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b663e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b663e-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b663e-115">Properties</span></span>

<span data-ttu-id="b663e-116">A classe **CIM \_ ResidesOnExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b663e-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b663e-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b663e-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b663e-118">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="b663e-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b663e-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b663e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b663e-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b663e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b663e-121">Um [**\_ StorageExtent CIM**](cim-storageextent.md) que descreve a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b663e-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="b663e-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b663e-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b663e-123">Tipo de dados **: \_ sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="b663e-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b663e-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b663e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b663e-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b663e-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b663e-126">Um [**\_ sistema de arquivos CIM**](cim-filesystem.md) que descreve o sistema de arquivos que está localizado na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b663e-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b663e-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b663e-127">Remarks</span></span>

<span data-ttu-id="b663e-128">A classe **CIM \_ ResidesOnExtent** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b663e-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b663e-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b663e-129">WMI does not implement this class.</span></span>

<span data-ttu-id="b663e-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b663e-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b663e-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b663e-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b663e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b663e-132">Requirements</span></span>



| <span data-ttu-id="b663e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b663e-133">Requirement</span></span> | <span data-ttu-id="b663e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b663e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b663e-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b663e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b663e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b663e-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b663e-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b663e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b663e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b663e-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b663e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="b663e-139">Namespace</span></span><br/>                | <span data-ttu-id="b663e-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b663e-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b663e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b663e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b663e-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b663e-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b663e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b663e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b663e-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b663e-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b663e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b663e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b663e-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b663e-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

