---
description: Representa uma associação na qual um serviço de ponte é um componente de um serviço de comutador.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: Classe CIM_SwitchServiceTransparentBridging
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780540"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="4102f-103">\_Classe CIM SwitchServiceTransparentBridging</span><span class="sxs-lookup"><span data-stu-id="4102f-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="4102f-104">Representa uma associação na qual um serviço de ponte é um componente de um serviço de comutador.</span><span class="sxs-lookup"><span data-stu-id="4102f-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4102f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4102f-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4102f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4102f-106">Members</span></span>

<span data-ttu-id="4102f-107">A classe **CIM \_ SwitchServiceTransparentBridging** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4102f-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="4102f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4102f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4102f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4102f-109">Properties</span></span>

<span data-ttu-id="4102f-110">A classe **CIM \_ SwitchServiceTransparentBridging** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4102f-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4102f-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4102f-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4102f-112">Tipo de dados: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="4102f-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="4102f-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4102f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4102f-114">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4102f-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4102f-115">Uma referência do [**CIM \_ SwitchService**](cim-switchservice.md) ao serviço de comutador.</span><span class="sxs-lookup"><span data-stu-id="4102f-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="4102f-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4102f-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4102f-117">Tipo de dados: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="4102f-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="4102f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4102f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4102f-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4102f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4102f-120">Uma referência do [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) ao serviço de ponte do componente.</span><span class="sxs-lookup"><span data-stu-id="4102f-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4102f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4102f-121">Requirements</span></span>



| <span data-ttu-id="4102f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4102f-122">Requirement</span></span> | <span data-ttu-id="4102f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4102f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4102f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4102f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4102f-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4102f-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4102f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4102f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4102f-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4102f-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4102f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4102f-128">Namespace</span></span><br/>                | <span data-ttu-id="4102f-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4102f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4102f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4102f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4102f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4102f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4102f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4102f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4102f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4102f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4102f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4102f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4102f-135">**Imcomponente CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4102f-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

