---
description: Representa uma associação entre um ponto de acesso de serviço (SAP) e um dispositivo lógico que o implementa.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Classe CIM_DeviceSAPImplementation (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787115"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="e8eb2-103">Classe CIM_DeviceSAPImplementation (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e8eb2-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="e8eb2-104">Representa uma associação entre um ponto de acesso de serviço (SAP) e um dispositivo lógico que o implementa.</span><span class="sxs-lookup"><span data-stu-id="e8eb2-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8eb2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8eb2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e8eb2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e8eb2-106">Members</span></span>

<span data-ttu-id="e8eb2-107">A classe **CIM \_ DeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e8eb2-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="e8eb2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e8eb2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8eb2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e8eb2-109">Properties</span></span>

<span data-ttu-id="e8eb2-110">A classe **CIM \_ DeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e8eb2-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8eb2-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e8eb2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8eb2-112">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="e8eb2-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e8eb2-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e8eb2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8eb2-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e8eb2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e8eb2-115">O dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e8eb2-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e8eb2-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e8eb2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8eb2-117">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="e8eb2-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="e8eb2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e8eb2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8eb2-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e8eb2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e8eb2-120">O SAP implementado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e8eb2-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8eb2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8eb2-121">Requirements</span></span>



| <span data-ttu-id="e8eb2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8eb2-122">Requirement</span></span> | <span data-ttu-id="e8eb2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e8eb2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8eb2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8eb2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e8eb2-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e8eb2-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e8eb2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8eb2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e8eb2-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8eb2-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e8eb2-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8eb2-128">Namespace</span></span><br/>                | <span data-ttu-id="e8eb2-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e8eb2-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8eb2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e8eb2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8eb2-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8eb2-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8eb2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e8eb2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8eb2-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8eb2-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8eb2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8eb2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8eb2-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="e8eb2-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

