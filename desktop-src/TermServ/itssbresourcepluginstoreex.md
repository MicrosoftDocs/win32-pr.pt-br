---
title: Interface ITsSbResourcePluginStoreEx
description: Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota da interface ITsSbResourcePluginStoreEx, descrita
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085761"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="d8467-105">Interface ITsSbResourcePluginStoreEx</span><span class="sxs-lookup"><span data-stu-id="d8467-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="d8467-106">Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.</span><span class="sxs-lookup"><span data-stu-id="d8467-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="d8467-107">Esses métodos adicionam, excluem e consultam esses objetos.</span><span class="sxs-lookup"><span data-stu-id="d8467-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="d8467-108">Essa interface só está disponível no Windows Server 2012 R2 com o [KB3091411](https://support.microsoft.com/kb/3091411) instalado.</span><span class="sxs-lookup"><span data-stu-id="d8467-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="d8467-109">Os métodos [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) e [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) da interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) estão disponíveis a partir do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d8467-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="d8467-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d8467-110">Members</span></span>

<span data-ttu-id="d8467-111">A interface **ITsSbResourcePluginStoreEx** herda de [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="d8467-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="d8467-112">**ITsSbResourcePluginStoreEx** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8467-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="d8467-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d8467-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8467-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d8467-114">Methods</span></span>

<span data-ttu-id="d8467-115">A interface **ITsSbResourcePluginStoreEx** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d8467-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="d8467-116">Método</span><span class="sxs-lookup"><span data-stu-id="d8467-116">Method</span></span>                                                                                                            | <span data-ttu-id="d8467-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8467-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8467-118">**AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="d8467-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="d8467-119">Bloqueia um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d8467-120">**AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="d8467-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="d8467-121">Adiciona um ambiente ao armazenamento de plug-in de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="d8467-122">**AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="d8467-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="d8467-123">Adiciona uma nova sessão ao armazenamento de plug-in de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="d8467-124">**AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="d8467-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="d8467-125">Adiciona um destino ao armazenamento de plug-in de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="d8467-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="d8467-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="d8467-127">Exclui um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="d8467-128">**EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="d8467-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="d8467-129">Retorna uma matriz que contém os ambientes presentes no repositório de plug-ins de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="d8467-130">**EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="d8467-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="d8467-131">Enumera todos os farms que foram adicionados ao armazenamento de plug-in de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="d8467-132">**EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="d8467-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="d8467-133">Enumera um conjunto de sessões especificado.</span><span class="sxs-lookup"><span data-stu-id="d8467-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="d8467-134">**EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="d8467-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="d8467-135">Retorna uma matriz que contém os destinos especificados que estão presentes no repositório de plug-ins de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="d8467-136">**Getfarmproperty**</span><span class="sxs-lookup"><span data-stu-id="d8467-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="d8467-137">Recupera uma propriedade de um farm.</span><span class="sxs-lookup"><span data-stu-id="d8467-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="d8467-138">**QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d8467-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="d8467-139">Retorna o objeto de ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="d8467-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="d8467-140">**QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="d8467-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="d8467-141">Retorna o objeto de sessão que tem a ID de sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="d8467-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="d8467-142">**QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="d8467-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="d8467-143">Retorna o destino que tem o nome de destino e o nome do farm especificados.</span><span class="sxs-lookup"><span data-stu-id="d8467-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="d8467-144">**ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="d8467-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="d8467-145">Libera um bloqueio em um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="d8467-146">**RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="d8467-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="d8467-147">Remove o ambiente especificado do armazenamento de plug-in de recurso.</span><span class="sxs-lookup"><span data-stu-id="d8467-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="d8467-148">**SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d8467-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="d8467-149">Salva um ambiente.</span><span class="sxs-lookup"><span data-stu-id="d8467-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="d8467-150">**SaveSession**</span><span class="sxs-lookup"><span data-stu-id="d8467-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="d8467-151">Salva uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d8467-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="d8467-152">**SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="d8467-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="d8467-153">Salva um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d8467-154">**Setenvironmentproperty**</span><span class="sxs-lookup"><span data-stu-id="d8467-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="d8467-155">Define uma propriedade em um ambiente.</span><span class="sxs-lookup"><span data-stu-id="d8467-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="d8467-156">**SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="d8467-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="d8467-157">Define uma propriedade em um ambiente.</span><span class="sxs-lookup"><span data-stu-id="d8467-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="d8467-158">**Setsessionstate**</span><span class="sxs-lookup"><span data-stu-id="d8467-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="d8467-159">Define o estado de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d8467-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="d8467-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="d8467-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="d8467-161">Define uma propriedade em um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="d8467-162">**SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="d8467-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="d8467-163">Define uma propriedade em um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="d8467-164">**Settargetstate**</span><span class="sxs-lookup"><span data-stu-id="d8467-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="d8467-165">Define o estado de um destino.</span><span class="sxs-lookup"><span data-stu-id="d8467-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="d8467-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8467-166">Requirements</span></span>



| <span data-ttu-id="d8467-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8467-167">Requirement</span></span> | <span data-ttu-id="d8467-168">Valor</span><span class="sxs-lookup"><span data-stu-id="d8467-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8467-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8467-169">Minimum supported client</span></span><br/> | <span data-ttu-id="d8467-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d8467-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8467-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8467-171">Minimum supported server</span></span><br/> | <span data-ttu-id="d8467-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d8467-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="d8467-173">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d8467-173">End of server support</span></span><br/>    | <span data-ttu-id="d8467-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d8467-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="d8467-175">IID</span><span class="sxs-lookup"><span data-stu-id="d8467-175">IID</span></span><br/>                      | <span data-ttu-id="d8467-176">IID \_ ITsSbResourcePluginStoreEx é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="d8467-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8467-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8467-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8467-178">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="d8467-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="d8467-179">Interfaces de virtualização Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="d8467-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





