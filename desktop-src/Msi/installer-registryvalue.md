---
description: O método RegistryValue do objeto Installer lê informações sobre uma chave do Registro especificada de value.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Método Installer.RegistryValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: eea77074a19ada084493bf5e24edaf49e25b659b0accdad16dab6c5781078f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074916"
---
# <a name="installerregistryvalue-method"></a>Método Installer.RegistryValue

O **método RegistryValue** do [**objeto Installer**](installer-object.md) lê informações sobre uma chave do Registro especificada de value. Se a chave ou o valor especificado não existir, o método retornará um erro de 9, "Subscrito fora do intervalo".

## <a name="syntax"></a>Sintaxe


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*root* 
</dt> <dd>

No Windows NT 4.0, a raiz do Registro é uma chave raiz numérica ou um nome de computador como uma cadeia de caracteres. Nomes de computador são sempre cadeias de caracteres. No Windows 95, Windows 98 ou Windows Me, a raiz do Registro é apenas uma chave raiz numérica. Você só pode acessar o HKLM em um computador remoto.



| Root                                                                                                                                                                                   | Significado      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**RAIZ DE \_ CLASSES HKEY \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**USUÁRIO ATUAL DO HKEY \_ \_**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**COMPUTADOR LOCAL HKEY \_ \_**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**USUÁRIOS \_ DO HKEY**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**HKEY \_ PERFORMANCE \_ DATA**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**CONFIGURAÇÃO \_ ATUAL DO HKEY \_**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY \_ DYN \_ DATA**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*chave* 
</dt> <dd>

Uma cadeia de caracteres que contém o caminho de chave completo da raiz.

</dd> <dt>

*value* 
</dt> <dd>

Esse parâmetro opcional designa qual valor associado retornar para a chave especificada. O valor é um dos valores mostrados na tabela a seguir.



| Valor                                                                                                                                                                                                    | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Ausente ou em branco**</dt> </dl> | Retorna um booliana que designa se a chave existe.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**String**</dt> </dl>                                         | Retornará os dados associados ao valor nomeado e falhará se o nome do valor não existir.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Inteiro positivo**</dt> </dl> | Retorna o nome do valor enumerado com base em 1, ele fica vazio se não existir. Essa opção usa a [**função RegEnumValue.**](/windows/win32/api/winreg/nf-winreg-regenumvaluea)<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Inteiro negativo**</dt> </dl> | Retorna o nome da sub-chave enumerada com base em 1; isso será vazio se não existir. Essa opção usa a [**função RegEnumKey.**](/windows/win32/api/winreg/nf-winreg-regenumkeya)<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Inteiro zero**</dt> </dl>                 | Retorna o nome da classe de cadeia de caracteres para a chave designada.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Cadeia de caracteres vazia " "**</dt> </dl> | Retorna o valor padrão da chave do Registro.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
