---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Descreve uma política de autorização de recursos do Área de Trabalho Remota (RD \ 160; RAP). Uma RD \ 160; A RAP é usada para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayResourceAuthorizationPolicy classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009290"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="50dfd-106">\_Classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="50dfd-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="50dfd-107">Descreve um Área de Trabalho Remota RD RAP (política de autorização de recursos).</span><span class="sxs-lookup"><span data-stu-id="50dfd-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="50dfd-108">Uma RD RAP é usada para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="50dfd-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="50dfd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50dfd-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="50dfd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="50dfd-110">Members</span></span>

<span data-ttu-id="50dfd-111">A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="50dfd-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="50dfd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="50dfd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="50dfd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="50dfd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="50dfd-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="50dfd-114">Methods</span></span>

<span data-ttu-id="50dfd-115">A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="50dfd-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="50dfd-116">Método</span><span class="sxs-lookup"><span data-stu-id="50dfd-116">Method</span></span>                                                                                          | <span data-ttu-id="50dfd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="50dfd-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50dfd-118">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="50dfd-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="50dfd-119">Adiciona os nomes de grupos de usuários especificados aos grupos de usuários existentes na propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="50dfd-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="50dfd-120">**Criar**</span><span class="sxs-lookup"><span data-stu-id="50dfd-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="50dfd-121">Cria uma RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="50dfd-122">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="50dfd-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="50dfd-123">Exclui a RD RAP atual.</span><span class="sxs-lookup"><span data-stu-id="50dfd-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="50dfd-124">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="50dfd-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="50dfd-125">Remove os nomes de grupo de usuários especificados dos grupos de usuários existentes na propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="50dfd-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="50dfd-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="50dfd-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="50dfd-127">Define a propriedade **Description** para a RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="50dfd-128">**Sethabilitado**</span><span class="sxs-lookup"><span data-stu-id="50dfd-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="50dfd-129">Habilita ou desabilita a RD RAP definindo a propriedade **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="50dfd-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="50dfd-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="50dfd-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="50dfd-131">Define a propriedade **Name** para a RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="50dfd-132">**Setportnumbers**</span><span class="sxs-lookup"><span data-stu-id="50dfd-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="50dfd-133">Define a propriedade **portnumbers** para a RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="50dfd-134">**Fileresource**</span><span class="sxs-lookup"><span data-stu-id="50dfd-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="50dfd-135">Define as propriedades **ResourceGroupType** e **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="50dfd-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="50dfd-136">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="50dfd-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="50dfd-137">Define a propriedade **Usergroupnames** para a RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="50dfd-138">**Cumulativo**</span><span class="sxs-lookup"><span data-stu-id="50dfd-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="50dfd-139">Atualiza a RD RAP atual.</span><span class="sxs-lookup"><span data-stu-id="50dfd-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="50dfd-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="50dfd-140">Properties</span></span>

<span data-ttu-id="50dfd-141">A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="50dfd-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50dfd-142">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50dfd-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-145">Descrição da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-145">Description of the RD RAP.</span></span> <span data-ttu-id="50dfd-146">Essa propriedade é alterada com o método [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="50dfd-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="50dfd-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-150">Indica se esta RD RAP está habilitada.</span><span class="sxs-lookup"><span data-stu-id="50dfd-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="50dfd-151">Essa propriedade é alterada com o método [**sethabilitado**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="50dfd-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="50dfd-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-156">Nome da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="50dfd-156">Name of the RD RAP.</span></span> <span data-ttu-id="50dfd-157">Essa propriedade é alterada com o método [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-158">**PortNumbers**</span><span class="sxs-lookup"><span data-stu-id="50dfd-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-161">Lista de números de porta separados por ponto e vírgula permitidos para esta política.</span><span class="sxs-lookup"><span data-stu-id="50dfd-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="50dfd-162">Para permitir qualquer número de porta, defina " \* ".</span><span class="sxs-lookup"><span data-stu-id="50dfd-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-163">**De protocolo**</span><span class="sxs-lookup"><span data-stu-id="50dfd-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-166">Lista de nomes de protocolo separados por ponto e vírgula que estão habilitados para esta política.</span><span class="sxs-lookup"><span data-stu-id="50dfd-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="50dfd-167">Os nomes devem corresponder ao retorno do método [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="50dfd-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-171">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50dfd-171">Resource group name.</span></span> <span data-ttu-id="50dfd-172">Essa propriedade é alterada com o método [**fileresource**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-173">**ResourceGroupType**</span><span class="sxs-lookup"><span data-stu-id="50dfd-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-176">Identifica o tipo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50dfd-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="50dfd-177">Essa propriedade é alterada com o método [**fileresource**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="50dfd-178">RT</span><span class="sxs-lookup"><span data-stu-id="50dfd-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="50dfd-179">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50dfd-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-180">CG</span><span class="sxs-lookup"><span data-stu-id="50dfd-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="50dfd-181">Grupo de computadores, conforme armazenado em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="50dfd-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="50dfd-182">OS</span><span class="sxs-lookup"><span data-stu-id="50dfd-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="50dfd-183">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="50dfd-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="50dfd-184">**Usergroupnames**</span><span class="sxs-lookup"><span data-stu-id="50dfd-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50dfd-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50dfd-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50dfd-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50dfd-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50dfd-187">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="50dfd-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="50dfd-188">Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.</span><span class="sxs-lookup"><span data-stu-id="50dfd-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="50dfd-189">Essa propriedade é alterada com os métodos [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="50dfd-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50dfd-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="50dfd-190">Remarks</span></span>

<span data-ttu-id="50dfd-191">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="50dfd-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="50dfd-192">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="50dfd-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="50dfd-193">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="50dfd-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="50dfd-194">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="50dfd-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="50dfd-195">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="50dfd-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="50dfd-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50dfd-196">Requirements</span></span>



| <span data-ttu-id="50dfd-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="50dfd-197">Requirement</span></span> | <span data-ttu-id="50dfd-198">Valor</span><span class="sxs-lookup"><span data-stu-id="50dfd-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dfd-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50dfd-199">Minimum supported client</span></span><br/> | <span data-ttu-id="50dfd-200">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="50dfd-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="50dfd-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50dfd-201">Minimum supported server</span></span><br/> | <span data-ttu-id="50dfd-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50dfd-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="50dfd-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="50dfd-203">Namespace</span></span><br/>                | <span data-ttu-id="50dfd-204">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="50dfd-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="50dfd-205">MOF</span><span class="sxs-lookup"><span data-stu-id="50dfd-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50dfd-206"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50dfd-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="50dfd-207">DLL</span><span class="sxs-lookup"><span data-stu-id="50dfd-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50dfd-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50dfd-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="50dfd-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="50dfd-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50dfd-210">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="50dfd-211">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="50dfd-212">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="50dfd-213">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="50dfd-214">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="50dfd-215">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="50dfd-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

