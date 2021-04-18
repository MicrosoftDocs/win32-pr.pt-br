---
description: A \_ classe WMI BootConfiguration do Win32 representa a configuração de inicialização de um sistema de computador executando o Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Classe Win32_BootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756433"
---
# <a name="win32_bootconfiguration-class"></a>\_Classe Win32 BootConfiguration

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration do Win32** representa a configuração de inicialização de um sistema de computador executando o Windows.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ BootConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ BootConfiguration** tem essas propriedades.

<dl> <dt>

**BootDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Caminho para os arquivos do sistema necessários para inicializar o sistema.

Exemplo: "C: \\ Windows"

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**ConfigurationPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")
</dt> </dl>

Caminho para os arquivos de configuração. Esse valor pode ser semelhante ao valor na propriedade **BootDirectory** .

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

**LastDrive**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetDriveType")
</dt> </dl>

Última letra da unidade à qual uma unidade física é atribuída.

Exemplo: "E:"

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nome da configuração de inicialização. É um identificador para a configuração de inicialização.

</dd> <dt>

**ScratchDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetTempPath")
</dt> </dl>

Diretório em que os arquivos temporários podem residir durante o tempo de inicialização.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**TempDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetTempPath")
</dt> </dl>

Diretório onde os arquivos temporários são armazenados.

Exemplo: "C: \\ Temp"

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ BootConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).

## <a name="examples"></a>Exemplos

A [lista as propriedades de configuração de inicialização de um computador de](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) exemplo Perl retorna informações de configuração de inicialização para um computador.

O exemplo de VBScript a seguir retorna informações de configuração de inicialização para um computador.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



O exemplo de código a seguir demonstra o uso da classe WMI **\_ BootConfiguration do Win32** .


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



O exemplo de código anterior cria a seguinte saída:

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

