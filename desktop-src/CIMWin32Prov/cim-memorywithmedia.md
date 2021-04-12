---
description: A \_ classe CIM MemoryWithMedia associa a memória física a uma mídia física e a seu cartucho. A memória fornece a identificação de mídia e armazena dados específicos do usuário.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: Classe CIM_MemoryWithMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297976"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="d23f2-104">\_Classe CIM MemoryWithMedia</span><span class="sxs-lookup"><span data-stu-id="d23f2-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="d23f2-105">A classe **CIM \_ MemoryWithMedia** associa a memória física a uma mídia física e a seu cartucho.</span><span class="sxs-lookup"><span data-stu-id="d23f2-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="d23f2-106">A memória fornece a identificação de mídia e armazena dados específicos do usuário.</span><span class="sxs-lookup"><span data-stu-id="d23f2-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d23f2-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d23f2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d23f2-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d23f2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d23f2-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d23f2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d23f2-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d23f2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d23f2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d23f2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d23f2-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d23f2-112">Members</span></span>

<span data-ttu-id="d23f2-113">A classe **CIM \_ MemoryWithMedia** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d23f2-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="d23f2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d23f2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d23f2-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d23f2-115">Properties</span></span>

<span data-ttu-id="d23f2-116">A classe **CIM \_ MemoryWithMedia** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d23f2-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d23f2-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d23f2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23f2-118">Tipo de dados: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="d23f2-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="d23f2-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d23f2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23f2-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d23f2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d23f2-121">Um [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) que descreve a memória associada à mídia física.</span><span class="sxs-lookup"><span data-stu-id="d23f2-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="d23f2-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d23f2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23f2-123">Tipo de dados: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="d23f2-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="d23f2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d23f2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23f2-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d23f2-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d23f2-126">Um [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que descreve a mídia física.</span><span class="sxs-lookup"><span data-stu-id="d23f2-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d23f2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d23f2-127">Remarks</span></span>

<span data-ttu-id="d23f2-128">**CIM \_ MemoryWithMedia** é herdado [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d23f2-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d23f2-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d23f2-129">WMI does not implement this class.</span></span>

<span data-ttu-id="d23f2-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d23f2-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d23f2-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d23f2-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d23f2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d23f2-132">Requirements</span></span>



| <span data-ttu-id="d23f2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d23f2-133">Requirement</span></span> | <span data-ttu-id="d23f2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d23f2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d23f2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d23f2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d23f2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d23f2-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d23f2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d23f2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d23f2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d23f2-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d23f2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d23f2-139">Namespace</span></span><br/>                | <span data-ttu-id="d23f2-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d23f2-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d23f2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d23f2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d23f2-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d23f2-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d23f2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d23f2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d23f2-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d23f2-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d23f2-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="d23f2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d23f2-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="d23f2-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

