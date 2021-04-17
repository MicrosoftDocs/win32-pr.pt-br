---
description: Uma associação entre uma instância do CIM \_ VirtualSystemSettingData e a \_ instância VIRTUALSYSTEMSETTINGDATA do CIM que representa o instantâneo mais recente no qual esse objeto se baseia.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791386"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="ee84a-103">\_Classe CIM ParentChildSettingData</span><span class="sxs-lookup"><span data-stu-id="ee84a-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="ee84a-104">Uma associação entre uma instância do [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) e a **instância \_ VirtualSystemSettingData do CIM** que representa o instantâneo mais recente no qual esse objeto se baseia.</span><span class="sxs-lookup"><span data-stu-id="ee84a-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee84a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ee84a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee84a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee84a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ee84a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ee84a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee84a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee84a-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="ee84a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ee84a-109">Members</span></span>

<span data-ttu-id="ee84a-110">A classe **CIM \_ ParentChildSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ee84a-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ee84a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ee84a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee84a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ee84a-112">Properties</span></span>

<span data-ttu-id="ee84a-113">A classe **CIM \_ ParentChildSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ee84a-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee84a-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ee84a-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee84a-115">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="ee84a-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="ee84a-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee84a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee84a-117">Referência ao objeto independente nesta associação.</span><span class="sxs-lookup"><span data-stu-id="ee84a-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="ee84a-118">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="ee84a-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="ee84a-119">**Filho**</span><span class="sxs-lookup"><span data-stu-id="ee84a-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee84a-120">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="ee84a-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ee84a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee84a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee84a-122">Os dados de configuração para o sistema virtual que representa o filho do pai.</span><span class="sxs-lookup"><span data-stu-id="ee84a-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="ee84a-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ee84a-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee84a-124">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="ee84a-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="ee84a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee84a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee84a-126">Referência ao objeto que é dependente da propriedade **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="ee84a-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="ee84a-127">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="ee84a-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="ee84a-128">**Pai**</span><span class="sxs-lookup"><span data-stu-id="ee84a-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee84a-129">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="ee84a-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ee84a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee84a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee84a-131">Os dados de configuração de instantâneo nos quais os dados de configuração filho se baseiam.</span><span class="sxs-lookup"><span data-stu-id="ee84a-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee84a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee84a-132">Requirements</span></span>



| <span data-ttu-id="ee84a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee84a-133">Requirement</span></span> | <span data-ttu-id="ee84a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ee84a-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="ee84a-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee84a-135">Namespace</span></span><br/> | <span data-ttu-id="ee84a-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ee84a-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee84a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee84a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee84a-138">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="ee84a-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

