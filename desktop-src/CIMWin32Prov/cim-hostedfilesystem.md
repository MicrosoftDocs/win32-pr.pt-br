---
description: A \_ associação CIM HostedFileSystem representa um link entre o sistema de computador e o sistema de arquivos hospedado no sistema de computador.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: Classe CIM_HostedFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089279"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="00252-103">\_Classe CIM HostedFileSystem</span><span class="sxs-lookup"><span data-stu-id="00252-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="00252-104">A associação **CIM \_ HostedFileSystem** representa um link entre o sistema de computador e o sistema de arquivos hospedado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="00252-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00252-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="00252-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="00252-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="00252-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="00252-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="00252-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="00252-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="00252-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00252-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00252-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="00252-110">Membros</span><span class="sxs-lookup"><span data-stu-id="00252-110">Members</span></span>

<span data-ttu-id="00252-111">A classe **CIM \_ HostedFileSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="00252-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="00252-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00252-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00252-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00252-113">Properties</span></span>

<span data-ttu-id="00252-114">A classe **CIM \_ HostedFileSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="00252-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00252-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="00252-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00252-116">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="00252-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="00252-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00252-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="00252-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="00252-119">Um [**computador \_ CIM**](cim-computersystem.md) que descreve o sistema de computadores.</span><span class="sxs-lookup"><span data-stu-id="00252-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="00252-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="00252-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00252-121">Tipo de dados **: \_ sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="00252-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="00252-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="00252-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00252-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00252-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00252-124">Um sistema de [**\_ arquivos CIM**](cim-filesystem.md) que descreve o sistema de arquivos de Propriedade do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="00252-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00252-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="00252-125">Remarks</span></span>

<span data-ttu-id="00252-126">A classe **CIM \_ HostedFileSystem** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="00252-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="00252-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="00252-127">WMI does not implement this class.</span></span>

<span data-ttu-id="00252-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="00252-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="00252-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="00252-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="00252-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00252-130">Requirements</span></span>



| <span data-ttu-id="00252-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="00252-131">Requirement</span></span> | <span data-ttu-id="00252-132">Valor</span><span class="sxs-lookup"><span data-stu-id="00252-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00252-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00252-133">Minimum supported client</span></span><br/> | <span data-ttu-id="00252-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00252-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00252-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00252-135">Minimum supported server</span></span><br/> | <span data-ttu-id="00252-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00252-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00252-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="00252-137">Namespace</span></span><br/>                | <span data-ttu-id="00252-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="00252-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00252-139">MOF</span><span class="sxs-lookup"><span data-stu-id="00252-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00252-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00252-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00252-141">DLL</span><span class="sxs-lookup"><span data-stu-id="00252-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00252-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00252-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00252-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="00252-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00252-144">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="00252-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

