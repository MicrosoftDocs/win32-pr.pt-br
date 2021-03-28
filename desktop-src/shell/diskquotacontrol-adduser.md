---
description: Atribui uma cota de disco não padrão a um novo usuário.
title: Método DiskQuotaControl. adduser
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
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501417"
---
# <a name="diskquotacontroladduser-method"></a>Método DiskQuotaControl. adduser

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

Tipo: **Char**

Um valor de cadeia de caracteres que contém o nome de logon do usuário. Use a propriedade [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar como o nome deve ser resolvido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **objeto**

Retorna uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.

## <a name="remarks"></a>Comentários

O sistema de arquivos NTFS cria automaticamente uma entrada de cota de usuário quando um usuário grava pela primeira vez no volume. As entradas criadas dessa forma recebem o limite de aviso padrão e os valores de limite de cota rígido para o volume. Esse método permite que você crie uma entrada de cota de usuário antes que um usuário grave informações no volume. Ele retorna um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que pode ser usado para atribuir um limite de aviso ou um valor de limite de cota que difere das configurações padrão para o volume.

Se o usuário já existir, nenhuma nova entrada será criada. O método retorna o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) associado à entrada existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




