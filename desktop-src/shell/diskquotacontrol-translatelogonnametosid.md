---
description: Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.
title: Método DiskQuotaControl. TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011331"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Método DiskQuotaControl. TranslateLogonNameToSID

Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LogonName* 
</dt> <dd>

Tipo: **cadeia de caracteres**

Um valor de cadeia de caracteres que especifica o nome de logon do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a ID de segurança do usuário (SID) no formato de cadeia de caracteres correspondente ao nome de logon fornecido. A cadeia de caracteres retornada inclui as chaves de circunscrição padrão. Por exemplo:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Comentários

A cadeia de caracteres SID retornada pode ser passada para o método [**FindUser**](diskquotacontrol-finduser.md) no lugar de um nome de logon.

Quando uma chamada para o método [**FindUser**](diskquotacontrol-finduser.md)( *LogonName*) falhar, isso pode ser devido a uma incompatibilidade entre o formulário (por exemplo, o Sam do Gerenciador de contas de segurança \[ \] e \[ o UPN do nome principal do usuário \] ) do nome de logon fornecido e o formulário armazenado no cache de nome de Sid. Nesses casos, o nome de logon pode ser convertido em um SID e a chamada para **FindUser** repetida. **FindUser** reconhece uma cadeia de caracteres Sid e irá ignorar a pesquisa de cache de nome Sid. O código do Microsoft Visual Basic Scripting Edition (VBScript) a seguir ilustra essa técnica.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



A conversão de nome para SID pode ser um processo lento quando comparada a pesquisas no cache de nome de SID. Portanto, é recomendável que [**FindUser**](diskquotacontrol-finduser.md) primeiro seja chamado com um nome de logon. O exemplo acima usa essa técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




