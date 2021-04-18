---
description: Uma associação entre uma instância de Msvm \_ VirtualSystemSettingData e a \_ instância VirtualSystemSettingData Msvm que representa o instantâneo mais recente no qual esse objeto se baseia.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Classe Msvm_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764683"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="1216a-103">\_Classe Msvm ParentChildSettingData</span><span class="sxs-lookup"><span data-stu-id="1216a-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="1216a-104">Uma associação entre uma instância de [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) e a **instância \_ VirtualSystemSettingData Msvm** que representa o instantâneo mais recente no qual esse objeto se baseia.</span><span class="sxs-lookup"><span data-stu-id="1216a-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="1216a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1216a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1216a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1216a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1216a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1216a-107">Members</span></span>

<span data-ttu-id="1216a-108">A classe **Msvm \_ ParentChildSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1216a-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1216a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1216a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1216a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1216a-110">Properties</span></span>

<span data-ttu-id="1216a-111">A classe **Msvm \_ ParentChildSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1216a-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1216a-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1216a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1216a-113">Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="1216a-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1216a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1216a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1216a-115">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1216a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1216a-116">Os dados de configuração de instantâneo nos quais os dados de configuração filho se baseiam.</span><span class="sxs-lookup"><span data-stu-id="1216a-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="1216a-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1216a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1216a-118">Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="1216a-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1216a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1216a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1216a-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="1216a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1216a-121">Os dados de configuração para a máquina virtual que representa o filho do pai.</span><span class="sxs-lookup"><span data-stu-id="1216a-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1216a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1216a-122">Remarks</span></span>

<span data-ttu-id="1216a-123">O acesso à classe **Msvm \_ ParentChildSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="1216a-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1216a-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1216a-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1216a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1216a-125">Requirements</span></span>



| <span data-ttu-id="1216a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1216a-126">Requirement</span></span> | <span data-ttu-id="1216a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1216a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1216a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1216a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1216a-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1216a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1216a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1216a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1216a-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1216a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1216a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1216a-132">Namespace</span></span><br/>                | <span data-ttu-id="1216a-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1216a-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1216a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1216a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1216a-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1216a-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1216a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1216a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1216a-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1216a-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1216a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1216a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1216a-139">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1216a-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="1216a-140">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1216a-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="1216a-141">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="1216a-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

