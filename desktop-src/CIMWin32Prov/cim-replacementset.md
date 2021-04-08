---
description: A \_ classe de conjunto de substituição CIM agrega elementos físicos que devem ser substituídos juntos.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: Classe CIM_ReplacementSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088981"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="4c789-103">Classe de substituição de CIM \_</span><span class="sxs-lookup"><span data-stu-id="4c789-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="4c789-104">A classe de conjunto de **\_ substituição CIM** agrega elementos físicos que devem ser substituídos juntos.</span><span class="sxs-lookup"><span data-stu-id="4c789-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="4c789-105">Por exemplo, ao substituir um cartão de memória, os chips de memória do componente também podem ser removidos e substituídos.</span><span class="sxs-lookup"><span data-stu-id="4c789-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="4c789-106">Ou, essa associação pode ser usada para substituir ou atualizar um conjunto de chips de memória.</span><span class="sxs-lookup"><span data-stu-id="4c789-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c789-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4c789-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4c789-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4c789-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4c789-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4c789-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4c789-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4c789-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c789-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c789-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="4c789-112">Membros</span><span class="sxs-lookup"><span data-stu-id="4c789-112">Members</span></span>

<span data-ttu-id="4c789-113">A classe do tipo de **\_ substituição CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c789-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="4c789-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c789-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c789-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c789-115">Properties</span></span>

<span data-ttu-id="4c789-116">A classe de **\_ substituição do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c789-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c789-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4c789-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c789-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c789-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c789-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c789-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c789-120">Cadeia de caracteres de forma livre que especifica informações relacionadas a essa classe.</span><span class="sxs-lookup"><span data-stu-id="4c789-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="4c789-121">A finalidade do conjunto ou das informações relacionadas a como os elementos do componente são substituídos pode ser incluída nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4c789-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="4c789-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4c789-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c789-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c789-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c789-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c789-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c789-125">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4c789-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c789-126">Cadeia de caracteres de forma livre que define um rótulo para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4c789-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="4c789-127">Essa propriedade é a chave para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4c789-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c789-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c789-128">Remarks</span></span>

<span data-ttu-id="4c789-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="4c789-129">WMI does not implement this class.</span></span>

<span data-ttu-id="4c789-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4c789-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4c789-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4c789-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c789-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c789-132">Requirements</span></span>



| <span data-ttu-id="4c789-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c789-133">Requirement</span></span> | <span data-ttu-id="4c789-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4c789-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c789-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c789-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4c789-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c789-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c789-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c789-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4c789-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c789-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c789-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c789-139">Namespace</span></span><br/>                | <span data-ttu-id="4c789-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4c789-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c789-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4c789-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c789-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c789-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c789-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4c789-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c789-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c789-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

