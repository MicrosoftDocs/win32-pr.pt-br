---
description: Atribui uma cota de disco não padrão a um novo usuário.
title: Método DiskQuotaControl.AddUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841527"
---
# <a name="diskquotacontroladduser-method"></a>Método DiskQuotaControl.AddUser

Atribui uma cota de disco não padrão a um novo usuário.

## <a name="syntax"></a>Sintaxe


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLogonName* 
</dt> <dd>

Tipo: **CHAR**

Um valor de cadeia de caracteres que contém o nome de logon do usuário. Use a [**propriedade UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar como o nome deve ser resolvido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **Objeto**

Retorna uma expressão de objeto que é avaliada para o objeto [**DIDiskQuotaUser do**](didiskquotauser-object.md) usuário.

## <a name="remarks"></a>Comentários

O sistema de arquivos NTFS cria automaticamente uma entrada de cota de usuário quando um usuário grava pela primeira vez no volume. As entradas criadas dessa maneira são atribuídas aos valores padrão de limite de aviso e limite de cota rígido para o volume. Esse método permite que você crie uma entrada de cota de usuário antes que um usuário escreva informações no volume. Ele retorna um [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) que pode ser usado para atribuir um limite de aviso ou um valor de limite de cota que difere das configurações padrão para o volume.

Se o usuário já existir, nenhuma nova entrada será criada. O método retorna o [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) associado à entrada existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




