---
description: Representa um serviço que controla a migração de sistemas virtuais entre sistemas de host. Essa classe também verifica se uma migração pendente provavelmente terá sucesso.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828116"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="36aa1-104">\_Classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="36aa1-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="36aa1-105">Representa um serviço que controla a migração de sistemas virtuais entre sistemas de host.</span><span class="sxs-lookup"><span data-stu-id="36aa1-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="36aa1-106">Essa classe também verifica se uma migração pendente provavelmente terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="36aa1-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="36aa1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36aa1-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="36aa1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="36aa1-108">Members</span></span>

<span data-ttu-id="36aa1-109">A classe **CIM \_ VirtualSystemMigrationService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="36aa1-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="36aa1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="36aa1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36aa1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="36aa1-111">Methods</span></span>

<span data-ttu-id="36aa1-112">A classe **CIM \_ VirtualSystemMigrationService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="36aa1-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="36aa1-113">Método</span><span class="sxs-lookup"><span data-stu-id="36aa1-113">Method</span></span>                                                                                                                     | <span data-ttu-id="36aa1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="36aa1-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36aa1-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="36aa1-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="36aa1-116">Verifica se uma migração de sistema virtual pendente para um host provavelmente terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="36aa1-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="36aa1-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="36aa1-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="36aa1-118">Verifica se uma migração de sistema virtual pendente para um sistema provavelmente será bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="36aa1-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="36aa1-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="36aa1-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="36aa1-120">Migra um sistema virtual para um host de destino.</span><span class="sxs-lookup"><span data-stu-id="36aa1-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="36aa1-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="36aa1-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="36aa1-122">Migra um sistema virtual para o sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="36aa1-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="36aa1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36aa1-123">Requirements</span></span>



| <span data-ttu-id="36aa1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="36aa1-124">Requirement</span></span> | <span data-ttu-id="36aa1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="36aa1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36aa1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36aa1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36aa1-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="36aa1-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="36aa1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36aa1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36aa1-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36aa1-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="36aa1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="36aa1-130">Namespace</span></span><br/>                | <span data-ttu-id="36aa1-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="36aa1-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36aa1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="36aa1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36aa1-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36aa1-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36aa1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="36aa1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36aa1-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36aa1-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36aa1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="36aa1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36aa1-137">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="36aa1-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




