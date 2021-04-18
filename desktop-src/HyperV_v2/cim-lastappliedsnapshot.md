---
description: Representa uma associação entre um sistema de computador e seu instantâneo de sistema virtual aplicado mais recentemente.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: Classe CIM_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810365"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="6cc29-103">\_Classe CIM LastAppliedSnapshot</span><span class="sxs-lookup"><span data-stu-id="6cc29-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="6cc29-104">Representa uma associação entre um sistema de computador e seu instantâneo de sistema virtual aplicado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="6cc29-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc29-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cc29-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6cc29-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6cc29-106">Members</span></span>

<span data-ttu-id="6cc29-107">A classe **CIM \_ LastAppliedSnapshot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6cc29-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="6cc29-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6cc29-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cc29-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6cc29-109">Properties</span></span>

<span data-ttu-id="6cc29-110">A classe **CIM \_ LastAppliedSnapshot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6cc29-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cc29-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6cc29-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cc29-112">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="6cc29-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6cc29-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cc29-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cc29-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6cc29-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6cc29-115">O instantâneo do sistema virtual que foi aplicado pela última vez no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="6cc29-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6cc29-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6cc29-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cc29-117">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="6cc29-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6cc29-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cc29-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cc29-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="6cc29-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6cc29-120">O sistema do computador.</span><span class="sxs-lookup"><span data-stu-id="6cc29-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cc29-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cc29-121">Requirements</span></span>



| <span data-ttu-id="6cc29-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cc29-122">Requirement</span></span> | <span data-ttu-id="6cc29-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6cc29-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc29-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cc29-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc29-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6cc29-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6cc29-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cc29-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc29-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cc29-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6cc29-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6cc29-128">Namespace</span></span><br/>                | <span data-ttu-id="6cc29-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6cc29-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6cc29-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6cc29-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cc29-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cc29-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cc29-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc29-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cc29-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cc29-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6cc29-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cc29-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc29-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="6cc29-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

