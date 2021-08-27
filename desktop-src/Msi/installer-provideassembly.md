---
description: O método ProvideAssembly do objeto Installer retorna o caminho instalado de um assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Método Installer::P rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 45d5c2d6b64936b034d859caddf72ddaaf6fba77451d066205d7f394200311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105206"
---
# <a name="installerprovideassembly-method"></a>Método Installer::P rovideAssembly

O **método ProvideAssembly** do [**objeto Installer**](installer-object.md) retorna o caminho instalado de um assembly.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Assembly* 
</dt> <dd>

O nome forte do assembly instalado que deve ser consultado.

</dd> <dt>

*appContext* 
</dt> <dd>

Definido como nulo para assemblies globais. Para assemblies privados, de definido *appContext* como o caminho completo do arquivo de configuração do aplicativo ou para o caminho completo do arquivo executável do aplicativo para o qual o assembly foi privado.

</dd> <dt>

*installMode* 
</dt> <dd>

Define o modo de instalação. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | Forneça o componente e execute qualquer instalação necessária para fornecer o componente. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | Forneça o componente somente se o recurso existir. Essa opção verificará se o assembly existe.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | Forneça o componente somente se o recurso existir. Essa opção não verifica se o assembly existe.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | Fornece o assembly somente se o assembly estiver instalado localmente.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Combinação dos sinalizadores usados por [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt> </dl> | Chama o [**método ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para *ReinstallMode* e retorna o caminho do assembly.<br/> |



 

</dd> <dt>

*Assemblyinfo* 
</dt> <dd>

Informações do assembly e tipo de assembly. De definido como um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                       | Significado                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | Um assembly do .NET.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Um assembly lado a lado do Win32.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O caminho para o assembly instalado.

## <a name="remarks"></a>Comentários

O **método ProvideAssembly** usa a [**função MsiProvideAssembly.**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)

## <a name="examples"></a>Exemplos

O script de exemplo a seguir demonstra o uso do método ProvideAssembly.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 4.5 no Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[Sem suporte no Windows 3.1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




