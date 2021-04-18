---
description: A \_ Associação de armazenamento de arquivo CIM vincula o sistema de arquivos e os arquivos lógicos endereçados por meio do sistema de arquivos.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: Classe CIM_FileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756466"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="c369a-103">Classe de armazenamento de filecim \_</span><span class="sxs-lookup"><span data-stu-id="c369a-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="c369a-104">A associação de **\_ armazenamento** de arquivo CIM vincula o sistema de arquivos e os arquivos lógicos endereçados por meio do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c369a-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c369a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c369a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c369a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c369a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c369a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c369a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c369a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c369a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c369a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c369a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="c369a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c369a-110">Members</span></span>

<span data-ttu-id="c369a-111">A classe de **\_ armazenamento de filecim** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c369a-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="c369a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c369a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c369a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c369a-113">Properties</span></span>

<span data-ttu-id="c369a-114">A classe **CIM \_ FileStorage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c369a-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c369a-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c369a-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c369a-116">Tipo de dados **: \_ sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="c369a-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c369a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c369a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c369a-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="c369a-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c369a-119">Um [**\_ sistema**](cim-filesystem.md) de arquivos CIM que descreve o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c369a-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="c369a-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c369a-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c369a-121">Tipo de dados: **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="c369a-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="c369a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c369a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c369a-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c369a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c369a-124">Um [**\_ LogicalFile CIM**](cim-logicalfile.md) que descreve o arquivo lógico armazenado no contexto do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c369a-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c369a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c369a-125">Remarks</span></span>

<span data-ttu-id="c369a-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c369a-126">WMI does not implement this class.</span></span>

<span data-ttu-id="c369a-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c369a-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c369a-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c369a-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c369a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c369a-129">Requirements</span></span>



| <span data-ttu-id="c369a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c369a-130">Requirement</span></span> | <span data-ttu-id="c369a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c369a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c369a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c369a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c369a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c369a-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c369a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c369a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c369a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c369a-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c369a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c369a-136">Namespace</span></span><br/>                | <span data-ttu-id="c369a-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c369a-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c369a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c369a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c369a-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c369a-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c369a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c369a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c369a-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c369a-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c369a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c369a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c369a-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="c369a-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

