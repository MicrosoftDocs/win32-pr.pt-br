---
title: Classe Win32_TSLogonSetting
description: Define as definições de configuração para a \_ classe de terminal Win32 relacionada ao logon do cliente.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLogonSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLogonSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369765"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="10beb-105">\_Classe Win32 TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="10beb-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="10beb-106">A classe WMI **\_ TSLogonSetting do Win32** define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) relacionada ao logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="10beb-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="10beb-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="10beb-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="10beb-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="10beb-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="10beb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10beb-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="10beb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="10beb-110">Members</span></span>

<span data-ttu-id="10beb-111">A classe **Win32 \_ TSLogonSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10beb-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="10beb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="10beb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="10beb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10beb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10beb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="10beb-114">Methods</span></span>

<span data-ttu-id="10beb-115">A classe **Win32 \_ TSLogonSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="10beb-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="10beb-116">Método</span><span class="sxs-lookup"><span data-stu-id="10beb-116">Method</span></span>                                                                    | <span data-ttu-id="10beb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="10beb-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="10beb-118">**ExplicitLogon**</span><span class="sxs-lookup"><span data-stu-id="10beb-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="10beb-119">Define o nome de usuário, a senha e as credenciais de autenticação de domínio.</span><span class="sxs-lookup"><span data-stu-id="10beb-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="10beb-120">**SetPromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="10beb-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="10beb-121">Define a propriedade **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="10beb-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="10beb-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10beb-122">Properties</span></span>

<span data-ttu-id="10beb-123">A classe **Win32 \_ TSLogonSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10beb-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10beb-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="10beb-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10beb-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="10beb-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10beb-128">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="10beb-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="10beb-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10beb-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="10beb-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10beb-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="10beb-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10beb-133">A política que o servidor usa para determinar as configurações de conexão.</span><span class="sxs-lookup"><span data-stu-id="10beb-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="10beb-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="10beb-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="10beb-135">As configurações de conexão de usuário individual estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="10beb-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="10beb-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)</span><span class="sxs-lookup"><span data-stu-id="10beb-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="10beb-137">As configurações de conexão de usuário individual são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="10beb-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10beb-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-141">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="10beb-141">Description of the object.</span></span>

<span data-ttu-id="10beb-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10beb-143">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="10beb-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-146">A credencial de autenticação de logon de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="10beb-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="10beb-147">Esse é o domínio no qual o computador do usuário reside.</span><span class="sxs-lookup"><span data-stu-id="10beb-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="10beb-148">Esta propriedade não pode ter mais de 17 caracteres.</span><span class="sxs-lookup"><span data-stu-id="10beb-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="10beb-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10beb-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-150">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10beb-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10beb-152">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="10beb-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="10beb-153">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="10beb-153">The date the object was installed.</span></span> <span data-ttu-id="10beb-154">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="10beb-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="10beb-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10beb-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="10beb-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-159">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="10beb-159">The name of the object.</span></span>

<span data-ttu-id="10beb-160">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10beb-161">**Senha**</span><span class="sxs-lookup"><span data-stu-id="10beb-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-164">A credencial de autenticação de logon de senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="10beb-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="10beb-165">Esta propriedade não pode ter mais de 14 caracteres.</span><span class="sxs-lookup"><span data-stu-id="10beb-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="10beb-166">É recomendável que você defina o nível de segurança como privacidade do pacote (wbemAuthenticationLevelPktPrivacy = 6) se consultar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10beb-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="10beb-167">Isso ocorre porque a senha não é criptografada na conexão sem esse nível de segurança.</span><span class="sxs-lookup"><span data-stu-id="10beb-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="10beb-168">Para obter mais informações sobre como definir níveis de segurança, consulte [definindo a segurança do processo do aplicativo cliente](/windows/desktop/WmiSdk/setting-client-application-process-security) na documentação do SDK do WMI.</span><span class="sxs-lookup"><span data-stu-id="10beb-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="10beb-169">**PolicySourceDomain**</span><span class="sxs-lookup"><span data-stu-id="10beb-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10beb-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-172">Indica se a propriedade de **domínio** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="10beb-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="10beb-173">0</span><span class="sxs-lookup"><span data-stu-id="10beb-173">0</span></span>
</dt> <dd>

<span data-ttu-id="10beb-174">Servidor</span><span class="sxs-lookup"><span data-stu-id="10beb-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="10beb-175">1</span><span class="sxs-lookup"><span data-stu-id="10beb-175">1</span></span>
</dt> <dd>

<span data-ttu-id="10beb-176">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="10beb-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="10beb-177">2</span><span class="sxs-lookup"><span data-stu-id="10beb-177">2</span></span>
</dt> <dd>

<span data-ttu-id="10beb-178">Padrão</span><span class="sxs-lookup"><span data-stu-id="10beb-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="10beb-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-180">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10beb-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-182">Indica se a propriedade **PromptForPassword** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="10beb-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="10beb-183">0</span><span class="sxs-lookup"><span data-stu-id="10beb-183">0</span></span>
</dt> <dd>

<span data-ttu-id="10beb-184">Servidor</span><span class="sxs-lookup"><span data-stu-id="10beb-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="10beb-185">1</span><span class="sxs-lookup"><span data-stu-id="10beb-185">1</span></span>
</dt> <dd>

<span data-ttu-id="10beb-186">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="10beb-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="10beb-187">2</span><span class="sxs-lookup"><span data-stu-id="10beb-187">2</span></span>
</dt> <dd>

<span data-ttu-id="10beb-188">Padrão</span><span class="sxs-lookup"><span data-stu-id="10beb-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-189">**PolicySourceUserName**</span><span class="sxs-lookup"><span data-stu-id="10beb-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-190">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10beb-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-192">Indica se a propriedade **username** está configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="10beb-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="10beb-193">0</span><span class="sxs-lookup"><span data-stu-id="10beb-193">0</span></span>
</dt> <dd>

<span data-ttu-id="10beb-194">Servidor</span><span class="sxs-lookup"><span data-stu-id="10beb-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="10beb-195">1</span><span class="sxs-lookup"><span data-stu-id="10beb-195">1</span></span>
</dt> <dd>

<span data-ttu-id="10beb-196">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="10beb-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="10beb-197">2</span><span class="sxs-lookup"><span data-stu-id="10beb-197">2</span></span>
</dt> <dd>

<span data-ttu-id="10beb-198">Padrão</span><span class="sxs-lookup"><span data-stu-id="10beb-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="10beb-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-200">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10beb-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-202">Especifica se sempre será solicitada uma senha ao usuário durante o logon no servidor.</span><span class="sxs-lookup"><span data-stu-id="10beb-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="10beb-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="10beb-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="10beb-204">O usuário não é solicitado a fornecer uma senha.</span><span class="sxs-lookup"><span data-stu-id="10beb-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="10beb-205"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="10beb-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="10beb-206">O usuário é solicitado para uma senha.</span><span class="sxs-lookup"><span data-stu-id="10beb-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-207">**Status**</span><span class="sxs-lookup"><span data-stu-id="10beb-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10beb-210">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="10beb-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="10beb-211">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="10beb-211">Current status of the object.</span></span> <span data-ttu-id="10beb-212">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="10beb-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10beb-213">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="10beb-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="10beb-214">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="10beb-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="10beb-215">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="10beb-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10beb-216">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="10beb-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="10beb-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="10beb-218">("OK")</span><span class="sxs-lookup"><span data-stu-id="10beb-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-219">("Erro")</span><span class="sxs-lookup"><span data-stu-id="10beb-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-220">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="10beb-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-221">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="10beb-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-222">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="10beb-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-223">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="10beb-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-224">("Parando")</span><span class="sxs-lookup"><span data-stu-id="10beb-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10beb-225">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="10beb-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10beb-226">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="10beb-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-229">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="10beb-229">The name of the terminal.</span></span>

<span data-ttu-id="10beb-230">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="10beb-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="10beb-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="10beb-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10beb-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10beb-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10beb-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10beb-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10beb-234">A credencial de autenticação de logon do nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="10beb-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="10beb-235">Esta propriedade não pode ter mais de 20 caracteres.</span><span class="sxs-lookup"><span data-stu-id="10beb-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10beb-236">Comentários</span><span class="sxs-lookup"><span data-stu-id="10beb-236">Remarks</span></span>

<span data-ttu-id="10beb-237">Lembre-se de que o WinStations associado à sessão de console não pode acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="10beb-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="10beb-238">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade Terminalname, os métodos desse objeto retornam **WBEM \_ E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="10beb-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="10beb-239">Esse código de erro será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="10beb-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="10beb-240">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="10beb-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="10beb-241">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="10beb-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="10beb-242">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="10beb-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="10beb-243">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="10beb-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="10beb-244">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10beb-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10beb-245">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="10beb-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10beb-246">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="10beb-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10beb-247">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10beb-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10beb-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10beb-248">Requirements</span></span>



| <span data-ttu-id="10beb-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="10beb-249">Requirement</span></span> | <span data-ttu-id="10beb-250">Valor</span><span class="sxs-lookup"><span data-stu-id="10beb-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10beb-251">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10beb-251">Minimum supported client</span></span><br/> | <span data-ttu-id="10beb-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10beb-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10beb-253">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10beb-253">Minimum supported server</span></span><br/> | <span data-ttu-id="10beb-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10beb-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10beb-255">Namespace</span><span class="sxs-lookup"><span data-stu-id="10beb-255">Namespace</span></span><br/>                | <span data-ttu-id="10beb-256">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="10beb-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="10beb-257">MOF</span><span class="sxs-lookup"><span data-stu-id="10beb-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10beb-258"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10beb-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="10beb-259">DLL</span><span class="sxs-lookup"><span data-stu-id="10beb-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10beb-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10beb-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10beb-261">Confira também</span><span class="sxs-lookup"><span data-stu-id="10beb-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10beb-262">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="10beb-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="10beb-263">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="10beb-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

