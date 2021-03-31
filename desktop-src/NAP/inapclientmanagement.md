---
title: Interface INapClientManagement (NapManagement. h)
description: Fornece métodos para o gerenciamento de cliente NAP. | Interface INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- INapClientManagement da interface NAP
- INapClientManagement interface NAP, descrita
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930438"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="2e4ff-106">Interface INapClientManagement</span><span class="sxs-lookup"><span data-stu-id="2e4ff-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="2e4ff-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2e4ff-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2e4ff-108">A interface **INapClientManagement** fornece métodos para o gerenciamento de cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="2e4ff-109">[**INapClientManagement2**](inapclientmanagement2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="2e4ff-110">Membros</span><span class="sxs-lookup"><span data-stu-id="2e4ff-110">Members</span></span>

<span data-ttu-id="2e4ff-111">A interface **INapClientManagement** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2e4ff-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e4ff-112">**INapClientManagement** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e4ff-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="2e4ff-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e4ff-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e4ff-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e4ff-114">Methods</span></span>

<span data-ttu-id="2e4ff-115">A interface **INapClientManagement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="2e4ff-116">Método</span><span class="sxs-lookup"><span data-stu-id="2e4ff-116">Method</span></span>                                                                                                                | <span data-ttu-id="2e4ff-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e4ff-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="2e4ff-118">**INapClientManagement::GetNapClientInfo**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="2e4ff-119">Recupera informações sobre um cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="2e4ff-120">**INapClientManagement::GetRegisteredEnforcementClients**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="2e4ff-121">Recupera informações sobre os clientes de imposição registrados.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="2e4ff-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="2e4ff-123">Recuperar informações sobre um SHA registrado.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="2e4ff-124">**INapClientManagement::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="2e4ff-125">Recupera informações sobre o estado de isolamento do cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="2e4ff-126">**INapClientManagement::RegisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="2e4ff-127">Registra um cliente de imposição com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="2e4ff-128">**INapClientManagement::RegisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="2e4ff-129">Registra um SHA com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="2e4ff-130">**INapClientManagement::UnregisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="2e4ff-131">Cancela o registro de um cliente de imposição com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="2e4ff-132">**INapClientManagement::UnregisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="2e4ff-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="2e4ff-133">Cancela o registro de um SHA com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="2e4ff-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e4ff-134">Requirements</span></span>



| <span data-ttu-id="2e4ff-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e4ff-135">Requirement</span></span> | <span data-ttu-id="2e4ff-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2e4ff-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4ff-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e4ff-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4ff-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e4ff-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2e4ff-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e4ff-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4ff-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e4ff-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2e4ff-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e4ff-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e4ff-142"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e4ff-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e4ff-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="2e4ff-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e4ff-144"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e4ff-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e4ff-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2e4ff-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4ff-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e4ff-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2e4ff-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e4ff-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4ff-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="2e4ff-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2e4ff-149">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="2e4ff-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

