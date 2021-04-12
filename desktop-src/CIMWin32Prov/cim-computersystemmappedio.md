---
description: A \_ classe CIM ComputerSystemMappedIO representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089349"
---
# <a name="cim_computersystemmappedio-class"></a><span data-ttu-id="58428-103">\_Classe CIM ComputerSystemMappedIO</span><span class="sxs-lookup"><span data-stu-id="58428-103">CIM\_ComputerSystemMappedIO class</span></span>

<span data-ttu-id="58428-104">A classe **CIM \_ ComputerSystemMappedIO** representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.</span><span class="sxs-lookup"><span data-stu-id="58428-104">The **CIM\_ComputerSystemMappedIO** class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58428-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="58428-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58428-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58428-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58428-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="58428-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58428-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="58428-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58428-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58428-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="58428-110">Membros</span><span class="sxs-lookup"><span data-stu-id="58428-110">Members</span></span>

<span data-ttu-id="58428-111">A classe **CIM \_ ComputerSystemMappedIO** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58428-111">The **CIM\_ComputerSystemMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="58428-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58428-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58428-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58428-113">Properties</span></span>

<span data-ttu-id="58428-114">A classe **CIM \_ ComputerSystemMappedIO** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58428-114">The **CIM\_ComputerSystemMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58428-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="58428-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58428-116">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="58428-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="58428-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58428-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58428-118">Qualificadores: [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="58428-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="58428-119">Um [**computador \_ CIM**](cim-computersystem.md) que descreve o sistema de computadores mapeado para a porta de e/s.</span><span class="sxs-lookup"><span data-stu-id="58428-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system mapped to the I/O port.</span></span>

<span data-ttu-id="58428-120">Esta propriedade é herdada do [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="58428-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="58428-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="58428-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58428-122">Tipo de dados: **CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="58428-122">Data type: **CIM\_MemoryMappedIO**</span></span>
</dt> <dt>

<span data-ttu-id="58428-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58428-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58428-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="58428-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="58428-125">Um [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md) que descreve uma porta de e/s mapeada da memória do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="58428-125">A [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) that describes a memory mapped I/O port of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58428-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="58428-126">Remarks</span></span>

<span data-ttu-id="58428-127">A classe **CIM \_ ComputerSystemMappedIO** é derivada de [**\_ ComputerSystemResource CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="58428-127">The **CIM\_ComputerSystemMappedIO** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="58428-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="58428-128">WMI does not implement this class.</span></span>

<span data-ttu-id="58428-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="58428-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58428-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="58428-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58428-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58428-131">Requirements</span></span>



| <span data-ttu-id="58428-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="58428-132">Requirement</span></span> | <span data-ttu-id="58428-133">Valor</span><span class="sxs-lookup"><span data-stu-id="58428-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58428-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58428-134">Minimum supported client</span></span><br/> | <span data-ttu-id="58428-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58428-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58428-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58428-136">Minimum supported server</span></span><br/> | <span data-ttu-id="58428-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58428-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58428-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="58428-138">Namespace</span></span><br/>                | <span data-ttu-id="58428-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="58428-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58428-140">MOF</span><span class="sxs-lookup"><span data-stu-id="58428-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58428-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58428-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58428-142">DLL</span><span class="sxs-lookup"><span data-stu-id="58428-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58428-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58428-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58428-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="58428-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58428-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="58428-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

