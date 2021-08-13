---
description: O método AdvertiseScript do objeto do instalador anuncia um pacote de instalação.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: 'Método Installer:: AdvertiseScript'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6a3ca8b4c07b4bd19b9f5d5066ed17dcc5aa7edb5828741e32ee05197a83777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633213"
---
# <a name="installeradvertisescript-method"></a>Método Installer:: AdvertiseScript

O método **AdvertiseScript** do objeto do [**instalador**](installer-object.md) anuncia um pacote de instalação.

## <a name="syntax"></a>Sintaxe


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*scriptPath* 
</dt> <dd>

O caminho completo para o arquivo de script gerado pelo método [**CreateAdvertiseScript**](installer-createadvertisescript.md) .

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Os sinalizadores que controlam o anúncio. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**msiAdvertiseScriptCacheInfo**</dt> <dt>0x001</dt> </dl>                                                                 | Inclua esse sinalizador se os ícones precisarem ser criados ou removidos.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiAdvertiseScriptShortcuts**</dt> <dt>0x004</dt> </dl>                                                                 | Inclua esse sinalizador se os atalhos precisarem ser criados ou removidos.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiAdvertiseScriptMachineAssign**</dt> <dt>0x008</dt> </dl>                                                 | Inclua esse sinalizador se o produto tiver que ser atribuído a um computador.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptConfigurationRegistration**</dt> <dt>0x020</dt> </dl> | Inclua esse sinalizador se as informações de configuração e gerenciamento nos dados do registro precisarem ser gravadas ou removidas.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**msiAdvertiseScriptValidateTransformList**</dt> <dt>0x040</dt> </dl>                 | Inclua esse sinalizador para forçar a validação das transformações listadas no script em relação às transformações registradas anteriormente para este produto. Observe que os conflitos de transformação são detectados usando uma comparação de cadeia de caracteres que não diferencia maiúsculas de minúsculas e são avaliadas entre instalações por usuário e por máquina em todos os [contextos de instalação](installation-context.md).<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptClassInfoRegistration**</dt> <dt>0x080</dt> </dl>                 | Inclua esse sinalizador se as informações de anúncio no registro relacionadas a classes COM precisarem ser gravadas ou removidas.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptExtensionInfoRegistration**</dt> <dt>0x100</dt> </dl> | Inclua esse sinalizador se as informações de anúncio no registro relacionadas a uma extensão precisarem ser gravadas ou removidas.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**msiAdvertiseScriptAppInfo**</dt> <dt>0x180</dt> </dl>                                                                         | Inclua esse sinalizador se as informações de anúncio no registro precisarem ser gravadas ou removidas.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**msiAdvertiseScriptRegData**</dt> <dt>0x1A0</dt> </dl>                                                                         | Inclua esse sinalizador se as informações de anúncio no registro precisarem ser gravadas ou removidas.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE se os itens especificados forem removidos em vez de serem criados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **AdvertiseScript** usa a função [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) . O uso do método **AdvertiseScript** requer que o script esteja sendo executado dentro de um processo do sistema local.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método **AdvertiseScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




