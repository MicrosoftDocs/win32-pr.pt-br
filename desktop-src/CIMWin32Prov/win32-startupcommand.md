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
# <a name="win32_startupcommand-class"></a>\_Classe Win32 StartupCommand

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand do Win32** representa um comando que é executado automaticamente quando um usuário faz logon no sistema de computador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Win32 \_ StartupCommand** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ StartupCommand** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")
</dt> </dl>

Comando executado pelo comando de inicialização.

O WMI Obtém esses dados da chave do registro

**HKEY \_ \_** \\  \\ Execução do software do computador local **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ 

Exemplo: "C: \\ Windows \\notepad.exe myfile.txt"

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Localidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")
</dt> </dl>

Caminho em que o comando de inicialização reside no sistema de arquivos de disco.

Por exemplo: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Inicialização** ("inicialização")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Inicialização comum** ("inicialização comum")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de arquivo win32api \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| testcfilename")
</dt> </dl>

Nome de arquivo do comando de inicialização.

Exemplo: "FindFast"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Usuário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nome de usuário para o qual este comando de inicialização será executado.

Exemplo: "mydomain \\ myname"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

A propriedade userid indica o SID do usuário para o qual esse comando de inicialização será executado. Essa propriedade de usuário pode estar vazia, mas o userid ainda tem um valor se o nome de usuário não puder ser resolvido (como no caso de um usuário excluído). A propriedade é útil para distinguir entre os comandos associados a dois usuários diferentes com nomes não resolvidos. Pode ser nulo quando o comando está associado a itens que não identificam de fato um usuário como todos os usuários.

Exemplo: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ StartupCommand** é derivada da [**\_ configuração de CIM**](cim-setting.md).

A inicialização do computador não termina depois que o sistema operacional é carregado. Em vez disso, o sistema operacional Windows pode ser configurado para que os comandos de inicialização sejam executados cada vez que o Windows for iniciado. Os comandos de inicialização são armazenados no registro ou como parte do perfil do usuário e são usados para iniciar automaticamente os scripts ou aplicativos especificados cada vez que o Windows é carregado.

Na maioria dos casos, os programas de inicialização automática são úteis; Eles garantem que determinados aplicativos, como ferramentas antivírus, sejam iniciados automaticamente e executados cada vez que o Windows for carregado. No entanto, os programas de inicialização automática também podem ser responsáveis por problemas como:

-   Computadores que levam um tempo excepcionalmente longo para iniciar. Isso pode ser o resultado de um grande número de aplicativos que devem ser iniciados toda vez que o Windows for iniciado.
-   Aplicativos que são representados na barra de tarefas ou no Gerenciador de tarefas, mesmo que o usuário não os tenha iniciado. Embora esses aplicativos não causem necessariamente problemas, eles podem resultar em chamadas de suporte técnico de usuários que são confundidos com o local de onde esses programas vieram e por que estão em execução.
-   Computadores que estão enfrentando problemas mesmo quando parecem ociosos. Esses problemas geralmente são rastreados para comandos de inicialização que estão em execução quando ninguém está ciente de que estão em execução.

Identificar os aplicativos e scripts que são executados automaticamente na inicialização é uma tarefa administrativa importante, mas difícil, porque os comandos de inicialização podem ser armazenados em vários locais diferentes:

-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   \\Execução de softwares HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\
-   HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   systemdrive \\ Documents and Settings \\ todos os usuários \\ menu iniciar \\ programas \\ inicialização
-   systemdrive \\ documentos e configurações \\ nome de usuário \\ Iniciar menu \\ programas \\ inicialização

Você pode usar a classe WMI Win32 \_ StartupCommand para enumerar programas de inicialização automática, independentemente de onde as informações estão armazenadas.

O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside. Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio. Para obter mais informações, consulte [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).

Você pode alterar os valores do registro em que o **Win32 \_ StartupCommand** Obtém os dados chamando os métodos do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI em script ou em C++. Para obter mais informações, consulte [modificando o registro do sistema](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Exemplos

O VBScript a seguir enumera os comandos de inicialização em um computador.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
