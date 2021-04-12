---
description: A \_ classe de associação CIM CollectedMSEs representa os membros do objeto GROUPING, uma classe CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: Classe CIM_CollectedMSEs (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457080"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="98510-103">Classe CIM_CollectedMSEs (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="98510-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="98510-104">A classe de associação **CIM \_ CollectedMSEs** representa os membros do objeto GROUPING, uma classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="98510-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98510-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="98510-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="98510-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="98510-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="98510-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="98510-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="98510-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="98510-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98510-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98510-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="98510-110">Membros</span><span class="sxs-lookup"><span data-stu-id="98510-110">Members</span></span>

<span data-ttu-id="98510-111">A classe **CIM \_ CollectedMSEs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="98510-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="98510-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98510-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98510-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98510-113">Properties</span></span>

<span data-ttu-id="98510-114">A classe **CIM \_ CollectedMSEs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="98510-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98510-115">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="98510-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98510-116">Tipo de dados: **cm \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="98510-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="98510-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98510-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98510-118">Referência ao objeto de agrupamento ou "recipiente" que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="98510-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="98510-119">**Membro**</span><span class="sxs-lookup"><span data-stu-id="98510-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98510-120">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="98510-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="98510-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98510-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98510-122">Referência a um membro da coleção.</span><span class="sxs-lookup"><span data-stu-id="98510-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98510-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="98510-123">Remarks</span></span>

<span data-ttu-id="98510-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="98510-124">WMI does not implement this class.</span></span> <span data-ttu-id="98510-125">Para obter mais informações sobre classes WMI derivadas do **CIM \_ CollectedMSEs**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="98510-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="98510-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="98510-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98510-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="98510-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98510-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98510-128">Requirements</span></span>



| <span data-ttu-id="98510-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="98510-129">Requirement</span></span> | <span data-ttu-id="98510-130">Valor</span><span class="sxs-lookup"><span data-stu-id="98510-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98510-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98510-131">Minimum supported client</span></span><br/> | <span data-ttu-id="98510-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98510-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98510-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98510-133">Minimum supported server</span></span><br/> | <span data-ttu-id="98510-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98510-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98510-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="98510-135">Namespace</span></span><br/>                | <span data-ttu-id="98510-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="98510-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98510-137">MOF</span><span class="sxs-lookup"><span data-stu-id="98510-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98510-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98510-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98510-139">DLL</span><span class="sxs-lookup"><span data-stu-id="98510-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98510-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98510-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




