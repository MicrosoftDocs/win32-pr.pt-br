---
description: A \_ associação CIM DirectorySpecificationFile representa o diretório que contém o arquivo especificado referenciando a \_ classe CIM DirectorySpecification.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecificationFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089388"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="e49bb-103">\_Classe CIM DirectorySpecificationFile</span><span class="sxs-lookup"><span data-stu-id="e49bb-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="e49bb-104">A associação **CIM \_ DirectorySpecificationFile** representa o diretório que contém o arquivo especificado referenciando a classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="e49bb-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e49bb-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e49bb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e49bb-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e49bb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e49bb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e49bb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e49bb-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e49bb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49bb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e49bb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="e49bb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e49bb-110">Members</span></span>

<span data-ttu-id="e49bb-111">A classe **CIM \_ DirectorySpecificationFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e49bb-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="e49bb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e49bb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e49bb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e49bb-113">Properties</span></span>

<span data-ttu-id="e49bb-114">A classe **CIM \_ DirectorySpecificationFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e49bb-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e49bb-115">**DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="e49bb-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e49bb-116">Tipo de dados: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="e49bb-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="e49bb-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e49bb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e49bb-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="e49bb-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="e49bb-119">Referência à especificação de diretório.</span><span class="sxs-lookup"><span data-stu-id="e49bb-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="e49bb-120">**Especificações de**</span><span class="sxs-lookup"><span data-stu-id="e49bb-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e49bb-121">Tipo de dados: o **CIM \_ fileespecificion**</span><span class="sxs-lookup"><span data-stu-id="e49bb-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="e49bb-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e49bb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e49bb-123">Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="e49bb-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="e49bb-124">Referência à especificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e49bb-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e49bb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e49bb-125">Remarks</span></span>

<span data-ttu-id="e49bb-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e49bb-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e49bb-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e49bb-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e49bb-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e49bb-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49bb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e49bb-129">Requirements</span></span>



| <span data-ttu-id="e49bb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e49bb-130">Requirement</span></span> | <span data-ttu-id="e49bb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e49bb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e49bb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e49bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e49bb-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e49bb-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e49bb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e49bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e49bb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e49bb-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e49bb-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e49bb-136">Namespace</span></span><br/>                | <span data-ttu-id="e49bb-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e49bb-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e49bb-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e49bb-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e49bb-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e49bb-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e49bb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e49bb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49bb-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e49bb-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

