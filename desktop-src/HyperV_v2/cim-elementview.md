---
description: Representa e associação entre uma exibição e uma instância que representa a exibição normalizada de um recurso gerenciado.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Classe CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755117"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="b6497-103">\_Classe CIM ElementView</span><span class="sxs-lookup"><span data-stu-id="b6497-103">CIM\_ElementView class</span></span>

<span data-ttu-id="b6497-104">Representa e associação entre uma exibição e uma instância que representa a exibição normalizada de um recurso gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b6497-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6497-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6497-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b6497-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b6497-106">Members</span></span>

<span data-ttu-id="b6497-107">A classe **CIM \_ ElementView** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b6497-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="b6497-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6497-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6497-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6497-109">Properties</span></span>

<span data-ttu-id="b6497-110">A classe **CIM \_ ElementView** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6497-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6497-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b6497-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6497-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="b6497-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="b6497-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6497-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6497-114">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="b6497-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b6497-115">A instância que representa a exibição normalizada do recurso gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b6497-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="b6497-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b6497-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6497-117">Tipo de dados **: \_ exibição CIM**</span><span class="sxs-lookup"><span data-stu-id="b6497-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="b6497-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6497-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6497-119">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b6497-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b6497-120">A exibição que representa uma exibição de não normalizada ou agregada do recurso gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b6497-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6497-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6497-121">Requirements</span></span>



| <span data-ttu-id="b6497-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6497-122">Requirement</span></span> | <span data-ttu-id="b6497-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b6497-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6497-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6497-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6497-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b6497-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b6497-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6497-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6497-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b6497-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b6497-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6497-128">Namespace</span></span><br/>                | <span data-ttu-id="b6497-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b6497-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6497-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b6497-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6497-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6497-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6497-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b6497-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6497-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6497-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6497-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6497-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6497-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b6497-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

