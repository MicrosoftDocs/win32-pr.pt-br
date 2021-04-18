---
description: Usado para proteger partes individuais de um aplicativo em um ambiente bloqueado. Ele pode ser usado com a instalação de arquivos, chaves do registro e pastas criadas.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabela LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778563"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="c3b81-104">Tabela LockPermissions</span><span class="sxs-lookup"><span data-stu-id="c3b81-104">LockPermissions Table</span></span>

<span data-ttu-id="c3b81-105">A Tabela LockPermissions é usada para proteger partes individuais de um aplicativo em um ambiente bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c3b81-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="c3b81-106">Ele pode ser usado com a instalação de arquivos, chaves do registro e pastas criadas.</span><span class="sxs-lookup"><span data-stu-id="c3b81-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="c3b81-107">Um pacote destinado à instalação no Windows Server 2008 R2 ou no Windows 7 deve usar a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) em vez da Tabela LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c3b81-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="c3b81-108">Windows Installer versões anteriores a Windows Installer 5,0 ignoram a tabela MsiLockPermissionsEx.</span><span class="sxs-lookup"><span data-stu-id="c3b81-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="c3b81-109">Windows Installer 5,0 pode instalar um pacote que contém a Tabela LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c3b81-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="c3b81-110">A partir do Windows Installer 5,0, a instalação de um pacote que contém a tabela MsiLockPermissionsEx e a Tabela LockPermissions falha e retorna Windows Installer mensagem de erro 1941.</span><span class="sxs-lookup"><span data-stu-id="c3b81-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="c3b81-111">A Tabela LockPermissions tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3b81-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="c3b81-112">Coluna</span><span class="sxs-lookup"><span data-stu-id="c3b81-112">Column</span></span>     | <span data-ttu-id="c3b81-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3b81-113">Type</span></span>                               | <span data-ttu-id="c3b81-114">Chave</span><span class="sxs-lookup"><span data-stu-id="c3b81-114">Key</span></span> | <span data-ttu-id="c3b81-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="c3b81-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="c3b81-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="c3b81-116">LockObject</span></span> | [<span data-ttu-id="c3b81-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="c3b81-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="c3b81-118">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-118">Y</span></span>   | <span data-ttu-id="c3b81-119">N</span><span class="sxs-lookup"><span data-stu-id="c3b81-119">N</span></span>        |
| <span data-ttu-id="c3b81-120">Tabela</span><span class="sxs-lookup"><span data-stu-id="c3b81-120">Table</span></span>      | [<span data-ttu-id="c3b81-121">Text</span><span class="sxs-lookup"><span data-stu-id="c3b81-121">Text</span></span>](text.md)                   | <span data-ttu-id="c3b81-122">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-122">Y</span></span>   | <span data-ttu-id="c3b81-123">N</span><span class="sxs-lookup"><span data-stu-id="c3b81-123">N</span></span>        |
| <span data-ttu-id="c3b81-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="c3b81-124">Domain</span></span>     | [<span data-ttu-id="c3b81-125">Binário</span><span class="sxs-lookup"><span data-stu-id="c3b81-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="c3b81-126">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-126">Y</span></span>   | <span data-ttu-id="c3b81-127">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-127">Y</span></span>        |
| <span data-ttu-id="c3b81-128">Usuário</span><span class="sxs-lookup"><span data-stu-id="c3b81-128">User</span></span>       | [<span data-ttu-id="c3b81-129">Binário</span><span class="sxs-lookup"><span data-stu-id="c3b81-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="c3b81-130">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-130">Y</span></span>   | <span data-ttu-id="c3b81-131">N</span><span class="sxs-lookup"><span data-stu-id="c3b81-131">N</span></span>        |
| <span data-ttu-id="c3b81-132">Permissão</span><span class="sxs-lookup"><span data-stu-id="c3b81-132">Permission</span></span> | [<span data-ttu-id="c3b81-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="c3b81-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="c3b81-134">N</span><span class="sxs-lookup"><span data-stu-id="c3b81-134">N</span></span>   | <span data-ttu-id="c3b81-135">S</span><span class="sxs-lookup"><span data-stu-id="c3b81-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c3b81-136">Colunas</span><span class="sxs-lookup"><span data-stu-id="c3b81-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c3b81-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="c3b81-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="c3b81-138">Essa coluna e a coluna da tabela juntas especificam o arquivo, o diretório ou a chave do registro a ser protegida.</span><span class="sxs-lookup"><span data-stu-id="c3b81-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="c3b81-139">A coluna lockobject é uma chave estrangeira que aponta para a chave primária da tabela especificada pela coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="c3b81-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="c3b81-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="c3b81-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="c3b81-141">Essa coluna e a coluna lockobject especificam o arquivo, diretório ou chave do registro que deve ser protegido.</span><span class="sxs-lookup"><span data-stu-id="c3b81-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="c3b81-142">Na coluna tabela, insira arquivo, registro ou CreateFolder para especificar um lockobject listado na tabela de [arquivos](file-table.md), na [tabela de registro](registry-table.md)ou na [tabela CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3b81-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b81-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Controlador</span><span class="sxs-lookup"><span data-stu-id="c3b81-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="c3b81-144">A coluna que identifica o domínio do usuário para o qual as permissões devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="c3b81-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="c3b81-145">Esse é o nome de um computador autônomo ou um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="c3b81-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="c3b81-146">O tipo de dados da coluna é [formatado](formatted.md)e você pode usar a cadeia de caracteres \[ % UserDomain \] neste campo para obter o valor da variável de ambiente UserDomain para o domínio atual.</span><span class="sxs-lookup"><span data-stu-id="c3b81-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="c3b81-147">Para obter qualquer outro domínio, é necessário usar [ações personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c3b81-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="c3b81-148">Para obter mais informações, consulte a tabela de ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c3b81-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="c3b81-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Usuário</span><span class="sxs-lookup"><span data-stu-id="c3b81-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="c3b81-150">A coluna que identifica o nome localizado do usuário para o qual as permissões devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="c3b81-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="c3b81-151">Esse nome deve estar localizado no computador ou no domínio.</span><span class="sxs-lookup"><span data-stu-id="c3b81-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="c3b81-152">A instalação falhará se o computador ou o controlador de domínio não reconhecer a combinação de domínio e usuário ou se o SID (identificador de segurança) do usuário não puder ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="c3b81-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="c3b81-153">Vários usuários podem ser especificados para um único lockobject.</span><span class="sxs-lookup"><span data-stu-id="c3b81-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="c3b81-154">Os nomes de usuário comuns "Everyone" e "Administrators" podem ser inseridos em inglês e mapeados para SIDs conhecidos.</span><span class="sxs-lookup"><span data-stu-id="c3b81-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="c3b81-155">O LocalSystem recebe controle total em todos os descritores de segurança criados por meio da Tabela LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c3b81-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="c3b81-156">Você pode usar a propriedade [**ComputerName**](computername.md), a propriedade [**LogonUser**](logonuser.md) ou a [**Propriedade UserName**](username.md) nesse campo para obter o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c3b81-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="c3b81-157">É necessária uma ação personalizada para inserir o nome localizado de qualquer outro usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="c3b81-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="c3b81-158">Você pode usar vários registros com lockobject e entradas de tabela idênticas (mas entradas de usuário diferentes) para especificar listas de controle de acesso para vários usuários.</span><span class="sxs-lookup"><span data-stu-id="c3b81-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="c3b81-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permissão</span><span class="sxs-lookup"><span data-stu-id="c3b81-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="c3b81-160">A coluna que identifica a descrição de inteiro de privilégios do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3b81-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="c3b81-161">O seguinte fornece os valores mais usados (há uma lista completa em Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="c3b81-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="c3b81-162">Privilege</span><span class="sxs-lookup"><span data-stu-id="c3b81-162">Privilege</span></span>                                                              | <span data-ttu-id="c3b81-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3b81-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="c3b81-164">\_tudo genérico</span><span class="sxs-lookup"><span data-stu-id="c3b81-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="c3b81-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="c3b81-165">0X10000000</span></span><br/> <span data-ttu-id="c3b81-166">268435456</span><span class="sxs-lookup"><span data-stu-id="c3b81-166">268435456</span></span><br/>     | <span data-ttu-id="c3b81-167">Ler, gravar e executar o acesso</span><span class="sxs-lookup"><span data-stu-id="c3b81-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="c3b81-168">\_execução genérica</span><span class="sxs-lookup"><span data-stu-id="c3b81-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="c3b81-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="c3b81-169">0X20000000</span></span><br/> <span data-ttu-id="c3b81-170">536870912</span><span class="sxs-lookup"><span data-stu-id="c3b81-170">536870912</span></span><br/> | <span data-ttu-id="c3b81-171">Acesso de execução</span><span class="sxs-lookup"><span data-stu-id="c3b81-171">Execute access</span></span>                  |
| <span data-ttu-id="c3b81-172">\_gravação genérica</span><span class="sxs-lookup"><span data-stu-id="c3b81-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="c3b81-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="c3b81-173">0X40000000</span></span><br/> <span data-ttu-id="c3b81-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="c3b81-174">1073741824</span></span><br/>  | <span data-ttu-id="c3b81-175">Acesso de gravação</span><span class="sxs-lookup"><span data-stu-id="c3b81-175">Write access</span></span>                    |



 

<span data-ttu-id="c3b81-176">Não é possível especificar \_ a leitura genérica na coluna permissão.</span><span class="sxs-lookup"><span data-stu-id="c3b81-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="c3b81-177">Tentar fazer isso irá falhar.</span><span class="sxs-lookup"><span data-stu-id="c3b81-177">Attempting to do so will fail.</span></span> <span data-ttu-id="c3b81-178">Em vez disso, você deve especificar um valor como leitura de chave \_ ou arquivo \_ genérico \_ ler.</span><span class="sxs-lookup"><span data-stu-id="c3b81-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="c3b81-179">NULL inserido nesta coluna está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c3b81-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3b81-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3b81-180">Remarks</span></span>

<span data-ttu-id="c3b81-181">As ações [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)e [createfolders](createfolders-action.md) em [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c3b81-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="c3b81-182">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3b81-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="c3b81-183">A permissão só pode ser definida na Tabela LockPermissions para usuários que já existem no computador ou domínio.</span><span class="sxs-lookup"><span data-stu-id="c3b81-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="c3b81-184">Uma tentativa de definir permissões para um usuário desconhecido faz com que a instalação falhe, mesmo que essa conta de usuário seja criada durante a instalação por uma ação personalizada adiada.</span><span class="sxs-lookup"><span data-stu-id="c3b81-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="c3b81-185">É recomendável que o grupo local do administrador do sistema seja incluído em todas as listas de controle de acesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="c3b81-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="c3b81-186">Isso garante que o administrador do sistema possa acessar e manter objetos.</span><span class="sxs-lookup"><span data-stu-id="c3b81-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="c3b81-187">Cada arquivo, chave do registro ou diretório listado na Tabela LockPermissions recebe um descritor de segurança explícito, independentemente de ele substituir um objeto existente ou não.</span><span class="sxs-lookup"><span data-stu-id="c3b81-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="c3b81-188">O Windows Installer tenta preservar a segurança em objetos que já existem no sistema.</span><span class="sxs-lookup"><span data-stu-id="c3b81-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="c3b81-189">Se um objeto não estiver listado na Tabela LockPermissions e substituir um objeto existente, a substituição obterá as configurações de segurança do objeto que ele substitui.</span><span class="sxs-lookup"><span data-stu-id="c3b81-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="c3b81-190">Se um objeto não estiver listado na Tabela LockPermissions e não substituir um objeto existente, ele não receberá nenhum descritor de segurança explícito.</span><span class="sxs-lookup"><span data-stu-id="c3b81-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="c3b81-191">O acesso ao novo objeto é baseado nos atributos de seu objeto pai ou contêiner.</span><span class="sxs-lookup"><span data-stu-id="c3b81-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="c3b81-192">Se um objeto não estiver listado na tabela e substituir um objeto sem descritor de segurança explícito, o acesso ao novo objeto será baseado nos atributos de seu objeto pai ou contêiner.</span><span class="sxs-lookup"><span data-stu-id="c3b81-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="c3b81-193">O Windows Installer define a propriedade [**userid**](usersid.md) como o Sid (identificador de segurança) ou o usuário que está executando a instalação.</span><span class="sxs-lookup"><span data-stu-id="c3b81-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="c3b81-194">Validação</span><span class="sxs-lookup"><span data-stu-id="c3b81-194">Validation</span></span>

<dl>

[<span data-ttu-id="c3b81-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="c3b81-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c3b81-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="c3b81-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c3b81-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="c3b81-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c3b81-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="c3b81-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




