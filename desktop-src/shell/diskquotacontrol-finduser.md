---
description: Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.
title: Método DiskQuotaControl. FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967309"
---
# <a name="diskquotacontrolfinduser-method"></a>Método DiskQuotaControl. FindUser

Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **cadeia de caracteres**

Um valor de cadeia de caracteres que contém o nome de logon do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.

## <a name="remarks"></a>Comentários

Esse método retorna um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) , mesmo se não houver nenhuma entrada para o usuário no arquivo de cota. O objeto de usuário retornado tem limite de aviso e limites de cota rígido definidos para os valores padrão do volume.

A cadeia de caracteres retornada de [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) pode ser passada no lugar do parâmetro *sLogonName* . Quando o **FindUser** recebe uma cadeia de caracteres Sid, ele usa o Sid correspondente para a pesquisa direta do registro de cota do usuário no volume. Isso ignora o cache de nome SID. Nos casos em que **FindUser** falha devido a uma incompatibilidade no formato (por exemplo, compatível com Sam e UPN) do nome de logon fornecido e o nome de logon armazenado em cache, o nome de logon pode ser convertido em uma cadeia de caracteres de Sid usando **TranslateLogonNameToSID** , então passado novamente para **FindUser**. O código VBScript a seguir ilustra essa técnica.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




