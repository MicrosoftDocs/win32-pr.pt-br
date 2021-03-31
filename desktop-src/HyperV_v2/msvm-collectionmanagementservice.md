---
description: Gerencia as coleções no host do Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663487"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="1a734-103">\_Classe Msvm CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="1a734-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="1a734-104">Gerencia as coleções no host do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1a734-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="1a734-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1a734-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a734-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a734-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="1a734-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1a734-107">Members</span></span>

<span data-ttu-id="1a734-108">A classe **Msvm \_ CollectionManagementService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a734-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="1a734-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1a734-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1a734-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1a734-110">Methods</span></span>

<span data-ttu-id="1a734-111">A classe **Msvm \_ CollectionManagementService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1a734-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="1a734-112">Método</span><span class="sxs-lookup"><span data-stu-id="1a734-112">Method</span></span>                                                                          | <span data-ttu-id="1a734-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a734-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a734-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="1a734-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="1a734-115">Adiciona o Managedelement especificado como um membro do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a734-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1a734-116">**Definocollection**</span><span class="sxs-lookup"><span data-stu-id="1a734-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="1a734-117">Cria um novo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="1a734-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="1a734-118">**Destruicollection**</span><span class="sxs-lookup"><span data-stu-id="1a734-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="1a734-119">Exclui o objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a734-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="1a734-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="1a734-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="1a734-121">Remove o Managedelement especificado como um membro do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a734-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="1a734-122">**RemoveMemberById**</span><span class="sxs-lookup"><span data-stu-id="1a734-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="1a734-123">Remove o Managedelement especificado como um membro do [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) com o identificador fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a734-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="1a734-124">Isso terá sucesso mesmo se o objeto com esse identificador não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="1a734-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="1a734-125">**Renomecollection**</span><span class="sxs-lookup"><span data-stu-id="1a734-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="1a734-126">Atualiza o ElementName do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a734-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="1a734-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1a734-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="1a734-128">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="1a734-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="1a734-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1a734-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="1a734-130">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="1a734-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="1a734-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a734-131">Requirements</span></span>



| <span data-ttu-id="1a734-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a734-132">Requirement</span></span> | <span data-ttu-id="1a734-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1a734-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a734-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a734-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1a734-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a734-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1a734-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a734-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1a734-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1a734-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1a734-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a734-138">Namespace</span></span><br/>                | <span data-ttu-id="1a734-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1a734-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a734-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1a734-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a734-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a734-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a734-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1a734-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a734-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a734-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a734-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a734-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a734-145">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="1a734-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




