---
description: Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Classe Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768748"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="a981d-103">\_Classe Msvm OwningJobElement</span><span class="sxs-lookup"><span data-stu-id="a981d-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="a981d-104">Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a981d-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="a981d-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a981d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a981d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a981d-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="a981d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a981d-107">Members</span></span>

<span data-ttu-id="a981d-108">A classe **Msvm \_ OwningJobElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a981d-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a981d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a981d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a981d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a981d-110">Properties</span></span>

<span data-ttu-id="a981d-111">A classe **Msvm \_ OwningJobElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a981d-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a981d-112">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="a981d-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a981d-113">Tipo de dados: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="a981d-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a981d-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a981d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a981d-115">O trabalho criado pelo elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a981d-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="a981d-116">**Propriedade proprietária**</span><span class="sxs-lookup"><span data-stu-id="a981d-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a981d-117">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="a981d-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="a981d-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a981d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a981d-119">O elemento gerenciado responsável pela criação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a981d-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a981d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a981d-120">Requirements</span></span>



| <span data-ttu-id="a981d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a981d-121">Requirement</span></span> | <span data-ttu-id="a981d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a981d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a981d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a981d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a981d-124">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a981d-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a981d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a981d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a981d-126">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a981d-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a981d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a981d-127">Namespace</span></span><br/>                | <span data-ttu-id="a981d-128">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a981d-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a981d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a981d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a981d-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a981d-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a981d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a981d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a981d-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a981d-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

