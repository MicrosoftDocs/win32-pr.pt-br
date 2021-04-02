---
description: Representa uma associação na qual um serviço é um componente de um serviço pai, que, juntos, formam um serviço de nível superior.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: Classe CIM_ServiceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164625"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="f3d3e-103">\_Classe de Filecomponent CIM</span><span class="sxs-lookup"><span data-stu-id="f3d3e-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="f3d3e-104">Representa uma associação na qual um serviço é um componente de um serviço pai, que, juntos, formam um serviço de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f3d3e-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3d3e-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f3d3e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f3d3e-106">Members</span></span>

<span data-ttu-id="f3d3e-107">A classe **CIM \_ filecomponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f3d3e-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f3d3e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3d3e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3d3e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3d3e-109">Properties</span></span>

<span data-ttu-id="f3d3e-110">A classe **CIM \_ filecomponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f3d3e-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3d3e-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f3d3e-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d3e-112">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="f3d3e-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="f3d3e-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3d3e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3d3e-114">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="f3d3e-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f3d3e-115">O serviço pai.</span><span class="sxs-lookup"><span data-stu-id="f3d3e-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="f3d3e-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f3d3e-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d3e-117">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="f3d3e-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="f3d3e-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3d3e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3d3e-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f3d3e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f3d3e-120">O serviço de componente.</span><span class="sxs-lookup"><span data-stu-id="f3d3e-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3d3e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3d3e-121">Requirements</span></span>



| <span data-ttu-id="f3d3e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d3e-122">Requirement</span></span> | <span data-ttu-id="f3d3e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f3d3e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d3e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3d3e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d3e-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3d3e-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f3d3e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3d3e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d3e-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f3d3e-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f3d3e-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3d3e-128">Namespace</span></span><br/>                | <span data-ttu-id="f3d3e-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f3d3e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3d3e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f3d3e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3d3e-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3d3e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3d3e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d3e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3d3e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3d3e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3d3e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3d3e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d3e-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="f3d3e-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

