---
description: A classe Win32 \_ DesktopWMI representa as características comuns da área de trabalho de um usuário. As propriedades dessa classe podem ser modificadas pelo usuário para personalizar a área de trabalho.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c59adebd2fdf3c0727016473e6c347be3af139d539bb007c794eb2aafb4c1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002876"
---
# <a name="win32_desktop-class"></a>Classe Win32 \_ Desktop

A **classe WMI do Win32 \_ Desktop** representa as características comuns da área de trabalho de um usuário.[](/windows/desktop/WmiSdk/retrieving-a-class) As propriedades dessa classe podem ser modificadas pelo usuário para personalizar a área de trabalho.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ Desktop** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ Desktop** tem essas propriedades.

<dl> <dt>

**BorderWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle \\ \\ \\ \\ DesktopMetrics \| BorderWidth")
</dt> </dl>

Largura das bordas em torno de todas as janelas com bordas ajustáveis.

Exemplo: 3

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descrição textual curta do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**CoolSwitch**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Painel de Controle Desktop \\ \\ \| CoolSwitch")
</dt> </dl>

A alternação rápida de tarefas está 100000001. A troca rápida de tarefas permite que o usuário alternar entre janelas usando a **combinação de teclado ALT+TAB.**

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Painel de Controle Desktop \\ \\ \| CursorBlinkRate"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")
</dt> </dl>

Período de tempo entre o cursor sucessivo piscar.

Exemplo: 530

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**DragFullWindows**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Painel de Controle Desktop \\ \\ \| DragFullWindows")
</dt> </dl>

O conteúdo de uma janela é mostrado quando um usuário move a janela.

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Painel de Controle Desktop \\ \\ \| GridGranularity"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")
</dt> </dl>

Espaçamento da grade à que as janelas estão vinculadas na área de trabalho. Isso facilita a organização de janelas. O espaçamento geralmente é suficiente para que o usuário não o observe.

Example: 1

</dd> <dt>

**IconSpacing**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| Default \\ \\ Painel de Controle Desktop \\ \\ \\ \\ \| IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Espaçamento entre ícones.

Exemplo: 75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \\ \\ IconMetricsFont") \|
</dt> </dl>

Fonte usada para os nomes dos ícones.

Exemplo: "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")
</dt> </dl>

Tamanho da fonte do ícone.

Exemplo: 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| Default \\ \\ Painel de Controle Desktop \\ \\ \\ \\ IconMetricsTitleWrap") \|
</dt> </dl>

O texto do título do ícone é wraps para a próxima linha.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nome que identifica o perfil da área de trabalho atual.

Exemplo: "MainProf"

</dd> <dt>

**Padrão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| Default \\ \\ Painel de Controle Desktop \\ \\ \| Pattern")
</dt> </dl>

Nome do padrão usado como a tela de fundo para a área de trabalho.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle \\ \\ Desktop \| ScreenSaveActive")
</dt> </dl>

A economia de tela está ativa.

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \|SCRNSAVE.EXE")
</dt> </dl>

Nome do arquivo executável da salvação de tela atual.

Exemplo: "LOGON. SCR"

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \| ScreenSaverIsSecure")
</dt> </dl>

A senha está habilitada para a proteção de tela.

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \| ScreenSaveTimeOut"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")
</dt> </dl>

Quantidade de tempo que passa antes do início da economia de tela.

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**Papel de parede**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT Painel de Controle \\ \\ \\ \\ Desktop \| Wallpaper")
</dt> </dl>

Nome do arquivo para o design de papel de parede na tela de fundo da área de trabalho.

Exemplo: "WINNT.BMP"

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \| WallpaperStyle")
</dt> </dl>

O papel de parede é estendido para preencher toda a tela. Microsoft Plus! deve ser instalado antes que essa opção seja disponibilizada. Se **FALSE**, o papel de parede manterá suas dimensões originais na tela de fundo da área de trabalho.

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry. \| DEFAULT \\ \\ Painel de Controle Desktop \\ \\ \| TileWallpaper")
</dt> </dl>

O papel de parede é lado a lado ou centralizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ Desktop** é derivada da [**configuração cim \_**](cim-setting.md).

O processo de chamada que usa essa classe deve ter ES **\_ privilégio RESTORE \_ NAME** no computador no qual o Registro reside. Por exemplo, se você enumerar essa classe no computador local, a conta na qual o aplicativo é executado deverá ter esse privilégio. Para obter mais informações, consulte [Executando operações privilegiadas.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="examples"></a>Exemplos

O exemplo de código a seguir descreve como recuperar informações da área de trabalho.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração cim \_**](cim-setting.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

