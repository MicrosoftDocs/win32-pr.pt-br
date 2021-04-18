---
description: O método REGISTRYVALUE do objeto do instalador lê informações sobre uma chave do Registro especificada de valor.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Método Installer. REGISTRYVALUE
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
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748978"
---
# <a name="installerregistryvalue-method"></a>Método Installer. REGISTRYVALUE

O método **REGISTRYVALUE** do objeto do [**instalador**](installer-object.md) lê informações sobre uma chave do Registro especificada de valor. Se a chave ou o valor especificado não existir, o método retornará um erro de 9, "Subscrito fora do intervalo".

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

No Windows NT 4,0, a raiz do registro é uma chave de raiz numérica ou um nome de computador como uma cadeia de caracteres. Os nomes de máquina são sempre cadeias de caracteres. No Windows 95, Windows 98 ou Windows me, a raiz do registro é apenas uma chave de raiz numérica. Você só pode acessar HKLM em um computador remoto.



| Root                                                                                                                                                                                   | Significado      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**\_raiz de classes hKey \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**HKEY \_ Current \_ User**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**\_máquina local \_ HKEY**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**usuários de HKEY \_**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**\_dados de desempenho de hKey \_**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**\_configuração atual de hKey \_**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**dados do HKEY \_ dyn \_**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*chave* 
</dt> <dd>

Uma cadeia de caracteres que contém o caminho de chave completo da raiz.

</dd> <dt>

*value* 
</dt> <dd>

Esse parâmetro opcional designa qual valor associado deve retornar para a chave especificada. O valor é um dos valores mostrados na tabela a seguir.



| Valor                                                                                                                                                                                                    | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Ausente ou em branco**</dt> </dl> | Retorna um valor booleano que indica se a chave existe.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**Strings**</dt> </dl>                                         | Retorna os dados associados ao valor nomeado e falha se o nome do valor for inexistente.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Inteiro positivo**</dt> </dl> | Retorna o nome do valor enumerado baseado em 1, ele estará vazio se não existir. Essa opção usa a função [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Número inteiro negativo**</dt> </dl> | Retorna o nome de subchave enumerado baseado em 1, que estará vazio se não existir. Essa opção usa a função [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Inteiro zero**</dt> </dl>                 | Retorna o nome da classe da cadeia de caracteres para a chave designada.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Cadeia de caracteres vazia ""**</dt> </dl> | Retorna o valor padrão da chave do registro.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
