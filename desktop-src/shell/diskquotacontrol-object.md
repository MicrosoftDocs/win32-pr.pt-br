---
description: Permite que um administrador gerencie as propriedades de cota de disco de um volume.
title: Objeto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841547"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="43970-103">Objeto DiskQuotaControl</span><span class="sxs-lookup"><span data-stu-id="43970-103">DiskQuotaControl object</span></span>

<span data-ttu-id="43970-104">Permite que um administrador gerencie as propriedades de cota de disco de um volume.</span><span class="sxs-lookup"><span data-stu-id="43970-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="43970-105">O sistema de arquivos NTFS permite que um administrador gerencie o uso de disco em um volume compartilhado alocando uma quantidade especificada de espaço em disco ou limite de cota *para* cada usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="43970-106">Você pode usar esse objeto para definir o limite de cota padrão que será atribuído automaticamente a todos os novos usuários.</span><span class="sxs-lookup"><span data-stu-id="43970-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="43970-107">Membros</span><span class="sxs-lookup"><span data-stu-id="43970-107">Members</span></span>

<span data-ttu-id="43970-108">O **objeto DiskQuotaControl** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43970-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="43970-109">Eventos</span><span class="sxs-lookup"><span data-stu-id="43970-109">Events</span></span>](#events)
-   [<span data-ttu-id="43970-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="43970-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="43970-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43970-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="43970-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="43970-112">Events</span></span>

<span data-ttu-id="43970-113">O **objeto DiskQuotaControl** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="43970-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="43970-114">Evento</span><span class="sxs-lookup"><span data-stu-id="43970-114">Event</span></span>                                                           | <span data-ttu-id="43970-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="43970-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43970-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="43970-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="43970-117">Ocorre quando as informações de nome de [**um objeto DIDiskQuotaUser**](didiskquotauser-object.md) foram resolvidas.</span><span class="sxs-lookup"><span data-stu-id="43970-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="43970-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="43970-118">Methods</span></span>

<span data-ttu-id="43970-119">O **objeto DiskQuotaControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="43970-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="43970-120">Método</span><span class="sxs-lookup"><span data-stu-id="43970-120">Method</span></span>                                                                                    | <span data-ttu-id="43970-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="43970-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43970-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="43970-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="43970-123">Atribui uma cota de disco não padrão a um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="43970-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="43970-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="43970-125">Exclui um usuário do volume.</span><span class="sxs-lookup"><span data-stu-id="43970-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="43970-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="43970-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="43970-127">Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.</span><span class="sxs-lookup"><span data-stu-id="43970-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="43970-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="43970-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="43970-129">Coloca o objeto de usuário especificado ao lado na linha para resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="43970-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="43970-130">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="43970-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="43970-131">Abre um volume especificado e inicializa seu objeto de controle de cota.</span><span class="sxs-lookup"><span data-stu-id="43970-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="43970-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="43970-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="43970-133">Invalida o cache de nome de usuário da ID de segurança.</span><span class="sxs-lookup"><span data-stu-id="43970-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="43970-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="43970-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="43970-135">Desliga o thread de resolução de nomes de usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="43970-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="43970-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="43970-137">Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="43970-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="43970-138">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43970-138">Properties</span></span>

<span data-ttu-id="43970-139">O objeto **DiskQuotaControl** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43970-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="43970-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="43970-140">Property</span></span>                                                                                   | <span data-ttu-id="43970-141">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="43970-141">Access type</span></span>           | <span data-ttu-id="43970-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="43970-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43970-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="43970-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="43970-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-144">Read/write</span></span><br/> | <span data-ttu-id="43970-145">Define ou Obtém o limite de cota padrão.</span><span class="sxs-lookup"><span data-stu-id="43970-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="43970-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="43970-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="43970-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43970-147">Read-only</span></span><br/>  | <span data-ttu-id="43970-148">Obtém o limite de cota padrão como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="43970-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="43970-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="43970-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="43970-150">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-150">Read/write</span></span><br/> | <span data-ttu-id="43970-151">Define ou Obtém o limite de cota padrão.</span><span class="sxs-lookup"><span data-stu-id="43970-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="43970-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="43970-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="43970-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43970-153">Read-only</span></span><br/>  | <span data-ttu-id="43970-154">Obtém o limite de cota padrão como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="43970-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="43970-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="43970-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="43970-156">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-156">Read/write</span></span><br/> | <span data-ttu-id="43970-157">Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.</span><span class="sxs-lookup"><span data-stu-id="43970-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="43970-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="43970-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="43970-159">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-159">Read/write</span></span><br/> | <span data-ttu-id="43970-160">Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.</span><span class="sxs-lookup"><span data-stu-id="43970-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="43970-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="43970-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="43970-162">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43970-162">Read-only</span></span><br/>  | <span data-ttu-id="43970-163">Obtém um valor booliano que indica se o arquivo de cota do volume está concluído.</span><span class="sxs-lookup"><span data-stu-id="43970-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="43970-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="43970-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="43970-165">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43970-165">Read-only</span></span><br/>  | <span data-ttu-id="43970-166">Obtém um valor booliana que indica se o arquivo de cota para o volume está sendo reconstruído no momento.</span><span class="sxs-lookup"><span data-stu-id="43970-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="43970-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="43970-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="43970-168">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-168">Read/write</span></span><br/> | <span data-ttu-id="43970-169">Define ou obtém o estado das cotas de disco do volume.</span><span class="sxs-lookup"><span data-stu-id="43970-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="43970-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="43970-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="43970-171">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="43970-171">Read/write</span></span><br/> | <span data-ttu-id="43970-172">Define ou obtém um valor que controla como o SID do usuário é resolvido para nomes de usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="43970-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="43970-173">Remarks</span></span>

<span data-ttu-id="43970-174">Um administrador pode usar o **objeto DiskQuotaControl** para realizar várias tarefas, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="43970-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="43970-175">Habilitando e desabilitando o sistema de cota de disco do volume.</span><span class="sxs-lookup"><span data-stu-id="43970-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="43970-176">Obtendo o status do sistema de cota no volume.</span><span class="sxs-lookup"><span data-stu-id="43970-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="43970-177">Negar espaço em disco para usuários que excedem o limite de cota.</span><span class="sxs-lookup"><span data-stu-id="43970-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="43970-178">Especificando os valores padrão de limite de aviso e limite de cota que serão atribuídos a novos usuários.</span><span class="sxs-lookup"><span data-stu-id="43970-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="43970-179">Adicionar e remover usuários.</span><span class="sxs-lookup"><span data-stu-id="43970-179">Adding and removing users.</span></span>

<span data-ttu-id="43970-180">O **objeto DiskQuotaControl** permite definir valores padrão globais para o volume para propriedades como limites de cota.</span><span class="sxs-lookup"><span data-stu-id="43970-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="43970-181">No entanto, cada usuário é representado por [**um objeto DIDiskQuotaUser**](didiskquotauser-object.md) que pode ser usado para especificar configurações de cota individuais.</span><span class="sxs-lookup"><span data-stu-id="43970-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="43970-182">Há várias maneiras de obter o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) de um usuário:</span><span class="sxs-lookup"><span data-stu-id="43970-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="43970-183">Os [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) para todos os usuários com cotas no volume são expostos como uma coleção e podem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="43970-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="43970-184">Para uma discussão sobre como enumerar **objetos DIDiskQuotaUser,** consulte **Enumerando** usuários de cota de disco na seção Comentários de **DIDiskQuotaUser**.</span><span class="sxs-lookup"><span data-stu-id="43970-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="43970-185">Quando você adiciona um novo usuário, o [**método AddUser**](diskquotacontrol-adduser.md) retorna o objeto [**DIDiskQuotaUser do**](didiskquotauser-object.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="43970-186">Se você tiver o nome do usuário, o [**método FindUser**](diskquotacontrol-finduser.md) retornará o objeto [**DIDiskQuotaUser do**](didiskquotauser-object.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="43970-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="43970-187">Esse objeto disponibiliza a funcionalidade essencial da interface IDiskQuotaControl para scripts e aplicativos baseados Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="43970-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="43970-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43970-188">Requirements</span></span>



| <span data-ttu-id="43970-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="43970-189">Requirement</span></span> | <span data-ttu-id="43970-190">Valor</span><span class="sxs-lookup"><span data-stu-id="43970-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43970-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43970-191">Minimum supported client</span></span><br/> | <span data-ttu-id="43970-192">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43970-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43970-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43970-193">Minimum supported server</span></span><br/> | <span data-ttu-id="43970-194">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43970-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="43970-195">DLL</span><span class="sxs-lookup"><span data-stu-id="43970-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43970-196"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="43970-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43970-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="43970-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43970-198">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="43970-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




