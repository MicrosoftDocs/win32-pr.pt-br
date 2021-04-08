---
description: A \_ classe CIM CollectedCollections é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Classe CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920434"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="d2dc0-103">\_Classe CIM CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="d2dc0-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="d2dc0-104">A classe **CIM \_ CollectedCollections** é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2dc0-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d2dc0-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d2dc0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d2dc0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d2dc0-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2dc0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2dc0-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="d2dc0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d2dc0-110">Members</span></span>

<span data-ttu-id="d2dc0-111">A classe **CIM \_ CollectedCollections** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d2dc0-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="d2dc0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d2dc0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2dc0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d2dc0-113">Properties</span></span>

<span data-ttu-id="d2dc0-114">A classe **CIM \_ CollectedCollections** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2dc0-115">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="d2dc0-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2dc0-116">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="d2dc0-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="d2dc0-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2dc0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2dc0-118">Referência ao elemento "nível superior" ou pai na agregação.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="d2dc0-119">**CollectionInCollection**</span><span class="sxs-lookup"><span data-stu-id="d2dc0-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2dc0-120">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="d2dc0-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="d2dc0-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2dc0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2dc0-122">Referência à **coleção**"coletada".</span><span class="sxs-lookup"><span data-stu-id="d2dc0-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2dc0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2dc0-123">Remarks</span></span>

<span data-ttu-id="d2dc0-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-124">WMI does not implement this class.</span></span>

<span data-ttu-id="d2dc0-125">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d2dc0-126">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2dc0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2dc0-127">Requirements</span></span>



| <span data-ttu-id="d2dc0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2dc0-128">Requirement</span></span> | <span data-ttu-id="d2dc0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d2dc0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2dc0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2dc0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d2dc0-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2dc0-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2dc0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2dc0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d2dc0-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2dc0-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2dc0-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2dc0-134">Namespace</span></span><br/>                | <span data-ttu-id="d2dc0-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2dc0-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2dc0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d2dc0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2dc0-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2dc0-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2dc0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d2dc0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2dc0-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2dc0-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




