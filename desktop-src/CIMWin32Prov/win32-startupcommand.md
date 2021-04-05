---
description: O Win32 \_ StartupCommand&\# 8194; A classe WMI representa um comando que é executado automaticamente quando um usuário faz logon no sistema de computador.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Classe Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826620"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="8f609-103">\_Classe Win32 StartupCommand</span><span class="sxs-lookup"><span data-stu-id="8f609-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="8f609-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand do Win32** representa um comando que é executado automaticamente quando um usuário faz logon no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="8f609-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="8f609-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8f609-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8f609-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="8f609-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f609-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f609-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="8f609-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8f609-108">Members</span></span>

<span data-ttu-id="8f609-109">A classe **Win32 \_ StartupCommand** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f609-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="8f609-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f609-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f609-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f609-111">Properties</span></span>

<span data-ttu-id="8f609-112">A classe **Win32 \_ StartupCommand** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f609-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f609-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8f609-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8f609-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f609-117">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8f609-117">Short textual description of the current object.</span></span>

<span data-ttu-id="8f609-118">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f609-119">**Comando**</span><span class="sxs-lookup"><span data-stu-id="8f609-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-122">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="8f609-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="8f609-123">Comando executado pelo comando de inicialização.</span><span class="sxs-lookup"><span data-stu-id="8f609-123">Command run by the startup command.</span></span>

<span data-ttu-id="8f609-124">O WMI Obtém esses dados da chave do registro</span><span class="sxs-lookup"><span data-stu-id="8f609-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="8f609-125">**HKEY \_ \_** \\  \\ Execução do software do computador local **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ </span><span class="sxs-lookup"><span data-stu-id="8f609-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="8f609-126">Exemplo: "C: \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="8f609-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="8f609-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8f609-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f609-130">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8f609-130">Textual description of the current object.</span></span>

<span data-ttu-id="8f609-131">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f609-132">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="8f609-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-135">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")</span><span class="sxs-lookup"><span data-stu-id="8f609-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="8f609-136">Caminho em que o comando de inicialização reside no sistema de arquivos de disco.</span><span class="sxs-lookup"><span data-stu-id="8f609-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="8f609-137">Por exemplo: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="8f609-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="8f609-138">**Inicialização** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="8f609-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="8f609-139">**Inicialização comum** ("inicialização comum")</span><span class="sxs-lookup"><span data-stu-id="8f609-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="8f609-140">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="8f609-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="8f609-141">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")</span><span class="sxs-lookup"><span data-stu-id="8f609-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f609-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8f609-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-145">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de arquivo win32api \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| testcfilename")</span><span class="sxs-lookup"><span data-stu-id="8f609-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="8f609-146">Nome de arquivo do comando de inicialização.</span><span class="sxs-lookup"><span data-stu-id="8f609-146">File name of the startup command.</span></span>

<span data-ttu-id="8f609-147">Exemplo: "FindFast"</span><span class="sxs-lookup"><span data-stu-id="8f609-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="8f609-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="8f609-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-151">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8f609-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f609-152">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8f609-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="8f609-153">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f609-154">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8f609-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-157">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8f609-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f609-158">Nome de usuário para o qual este comando de inicialização será executado.</span><span class="sxs-lookup"><span data-stu-id="8f609-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="8f609-159">Exemplo: "mydomain \\ myname"</span><span class="sxs-lookup"><span data-stu-id="8f609-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="8f609-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="8f609-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f609-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f609-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f609-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f609-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f609-163">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8f609-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8f609-164">A propriedade userid indica o SID do usuário para o qual esse comando de inicialização será executado.</span><span class="sxs-lookup"><span data-stu-id="8f609-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="8f609-165">Essa propriedade de usuário pode estar vazia, mas o userid ainda tem um valor se o nome de usuário não puder ser resolvido (como no caso de um usuário excluído).</span><span class="sxs-lookup"><span data-stu-id="8f609-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="8f609-166">A propriedade é útil para distinguir entre os comandos associados a dois usuários diferentes com nomes não resolvidos.</span><span class="sxs-lookup"><span data-stu-id="8f609-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="8f609-167">Pode ser nulo quando o comando está associado a itens que não identificam de fato um usuário como todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="8f609-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="8f609-168">Exemplo: S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="8f609-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f609-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f609-169">Remarks</span></span>

<span data-ttu-id="8f609-170">A classe **Win32 \_ StartupCommand** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="8f609-171">A inicialização do computador não termina depois que o sistema operacional é carregado.</span><span class="sxs-lookup"><span data-stu-id="8f609-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="8f609-172">Em vez disso, o sistema operacional Windows pode ser configurado para que os comandos de inicialização sejam executados cada vez que o Windows for iniciado.</span><span class="sxs-lookup"><span data-stu-id="8f609-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="8f609-173">Os comandos de inicialização são armazenados no registro ou como parte do perfil do usuário e são usados para iniciar automaticamente os scripts ou aplicativos especificados cada vez que o Windows é carregado.</span><span class="sxs-lookup"><span data-stu-id="8f609-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="8f609-174">Na maioria dos casos, os programas de inicialização automática são úteis; Eles garantem que determinados aplicativos, como ferramentas antivírus, sejam iniciados automaticamente e executados cada vez que o Windows for carregado.</span><span class="sxs-lookup"><span data-stu-id="8f609-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="8f609-175">No entanto, os programas de inicialização automática também podem ser responsáveis por problemas como:</span><span class="sxs-lookup"><span data-stu-id="8f609-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="8f609-176">Computadores que levam um tempo excepcionalmente longo para iniciar.</span><span class="sxs-lookup"><span data-stu-id="8f609-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="8f609-177">Isso pode ser o resultado de um grande número de aplicativos que devem ser iniciados toda vez que o Windows for iniciado.</span><span class="sxs-lookup"><span data-stu-id="8f609-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="8f609-178">Aplicativos que são representados na barra de tarefas ou no Gerenciador de tarefas, mesmo que o usuário não os tenha iniciado.</span><span class="sxs-lookup"><span data-stu-id="8f609-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="8f609-179">Embora esses aplicativos não causem necessariamente problemas, eles podem resultar em chamadas de suporte técnico de usuários que são confundidos com o local de onde esses programas vieram e por que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="8f609-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="8f609-180">Computadores que estão enfrentando problemas mesmo quando parecem ociosos.</span><span class="sxs-lookup"><span data-stu-id="8f609-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="8f609-181">Esses problemas geralmente são rastreados para comandos de inicialização que estão em execução quando ninguém está ciente de que estão em execução.</span><span class="sxs-lookup"><span data-stu-id="8f609-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="8f609-182">Identificar os aplicativos e scripts que são executados automaticamente na inicialização é uma tarefa administrativa importante, mas difícil, porque os comandos de inicialização podem ser armazenados em vários locais diferentes:</span><span class="sxs-lookup"><span data-stu-id="8f609-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="8f609-183">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="8f609-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="8f609-184">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="8f609-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="8f609-185">\\Execução de softwares HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\</span><span class="sxs-lookup"><span data-stu-id="8f609-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="8f609-186">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="8f609-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="8f609-187">HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="8f609-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="8f609-188">systemdrive \\ Documents and Settings \\ todos os usuários \\ menu iniciar \\ programas \\ inicialização</span><span class="sxs-lookup"><span data-stu-id="8f609-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="8f609-189">systemdrive \\ documentos e configurações \\ nome de usuário \\ Iniciar menu \\ programas \\ inicialização</span><span class="sxs-lookup"><span data-stu-id="8f609-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="8f609-190">Você pode usar a classe WMI Win32 \_ StartupCommand para enumerar programas de inicialização automática, independentemente de onde as informações estão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="8f609-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="8f609-191">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="8f609-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="8f609-192">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="8f609-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="8f609-193">Para obter mais informações, consulte [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="8f609-194">Você pode alterar os valores do registro em que o **Win32 \_ StartupCommand** Obtém os dados chamando os métodos do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI em script ou em C++.</span><span class="sxs-lookup"><span data-stu-id="8f609-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="8f609-195">Para obter mais informações, consulte [modificando o registro do sistema](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="8f609-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8f609-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f609-196">Examples</span></span>

<span data-ttu-id="8f609-197">O VBScript a seguir enumera os comandos de inicialização em um computador.</span><span class="sxs-lookup"><span data-stu-id="8f609-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="8f609-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f609-198">Requirements</span></span>



| <span data-ttu-id="8f609-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f609-199">Requirement</span></span> | <span data-ttu-id="8f609-200">Valor</span><span class="sxs-lookup"><span data-stu-id="8f609-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f609-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f609-201">Minimum supported client</span></span><br/> | <span data-ttu-id="8f609-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f609-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f609-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f609-203">Minimum supported server</span></span><br/> | <span data-ttu-id="8f609-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f609-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f609-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f609-205">Namespace</span></span><br/>                | <span data-ttu-id="8f609-206">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8f609-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f609-207">MOF</span><span class="sxs-lookup"><span data-stu-id="8f609-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f609-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f609-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f609-209">DLL</span><span class="sxs-lookup"><span data-stu-id="8f609-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f609-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f609-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f609-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f609-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f609-212">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8f609-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="8f609-213">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="8f609-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
