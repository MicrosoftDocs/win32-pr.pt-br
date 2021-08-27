---
description: Converte um nome de logon para a ID de segurança do usuário correspondente no formato de cadeia de caracteres.
title: Método DiskQuotaControl.TranslateLogonNameToSID
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
ms.openlocfilehash: 6bcaa5ac4f7dff4be80763b0aa411b7f104ff786b21e422044bdc7198697d54c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111816"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Método DiskQuotaControl.TranslateLogonNameToSID

Converte um nome de logon para a ID de segurança do usuário correspondente no formato de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*logonname* 
</dt> <dd>

Tipo: Cadeia **de caracteres**

Um valor de cadeia de caracteres que especifica o nome de logon do usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a SID (ID de segurança do usuário) no formato de cadeia de caracteres correspondente ao nome de logon fornecido. A cadeia de caracteres retornada inclui as chaves delimitadores padrão. Por exemplo:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Comentários

A cadeia de caracteres SID retornada pode ser passada para o [**método FindUser**](diskquotacontrol-finduser.md) no lugar de um nome de logon.

Quando uma chamada para o método [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) falha, isso pode ser devido a uma incompatibilidade entre o formulário (por exemplo, SAM compatível com o Gerenciador de Contas de Segurança e UPN de Nome upn de usuário) do nome de logon fornecido e o formulário armazenado no cache de nome \[ \] \[ \] SID. Nesses casos, o nome de logon pode ser convertido em um SID e a chamada para **FindUser é** repetida. **FindUser reconhece** uma cadeia de caracteres SID e ignorará a consulta de cache de nome SID. O código do Microsoft Visual Basic VBScript (Scripting Edition) a seguir ilustra essa técnica.


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



A conversão de nome para SID pode ser um processo lento em comparação com as buscas no cache de nome SID. Portanto, é recomendável que [**FindUser seja**](diskquotacontrol-finduser.md) chamado primeiro com um nome de logon. O exemplo acima usa essa técnica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




