---
description: A \_ classe CIM DirectoryContainsFile representa uma associação entre um diretório e os arquivos contidos nesse diretório.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Classe CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826531"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="8e920-103">\_Classe CIM DirectoryContainsFile</span><span class="sxs-lookup"><span data-stu-id="8e920-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="8e920-104">A classe **CIM \_ DirectoryContainsFile** representa uma associação entre um diretório e os arquivos contidos nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="8e920-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e920-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8e920-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e920-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e920-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e920-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8e920-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e920-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8e920-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e920-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e920-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="8e920-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8e920-110">Members</span></span>

<span data-ttu-id="8e920-111">A classe **CIM \_ DirectoryContainsFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8e920-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="8e920-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e920-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e920-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e920-113">Properties</span></span>

<span data-ttu-id="8e920-114">A classe **CIM \_ DirectoryContainsFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e920-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e920-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8e920-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e920-116">Tipo de dados **: \_ diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="8e920-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="8e920-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e920-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e920-118">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="8e920-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8e920-119">Um [**\_ diretório CIM**](cim-directory.md) que descreve o diretório.</span><span class="sxs-lookup"><span data-stu-id="8e920-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="8e920-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8e920-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e920-121">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="8e920-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="8e920-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e920-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e920-123">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8e920-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8e920-124">Um [**\_ DataFile do CIM**](cim-datafile.md) que descreve o LogicalFile contido no diretório.</span><span class="sxs-lookup"><span data-stu-id="8e920-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e920-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e920-125">Remarks</span></span>

<span data-ttu-id="8e920-126">O WMI implementa a classe **CIM \_ DirectoryContainsFile** , que é uma classe dinâmica.</span><span class="sxs-lookup"><span data-stu-id="8e920-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="8e920-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e920-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e920-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e920-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e920-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e920-129">Requirements</span></span>



| <span data-ttu-id="8e920-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e920-130">Requirement</span></span> | <span data-ttu-id="8e920-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8e920-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e920-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e920-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8e920-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e920-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e920-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e920-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8e920-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e920-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e920-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e920-136">Namespace</span></span><br/>                | <span data-ttu-id="8e920-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e920-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e920-138">MOF</span><span class="sxs-lookup"><span data-stu-id="8e920-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e920-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e920-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e920-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8e920-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e920-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e920-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e920-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e920-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e920-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="8e920-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

