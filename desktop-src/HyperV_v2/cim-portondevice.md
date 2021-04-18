---
description: Representa uma associação entre uma porta ou um ponto de conexão e um dispositivo.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: Classe CIM_PortOnDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764692"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="677c7-103">\_Classe CIM PortOnDevice</span><span class="sxs-lookup"><span data-stu-id="677c7-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="677c7-104">Representa uma associação entre uma porta ou um ponto de conexão e um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="677c7-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="677c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="677c7-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="677c7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="677c7-106">Members</span></span>

<span data-ttu-id="677c7-107">A classe **CIM \_ PortOnDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="677c7-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="677c7-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="677c7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="677c7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="677c7-109">Properties</span></span>

<span data-ttu-id="677c7-110">A classe **CIM \_ PortOnDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="677c7-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="677c7-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="677c7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="677c7-112">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="677c7-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="677c7-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="677c7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="677c7-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="677c7-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="677c7-115">O dispositivo que inclui a porta.</span><span class="sxs-lookup"><span data-stu-id="677c7-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="677c7-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="677c7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="677c7-117">Tipo de dados: **CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="677c7-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="677c7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="677c7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="677c7-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="677c7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="677c7-120">A porta no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="677c7-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="677c7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="677c7-121">Requirements</span></span>



| <span data-ttu-id="677c7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="677c7-122">Requirement</span></span> | <span data-ttu-id="677c7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="677c7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="677c7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="677c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="677c7-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="677c7-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="677c7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="677c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="677c7-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="677c7-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="677c7-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="677c7-128">Namespace</span></span><br/>                | <span data-ttu-id="677c7-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="677c7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="677c7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="677c7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="677c7-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="677c7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="677c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="677c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677c7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="677c7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="677c7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="677c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677c7-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="677c7-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

