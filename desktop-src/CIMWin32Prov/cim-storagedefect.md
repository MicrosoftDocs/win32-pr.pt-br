---
description: A \_ agregação CIM StorageDefect coleta os erros de armazenamento para uma extensão de armazenamento.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Classe CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920541"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="dbf91-103">\_Classe CIM StorageDefect</span><span class="sxs-lookup"><span data-stu-id="dbf91-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="dbf91-104">A agregação **CIM \_ StorageDefect** coleta os erros de armazenamento para uma extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dbf91-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbf91-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="dbf91-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbf91-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbf91-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbf91-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dbf91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dbf91-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="dbf91-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf91-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbf91-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="dbf91-110">Membros</span><span class="sxs-lookup"><span data-stu-id="dbf91-110">Members</span></span>

<span data-ttu-id="dbf91-111">A classe **CIM \_ StorageDefect** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dbf91-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="dbf91-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbf91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbf91-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbf91-113">Properties</span></span>

<span data-ttu-id="dbf91-114">A classe **CIM \_ StorageDefect** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dbf91-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbf91-115">**Erro**</span><span class="sxs-lookup"><span data-stu-id="dbf91-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf91-116">Tipo de dados: **CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="dbf91-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="dbf91-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbf91-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf91-118">Qualificadores: [ **fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbf91-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbf91-119">Referência ao objeto de erro, que define os endereços inicial e final que são mapeados fora da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dbf91-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="dbf91-120">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="dbf91-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf91-121">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="dbf91-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="dbf91-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbf91-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf91-123">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dbf91-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dbf91-124">Referência à extensão de armazenamento na qual os erros ocorreram.</span><span class="sxs-lookup"><span data-stu-id="dbf91-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbf91-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbf91-125">Remarks</span></span>

<span data-ttu-id="dbf91-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="dbf91-126">WMI does not implement this class.</span></span>

<span data-ttu-id="dbf91-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="dbf91-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbf91-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="dbf91-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf91-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbf91-129">Requirements</span></span>



| <span data-ttu-id="dbf91-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbf91-130">Requirement</span></span> | <span data-ttu-id="dbf91-131">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf91-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf91-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbf91-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf91-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbf91-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbf91-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbf91-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf91-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf91-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbf91-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbf91-136">Namespace</span></span><br/>                | <span data-ttu-id="dbf91-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dbf91-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbf91-138">MOF</span><span class="sxs-lookup"><span data-stu-id="dbf91-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbf91-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbf91-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbf91-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf91-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf91-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf91-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

