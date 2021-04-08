---
description: A \_ classe de exportação CIM representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Classe CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920391"
---
# <a name="cim_export-class"></a><span data-ttu-id="98623-103">\_Classe de exportação CIM</span><span class="sxs-lookup"><span data-stu-id="98623-103">CIM\_Export class</span></span>

<span data-ttu-id="98623-104">A classe de **\_ exportação CIM** representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem.</span><span class="sxs-lookup"><span data-stu-id="98623-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="98623-105">Ao exportar um sistema de arquivos inteiro, o diretório deve fazer referência ao diretório de nível superior do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="98623-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98623-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="98623-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="98623-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="98623-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="98623-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="98623-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="98623-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="98623-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98623-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98623-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="98623-111">Membros</span><span class="sxs-lookup"><span data-stu-id="98623-111">Members</span></span>

<span data-ttu-id="98623-112">A classe de **\_ exportação CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="98623-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="98623-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98623-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98623-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98623-114">Properties</span></span>

<span data-ttu-id="98623-115">A classe de **\_ exportação CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="98623-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98623-116">**Diretório**</span><span class="sxs-lookup"><span data-stu-id="98623-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98623-117">Tipo de dados **: \_ diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="98623-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="98623-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98623-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98623-119">Referência ao diretório exportado para montagem NFS (sistema de arquivos de rede).</span><span class="sxs-lookup"><span data-stu-id="98623-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="98623-120">**ExportedDirectoryName**</span><span class="sxs-lookup"><span data-stu-id="98623-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98623-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98623-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98623-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98623-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98623-123">Nome sob o qual o diretório é exportado.</span><span class="sxs-lookup"><span data-stu-id="98623-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="98623-124">**LocalFS**</span><span class="sxs-lookup"><span data-stu-id="98623-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98623-125">Tipo de dados: **CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="98623-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="98623-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98623-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98623-127">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="98623-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="98623-128">Referência ao sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="98623-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98623-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="98623-129">Remarks</span></span>

<span data-ttu-id="98623-130">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="98623-130">WMI does not implement this class.</span></span>

<span data-ttu-id="98623-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="98623-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98623-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="98623-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98623-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98623-133">Requirements</span></span>



| <span data-ttu-id="98623-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="98623-134">Requirement</span></span> | <span data-ttu-id="98623-135">Valor</span><span class="sxs-lookup"><span data-stu-id="98623-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98623-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98623-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98623-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98623-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98623-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98623-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98623-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98623-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98623-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="98623-140">Namespace</span></span><br/>                | <span data-ttu-id="98623-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="98623-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98623-142">MOF</span><span class="sxs-lookup"><span data-stu-id="98623-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98623-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98623-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98623-144">DLL</span><span class="sxs-lookup"><span data-stu-id="98623-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98623-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98623-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

