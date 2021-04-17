---
description: Representa uma associação entre um trabalho e o elemento gerenciado que criou o trabalho.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758343"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="39be8-103">\_Classe CIM OwningJobElement</span><span class="sxs-lookup"><span data-stu-id="39be8-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="39be8-104">Representa uma associação entre um trabalho e o elemento gerenciado que criou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="39be8-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="39be8-105">Como um trabalho pode ser movido entre sistemas, e o elemento gerenciado pode não existir durante toda a duração do trabalho, em alguns casos, essa associação pode não ser possível ou só pode existir para uma parte da existência do trabalho.</span><span class="sxs-lookup"><span data-stu-id="39be8-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="39be8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39be8-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="39be8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="39be8-107">Members</span></span>

<span data-ttu-id="39be8-108">A classe **CIM \_ OwningJobElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39be8-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="39be8-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39be8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39be8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39be8-110">Properties</span></span>

<span data-ttu-id="39be8-111">A classe **CIM \_ OwningJobElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39be8-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39be8-112">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="39be8-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39be8-113">Tipo de dados **: \_ trabalho do CIM**</span><span class="sxs-lookup"><span data-stu-id="39be8-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="39be8-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39be8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39be8-115">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39be8-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39be8-116">Uma referência ao trabalho criado pelo elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="39be8-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="39be8-117">**Propriedade proprietária**</span><span class="sxs-lookup"><span data-stu-id="39be8-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39be8-118">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="39be8-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="39be8-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39be8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39be8-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="39be8-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="39be8-121">Uma referência ao elemento gerenciado que criou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="39be8-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39be8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39be8-122">Requirements</span></span>



| <span data-ttu-id="39be8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="39be8-123">Requirement</span></span> | <span data-ttu-id="39be8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="39be8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39be8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39be8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39be8-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="39be8-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="39be8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39be8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39be8-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39be8-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="39be8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="39be8-129">Namespace</span></span><br/>                | <span data-ttu-id="39be8-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="39be8-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="39be8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="39be8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39be8-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39be8-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39be8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="39be8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39be8-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39be8-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

