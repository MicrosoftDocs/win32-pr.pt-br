---
description: Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Classe Msvm_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783292"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="ac0af-103">\_Classe Msvm LastAppliedSnapshot</span><span class="sxs-lookup"><span data-stu-id="ac0af-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="ac0af-104">Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="ac0af-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="ac0af-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ac0af-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac0af-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac0af-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ac0af-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ac0af-107">Members</span></span>

<span data-ttu-id="ac0af-108">A classe **Msvm \_ LastAppliedSnapshot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ac0af-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="ac0af-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac0af-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac0af-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac0af-110">Properties</span></span>

<span data-ttu-id="ac0af-111">A classe **Msvm \_ LastAppliedSnapshot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac0af-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac0af-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ac0af-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0af-113">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="ac0af-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ac0af-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac0af-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac0af-115">Qualificadores: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="ac0af-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="ac0af-116">Referência a uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual que foi aplicado pela última vez ao sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="ac0af-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="ac0af-117">Essa propriedade é herdada **da \_ dependência CIM**.</span><span class="sxs-lookup"><span data-stu-id="ac0af-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="ac0af-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ac0af-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0af-119">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="ac0af-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ac0af-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac0af-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac0af-121">Qualificadores: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="ac0af-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="ac0af-122">Referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema virtual no qual o instantâneo do sistema virtual representado pela propriedade **Antecedent** foi aplicado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="ac0af-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="ac0af-123">Essa propriedade é herdada **da \_ dependência CIM**.</span><span class="sxs-lookup"><span data-stu-id="ac0af-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac0af-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac0af-124">Requirements</span></span>



| <span data-ttu-id="ac0af-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac0af-125">Requirement</span></span> | <span data-ttu-id="ac0af-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ac0af-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0af-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac0af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0af-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac0af-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac0af-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac0af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0af-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac0af-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac0af-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac0af-131">Namespace</span></span><br/>                | <span data-ttu-id="ac0af-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ac0af-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac0af-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ac0af-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac0af-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac0af-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac0af-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ac0af-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac0af-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac0af-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




