---
description: Representa um serviço que gerencia sistemas virtuais.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768512"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="6665d-103">\_Classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="6665d-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6665d-104">Representa um serviço que gerencia sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6665d-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="6665d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6665d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="6665d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6665d-106">Members</span></span>

<span data-ttu-id="6665d-107">A classe **CIM \_ VirtualSystemManagementService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6665d-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="6665d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6665d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6665d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6665d-109">Methods</span></span>

<span data-ttu-id="6665d-110">A classe **CIM \_ VirtualSystemManagementService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6665d-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="6665d-111">Método</span><span class="sxs-lookup"><span data-stu-id="6665d-111">Method</span></span>                                                                                      | <span data-ttu-id="6665d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6665d-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6665d-113">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6665d-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="6665d-114">Adiciona recursos a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="6665d-115">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="6665d-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="6665d-116">Define um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="6665d-117">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="6665d-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="6665d-118">Exclui um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="6665d-119">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6665d-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="6665d-120">Modifica as configurações de recurso virtual para uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="6665d-121">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="6665d-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="6665d-122">Modifica as configurações do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="6665d-123">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6665d-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="6665d-124">Remove as configurações de recursos virtuais de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6665d-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="6665d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6665d-125">Requirements</span></span>



| <span data-ttu-id="6665d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6665d-126">Requirement</span></span> | <span data-ttu-id="6665d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6665d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6665d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6665d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6665d-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6665d-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6665d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6665d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6665d-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6665d-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6665d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6665d-132">Namespace</span></span><br/>                | <span data-ttu-id="6665d-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6665d-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6665d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6665d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6665d-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6665d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6665d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6665d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6665d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6665d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6665d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6665d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6665d-139">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="6665d-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




