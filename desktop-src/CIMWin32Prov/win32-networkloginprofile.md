---
description: O Win32 \_ NetworkLoginProfile&\# 8194; A classe WMI representa as informações de logon de rede de um usuário específico em um sistema de computador executando o Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752406"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="75b34-103">\_Classe Win32 NetworkLoginProfile</span><span class="sxs-lookup"><span data-stu-id="75b34-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="75b34-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile do Win32** representa as informações de logon de rede de um usuário específico em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="75b34-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="75b34-105">Isso inclui, mas não se limita a status de senha, privilégios de acesso, cotas de disco e caminhos de diretório de logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="75b34-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="75b34-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b34-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b34-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="75b34-108">Membros</span><span class="sxs-lookup"><span data-stu-id="75b34-108">Members</span></span>

<span data-ttu-id="75b34-109">A classe **Win32 \_ NetworkLoginProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75b34-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="75b34-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75b34-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75b34-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75b34-111">Properties</span></span>

<span data-ttu-id="75b34-112">A classe **Win32 \_ NetworkLoginProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="75b34-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75b34-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="75b34-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-114">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75b34-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ Expires")</span><span class="sxs-lookup"><span data-stu-id="75b34-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-117">A conta vai expirar.</span><span class="sxs-lookup"><span data-stu-id="75b34-117">Account will expire.</span></span> <span data-ttu-id="75b34-118">Esse valor é calculado a partir do número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970 e é definido neste formato: AAAAMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="75b34-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="75b34-119">Exemplo: 20521201000230, 0 000</span><span class="sxs-lookup"><span data-stu-id="75b34-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="75b34-120">**AuthorizationFlags**</span><span class="sxs-lookup"><span data-stu-id="75b34-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-123">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas \| de [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 sinalizadores de \_ autenticação \_ "), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("impressora", "comunicação", "servidor", "contas")</span><span class="sxs-lookup"><span data-stu-id="75b34-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-124">Conjunto de sinalizadores que especificam os recursos que um usuário está autorizado a usar ou modificar.</span><span class="sxs-lookup"><span data-stu-id="75b34-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="75b34-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="75b34-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-126">Impressora</span><span class="sxs-lookup"><span data-stu-id="75b34-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="75b34-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="75b34-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-128">Comunicação</span><span class="sxs-lookup"><span data-stu-id="75b34-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="75b34-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="75b34-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-130">Servidor</span><span class="sxs-lookup"><span data-stu-id="75b34-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="75b34-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="75b34-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-132">Contas</span><span class="sxs-lookup"><span data-stu-id="75b34-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="75b34-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="75b34-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-136">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| funções de gerenciamento de rede \| NetUserEnum")</span><span class="sxs-lookup"><span data-stu-id="75b34-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-137">Número de vezes que o usuário insere uma senha inadequada ao fazer logon em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="75b34-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="75b34-138">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="75b34-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="75b34-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="75b34-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-142">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="75b34-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="75b34-143">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="75b34-143">Short textual description of the current object.</span></span>

<span data-ttu-id="75b34-144">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="75b34-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="75b34-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-148">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Code \_ Page")</span><span class="sxs-lookup"><span data-stu-id="75b34-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-149">Página de código para o idioma de escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="75b34-150">Uma página de código é o conjunto de caracteres usado.</span><span class="sxs-lookup"><span data-stu-id="75b34-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-151">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="75b34-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-154">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")</span><span class="sxs-lookup"><span data-stu-id="75b34-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-155">Comentário ou descrição para este perfil de logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="75b34-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-159">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ país \_ Code")</span><span class="sxs-lookup"><span data-stu-id="75b34-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-160">Código de país/região para o idioma de escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-161">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75b34-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75b34-164">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="75b34-164">Textual description of the current object.</span></span>

<span data-ttu-id="75b34-165">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="75b34-166">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="75b34-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-169">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags"), [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("script", "conta desabilitada", "página inicial necessária", "bloqueio", "senha não necessária", "paswword não pode mudar", "senha de teste criptografada permitida", "conta duplicada temporária", "conta normal", "conta de confiança entre domínios", "conta de confiança de estação de trabalho", "conta de confiança do servidor", "não expirar senha", "conta de logon MNS", "cartão inteligente necessário", "confiável para delegação", "não delegado", "usar somente chave des", "não exigir preautoria", "senha expirada")</span><span class="sxs-lookup"><span data-stu-id="75b34-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-170">As propriedades disponíveis para este perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="75b34-170">The properties available to this network profile.</span></span>

<span data-ttu-id="75b34-171">As propriedades que podem ser definidas incluem:</span><span class="sxs-lookup"><span data-stu-id="75b34-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="75b34-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="75b34-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-173">Script</span><span class="sxs-lookup"><span data-stu-id="75b34-173">Script</span></span>

<span data-ttu-id="75b34-174">Um script de logon executado.</span><span class="sxs-lookup"><span data-stu-id="75b34-174">A logon script executed.</span></span> <span data-ttu-id="75b34-175">Esse valor deve ser definido para o Gerenciador de LAN 2,0.</span><span class="sxs-lookup"><span data-stu-id="75b34-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-176">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="75b34-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-177">Conta desabilitada</span><span class="sxs-lookup"><span data-stu-id="75b34-177">Account Disabled</span></span>

<span data-ttu-id="75b34-178">A conta do usuário está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="75b34-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="75b34-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-180">Diretório base necessário</span><span class="sxs-lookup"><span data-stu-id="75b34-180">Home Directory Required</span></span>

<span data-ttu-id="75b34-181">Um diretório base é necessário.</span><span class="sxs-lookup"><span data-stu-id="75b34-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="75b34-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-183">Bloquear</span><span class="sxs-lookup"><span data-stu-id="75b34-183">Lockout</span></span>

<span data-ttu-id="75b34-184">A conta está bloqueada no momento. Para [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), esse valor pode ser limpo para desbloquear uma conta bloqueada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="75b34-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="75b34-185">Esse valor não pode ser usado para bloquear uma conta desbloqueada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="75b34-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="75b34-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-187">Senha não necessária</span><span class="sxs-lookup"><span data-stu-id="75b34-187">Password Not Required</span></span>

<span data-ttu-id="75b34-188">Nenhuma senha é necessária.</span><span class="sxs-lookup"><span data-stu-id="75b34-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="75b34-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-190">A senha não pode ser alterada</span><span class="sxs-lookup"><span data-stu-id="75b34-190">Password Cannot Change</span></span>

<span data-ttu-id="75b34-191">O usuário não pode alterar a senha.</span><span class="sxs-lookup"><span data-stu-id="75b34-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="75b34-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-193">Senha de teste criptografada permitida</span><span class="sxs-lookup"><span data-stu-id="75b34-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="75b34-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="75b34-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-195">Conta duplicada temporária</span><span class="sxs-lookup"><span data-stu-id="75b34-195">Temp Duplicate Account</span></span>

<span data-ttu-id="75b34-196">Uma conta para usuários cuja conta primária está em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="75b34-197">Essa conta fornece acesso de usuário a esse domínio, mas não a qualquer domínio que confie nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="75b34-198">O gerente de usuário refere-se a esse tipo de conta como uma conta de usuário local.</span><span class="sxs-lookup"><span data-stu-id="75b34-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="75b34-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-200">Conta normal</span><span class="sxs-lookup"><span data-stu-id="75b34-200">Normal Account</span></span>

<span data-ttu-id="75b34-201">Tipo de conta padrão que representa um usuário típico.</span><span class="sxs-lookup"><span data-stu-id="75b34-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="75b34-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-203">Conta de confiança entre domínios</span><span class="sxs-lookup"><span data-stu-id="75b34-203">Interdomain Trust Account</span></span>

<span data-ttu-id="75b34-204">Uma permissão para uma conta de confiança para um domínio que confia em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="75b34-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="75b34-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-206">Conta de confiança da estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="75b34-206">Workstation Trust Account</span></span>

<span data-ttu-id="75b34-207">Uma conta de computador para uma estação de trabalho do Windows ou servidor que seja membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="75b34-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-209">Conta de confiança do servidor</span><span class="sxs-lookup"><span data-stu-id="75b34-209">Server Trust Account</span></span>

<span data-ttu-id="75b34-210">Uma conta de computador para um controlador de domínio de backup que é membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="75b34-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-212">Não expirar senha</span><span class="sxs-lookup"><span data-stu-id="75b34-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="75b34-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="75b34-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-214">Conta de logon MNS</span><span class="sxs-lookup"><span data-stu-id="75b34-214">MNS Logon Account</span></span>

<span data-ttu-id="75b34-215">Tipo de conta de logon de MNS (conjunto de nós principais) que representa um usuário MNS.</span><span class="sxs-lookup"><span data-stu-id="75b34-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="75b34-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-217">Cartão inteligente necessário</span><span class="sxs-lookup"><span data-stu-id="75b34-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="75b34-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="75b34-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-219">Confiável para delegação</span><span class="sxs-lookup"><span data-stu-id="75b34-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="75b34-220">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="75b34-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-221">Não delegado</span><span class="sxs-lookup"><span data-stu-id="75b34-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="75b34-222">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="75b34-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-223">Usar somente chave DES</span><span class="sxs-lookup"><span data-stu-id="75b34-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="75b34-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="75b34-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-225">Não requer preautoria</span><span class="sxs-lookup"><span data-stu-id="75b34-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="75b34-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="75b34-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="75b34-227">Senha expirada</span><span class="sxs-lookup"><span data-stu-id="75b34-227">Password Expired</span></span>

<span data-ttu-id="75b34-228">Indica que a senha expirou.</span><span class="sxs-lookup"><span data-stu-id="75b34-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="75b34-229">As propriedades a seguir descrevem o tipo de conta.</span><span class="sxs-lookup"><span data-stu-id="75b34-229">The following properties describe the account type.</span></span> <span data-ttu-id="75b34-230">Somente um valor pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="75b34-230">Only one value can be set:</span></span>

-   <span data-ttu-id="75b34-231">\_conta normal da UF \_</span><span class="sxs-lookup"><span data-stu-id="75b34-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="75b34-232">UF \_ \_ duplicado de \_ conta temporária</span><span class="sxs-lookup"><span data-stu-id="75b34-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="75b34-233">conta de confiança da UF \_ Workstation \_ \_</span><span class="sxs-lookup"><span data-stu-id="75b34-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="75b34-234">\_conta de \_ confiança do servidor UF \_</span><span class="sxs-lookup"><span data-stu-id="75b34-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="75b34-235">conta de confiança de domínio da UF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="75b34-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="75b34-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="75b34-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-239">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ name")</span><span class="sxs-lookup"><span data-stu-id="75b34-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-240">Nome completo do usuário que pertence ao perfil de logon de rede.</span><span class="sxs-lookup"><span data-stu-id="75b34-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="75b34-241">Essa cadeia de caracteres poderá ficar vazia se o usuário optar por não associar um nome completo a um nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="75b34-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-245">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")</span><span class="sxs-lookup"><span data-stu-id="75b34-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-246">Caminho para o diretório base do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-246">Path to the home directory of the user.</span></span> <span data-ttu-id="75b34-247">Essa cadeia de caracteres pode estar vazia se o usuário optar por não especificar um diretório base.</span><span class="sxs-lookup"><span data-stu-id="75b34-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="75b34-248">Exemplo: " \\ HOMEDIR"</span><span class="sxs-lookup"><span data-stu-id="75b34-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-249">**HomeDirectoryDrive**</span><span class="sxs-lookup"><span data-stu-id="75b34-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-252">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ drive")</span><span class="sxs-lookup"><span data-stu-id="75b34-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-253">Letra da unidade atribuída ao diretório base do usuário para fins de logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="75b34-254">Exemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="75b34-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-255">**LastLogoff**</span><span class="sxs-lookup"><span data-stu-id="75b34-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-256">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75b34-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-258">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede do usuário de estruturas \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ último \_ logoff")</span><span class="sxs-lookup"><span data-stu-id="75b34-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-259">O usuário fez o último logoff do sistema.</span><span class="sxs-lookup"><span data-stu-id="75b34-259">User last logged off the system.</span></span> <span data-ttu-id="75b34-260">Esse valor é calculado a partir do número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970.</span><span class="sxs-lookup"><span data-stu-id="75b34-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="75b34-261">Um valor " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " significa que a hora do último logoff é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="75b34-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="75b34-262">O formato desse valor é AAAAMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="75b34-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="75b34-263">Para obter informações sobre como converter essa propriedade em sua hora local, consulte [tarefas do WMI: datas e horas](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="75b34-264">Exemplo: 19521201000230, 0 000</span><span class="sxs-lookup"><span data-stu-id="75b34-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="75b34-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="75b34-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-266">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75b34-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-268">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede do usuário de estruturas \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ último \_ logon")</span><span class="sxs-lookup"><span data-stu-id="75b34-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-269">O usuário fez o último logon no sistema.</span><span class="sxs-lookup"><span data-stu-id="75b34-269">User last logged on to the system.</span></span> <span data-ttu-id="75b34-270">Esse valor é calculado a partir do número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970.</span><span class="sxs-lookup"><span data-stu-id="75b34-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="75b34-271">O formato desse valor é AAAAMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="75b34-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="75b34-272">Para obter informações sobre como converter essa propriedade em sua hora local, consulte [tarefas do WMI: datas e horas](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="75b34-273">Exemplo: 19521201000230, 0 000</span><span class="sxs-lookup"><span data-stu-id="75b34-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="75b34-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="75b34-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-277">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management estruturas \| [**usuário \_ informações \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ horário de logon \_ ")</span><span class="sxs-lookup"><span data-stu-id="75b34-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-278">Vezes durante a semana em que o usuário pode fazer logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="75b34-279">Cada bit representa uma unidade de tempo especificada pela propriedade **UnitsPerWeek** .</span><span class="sxs-lookup"><span data-stu-id="75b34-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="75b34-280">Por exemplo, se a unidade de tempo for por hora, o primeiro bit (bit 0, Word 0) é domingo, 0:00 a 0:59, o segundo bit (bit 1, Word 0) é domingo, 1:00 a 1:59 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="75b34-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="75b34-281">Se esse membro for definido como **NULL**, não haverá restrição de tempo.</span><span class="sxs-lookup"><span data-stu-id="75b34-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="75b34-282">A hora é definida como GMT e deve ser ajustada para outros fusos horários (por exemplo, GMT menos 8 horas para PST).</span><span class="sxs-lookup"><span data-stu-id="75b34-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="75b34-283">**LogonServer**</span><span class="sxs-lookup"><span data-stu-id="75b34-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-286">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede do usuário de estruturas" \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 servidor de \_ logon \_ ")</span><span class="sxs-lookup"><span data-stu-id="75b34-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-287">Nome do servidor para o qual as solicitações de logon são enviadas.</span><span class="sxs-lookup"><span data-stu-id="75b34-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="75b34-288">Os nomes de servidor devem ser precedidos por duas barras invertidas ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="75b34-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="75b34-289">Um nome de servidor com um asterisco ( \\ \\ \* ) indica que a solicitação de logon pode ser tratada por qualquer servidor de logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="75b34-290">Uma cadeia de caracteres nula indica que as solicitações são enviadas para o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="75b34-291">Exemplo: " \\ \\ meuservidor"</span><span class="sxs-lookup"><span data-stu-id="75b34-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="75b34-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-293">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="75b34-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-295">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="75b34-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-296">Quantidade máxima de espaço em disco disponível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="75b34-297">Se MaximumStorage for definido como USER \_ MAXSTORAGE \_ Unlimited, o usuário poderá usar todo o espaço em disco disponível.</span><span class="sxs-lookup"><span data-stu-id="75b34-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="75b34-298">Exemplo: 10 milhões</span><span class="sxs-lookup"><span data-stu-id="75b34-298">Example: 10000000</span></span>

<span data-ttu-id="75b34-299">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="75b34-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="75b34-300">**Nome**</span><span class="sxs-lookup"><span data-stu-id="75b34-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-303">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ name")</span><span class="sxs-lookup"><span data-stu-id="75b34-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-304">Conta de usuário em um determinado domínio ou computador.</span><span class="sxs-lookup"><span data-stu-id="75b34-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="75b34-305">O número de caracteres no nome não pode exceder o valor de UNLEN.</span><span class="sxs-lookup"><span data-stu-id="75b34-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="75b34-306">Exemplo: "algumdomínio \\ davibarros"</span><span class="sxs-lookup"><span data-stu-id="75b34-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-307">**NumberOfLogons**</span><span class="sxs-lookup"><span data-stu-id="75b34-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-308">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-310">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ logons")</span><span class="sxs-lookup"><span data-stu-id="75b34-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-311">Número de vezes com êxito que o usuário tentou fazer logon nesta conta.</span><span class="sxs-lookup"><span data-stu-id="75b34-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="75b34-312">Um valor de 0xFFFFFFFF indica que o valor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="75b34-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="75b34-313">Essa propriedade é mantida separadamente em cada BDC (controlador de domínio de backup) no domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="75b34-314">Para obter um valor preciso, somente o maior valor de todos os BDCs deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="75b34-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="75b34-315">Exemplo: 4</span><span class="sxs-lookup"><span data-stu-id="75b34-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="75b34-316">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="75b34-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-319">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas de \| [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")</span><span class="sxs-lookup"><span data-stu-id="75b34-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-320">Espaço reservado para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="75b34-320">Space set aside for use by applications.</span></span> <span data-ttu-id="75b34-321">Essa cadeia de caracteres pode ser nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="75b34-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="75b34-322">Os produtos da Microsoft usam esse membro para armazenar informações de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="75b34-323">Não modifique essas informações, pois esse valor é específico de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75b34-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-324">**Senha**</span><span class="sxs-lookup"><span data-stu-id="75b34-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-325">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75b34-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-327">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas de \| [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 duração da \_ senha \_ ")</span><span class="sxs-lookup"><span data-stu-id="75b34-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-328">Período de tempo em que uma senha esteve em vigor.</span><span class="sxs-lookup"><span data-stu-id="75b34-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="75b34-329">Esse valor é medido a partir do número de segundos decorridos desde a última alteração da senha.</span><span class="sxs-lookup"><span data-stu-id="75b34-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="75b34-330">Exemplo: 1201000230, 0 000</span><span class="sxs-lookup"><span data-stu-id="75b34-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="75b34-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="75b34-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-332">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75b34-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-334">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de gerenciamento de rede de \| [**usuário \_ modal \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ age")</span><span class="sxs-lookup"><span data-stu-id="75b34-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-335">Data e hora em que a senha expira.</span><span class="sxs-lookup"><span data-stu-id="75b34-335">Date and time the password expires.</span></span> <span data-ttu-id="75b34-336">O valor é definido neste formato: AAAAMMDDHHMMSS. mmmmmm sutc</span><span class="sxs-lookup"><span data-stu-id="75b34-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="75b34-337">Exemplo: 19521201000230, 0 000</span><span class="sxs-lookup"><span data-stu-id="75b34-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="75b34-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="75b34-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-339">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-341">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")</span><span class="sxs-lookup"><span data-stu-id="75b34-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-342">O identificador relativo (RID) do grupo global primário deste usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="75b34-343">O identificador verifica o grupo primário ao qual o perfil do usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="75b34-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-344">**Direitos**</span><span class="sxs-lookup"><span data-stu-id="75b34-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-345">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-347">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")</span><span class="sxs-lookup"><span data-stu-id="75b34-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-348">Nível de privilégio atribuído à propriedade **de \_ nome usri3** .</span><span class="sxs-lookup"><span data-stu-id="75b34-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="75b34-349">**Convidado** (0)</span><span class="sxs-lookup"><span data-stu-id="75b34-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="75b34-350">**Usuário** (1)</span><span class="sxs-lookup"><span data-stu-id="75b34-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="75b34-351">**Administrador** (2)</span><span class="sxs-lookup"><span data-stu-id="75b34-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b34-352">**Perfil**</span><span class="sxs-lookup"><span data-stu-id="75b34-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-355">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")</span><span class="sxs-lookup"><span data-stu-id="75b34-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-356">Caminho para o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-356">Path to the user's profile.</span></span> <span data-ttu-id="75b34-357">Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="75b34-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="75b34-358">Um perfil de usuário contém configurações que são personalizáveis para cada usuário, como as cores da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="75b34-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="75b34-359">Exemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="75b34-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="75b34-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-363">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ caminho")</span><span class="sxs-lookup"><span data-stu-id="75b34-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-364">Caminho do diretório para o script de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="75b34-365">Um script de logon executa automaticamente um conjunto de comandos sempre que um usuário faz logon em um sistema.</span><span class="sxs-lookup"><span data-stu-id="75b34-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="75b34-366">Exemplo: "C: \\ Win \\ Profiles \\ ThomasSteven"</span><span class="sxs-lookup"><span data-stu-id="75b34-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="75b34-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="75b34-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-368">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-370">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="75b34-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75b34-371">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="75b34-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="75b34-372">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="75b34-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="75b34-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-374">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-376">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ unidades \_ por \_ semana")</span><span class="sxs-lookup"><span data-stu-id="75b34-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-377">Número de unidades de tempo em que a semana está dividida.</span><span class="sxs-lookup"><span data-stu-id="75b34-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="75b34-378">Ele é usado com a propriedade **LogonHours** para limitar o acesso do usuário ao computador.</span><span class="sxs-lookup"><span data-stu-id="75b34-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="75b34-379">Exemplo: 168 (horas por semana)</span><span class="sxs-lookup"><span data-stu-id="75b34-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="75b34-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="75b34-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-383">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comentário")</span><span class="sxs-lookup"><span data-stu-id="75b34-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-384">Descrição ou comentário definido pelo usuário para este perfil.</span><span class="sxs-lookup"><span data-stu-id="75b34-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-385">**ID**</span><span class="sxs-lookup"><span data-stu-id="75b34-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-386">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75b34-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-388">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ user \_ ID")</span><span class="sxs-lookup"><span data-stu-id="75b34-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-389">RID do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b34-389">RID of the user.</span></span> <span data-ttu-id="75b34-390">O identificador verifica se o usuário existe e se é exclusivo para esse domínio.</span><span class="sxs-lookup"><span data-stu-id="75b34-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="75b34-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="75b34-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-394">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags")</span><span class="sxs-lookup"><span data-stu-id="75b34-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-395">Tipo de conta à qual o usuário tem privilégios.</span><span class="sxs-lookup"><span data-stu-id="75b34-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="75b34-396">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="75b34-396">The values are:</span></span>

-   <span data-ttu-id="75b34-397">"Conta normal"</span><span class="sxs-lookup"><span data-stu-id="75b34-397">"Normal Account"</span></span>
-   <span data-ttu-id="75b34-398">"Conta duplicada"</span><span class="sxs-lookup"><span data-stu-id="75b34-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="75b34-399">"Conta de confiança da estação de trabalho"</span><span class="sxs-lookup"><span data-stu-id="75b34-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="75b34-400">"Conta de confiança do servidor"</span><span class="sxs-lookup"><span data-stu-id="75b34-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="75b34-401">"Conta de confiança entre domínios"</span><span class="sxs-lookup"><span data-stu-id="75b34-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="75b34-402">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="75b34-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="75b34-403">**Conta normal** ("conta normal")</span><span class="sxs-lookup"><span data-stu-id="75b34-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="75b34-404">**Conta duplicada** ("conta duplicada")</span><span class="sxs-lookup"><span data-stu-id="75b34-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="75b34-405">**Conta de confiança da estação de trabalho** ("conta de confiança da estação de trabalho")</span><span class="sxs-lookup"><span data-stu-id="75b34-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="75b34-406">**Conta de confiança do servidor** ("conta de confiança do servidor")</span><span class="sxs-lookup"><span data-stu-id="75b34-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="75b34-407">**Conta de confiança entre domínios** ("conta de confiança entre domínios")</span><span class="sxs-lookup"><span data-stu-id="75b34-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75b34-408">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="75b34-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b34-409">**Estações**</span><span class="sxs-lookup"><span data-stu-id="75b34-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b34-410">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75b34-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b34-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75b34-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b34-412">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ workstations")</span><span class="sxs-lookup"><span data-stu-id="75b34-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="75b34-413">Nomes de estações de trabalho das quais o usuário pode fazer logon.</span><span class="sxs-lookup"><span data-stu-id="75b34-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="75b34-414">Até oito estações de trabalho podem ser especificadas; os nomes devem ser separados por vírgulas (,).</span><span class="sxs-lookup"><span data-stu-id="75b34-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="75b34-415">Uma cadeia de caracteres nula indica que não há restrições.</span><span class="sxs-lookup"><span data-stu-id="75b34-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="75b34-416">Para desabilitar logons de todas as estações de trabalho para essa conta, defina a UF \_ ACCOUNTDISABLE na propriedade **flags** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="75b34-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75b34-417">Comentários</span><span class="sxs-lookup"><span data-stu-id="75b34-417">Remarks</span></span>

<span data-ttu-id="75b34-418">A classe **Win32 \_ NetworkLoginProfile** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="75b34-419">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="75b34-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="75b34-420">Para obter mais informações, consulte [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="75b34-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="75b34-421">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75b34-421">Examples</span></span>

<span data-ttu-id="75b34-422">A amostra do PowerShell [listar perfis de logon de rede](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) retorna informações de logon de rede para todos os usuários de um computador.</span><span class="sxs-lookup"><span data-stu-id="75b34-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="75b34-423">O exemplo de VBScript a seguir retorna informações de logon de rede.</span><span class="sxs-lookup"><span data-stu-id="75b34-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="75b34-424">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b34-424">Requirements</span></span>



| <span data-ttu-id="75b34-425">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b34-425">Requirement</span></span> | <span data-ttu-id="75b34-426">Valor</span><span class="sxs-lookup"><span data-stu-id="75b34-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b34-427">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b34-427">Minimum supported client</span></span><br/> | <span data-ttu-id="75b34-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75b34-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75b34-429">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b34-429">Minimum supported server</span></span><br/> | <span data-ttu-id="75b34-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75b34-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75b34-431">Namespace</span><span class="sxs-lookup"><span data-stu-id="75b34-431">Namespace</span></span><br/>                | <span data-ttu-id="75b34-432">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="75b34-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75b34-433">MOF</span><span class="sxs-lookup"><span data-stu-id="75b34-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75b34-434"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75b34-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75b34-435">DLL</span><span class="sxs-lookup"><span data-stu-id="75b34-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b34-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b34-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b34-437">Confira também</span><span class="sxs-lookup"><span data-stu-id="75b34-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b34-438">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="75b34-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="75b34-439">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="75b34-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
