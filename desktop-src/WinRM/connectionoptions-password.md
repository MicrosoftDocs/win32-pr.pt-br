---
title: Propriedade ConnectionOptions. Password (WSManDisp. h)
description: Define a senha de uma conta local ou de domínio no computador remoto. Essa propriedade determina a senha para autenticação.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de propriedade de senha
- Propriedade Password Gerenciamento Remoto do Windows, objeto ConnectionOptions
- Objeto ConnectionOptions Gerenciamento Remoto do Windows, Propriedade Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085858"
---
# <a name="connectionoptionspassword-property"></a>Propriedade ConnectionOptions. Password

Define a senha de uma conta local ou de domínio no computador remoto. Essa propriedade determina a senha para autenticação. Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres que contém a senha de uma conta local ou de domínio no computador remoto.

Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** não estiver definido, a senha da conta que está executando o script será usada.

Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** estiver definido, o script solicitará que o usuário insira a senha (e o nome de usuário, se isso não for fornecido). Se um nome de usuário e senha válidos não forem inseridos, um erro de acesso negado será retornado.

## <a name="remarks"></a>Comentários

Lembre-se de que você não pode recuperar a senha. A senha só pode ser definida com esta propriedade.

Se você criar um objeto [**ConnectionOptions**](connectionoptions.md) e usar um nome de usuário e senha para se conectar ao gerenciamento remoto do Windows, o sinalizador **WSManFlagCredUserNamePassword** deverá ser definido na chamada para [**WSMan. CreateSession**](wsman-createsession.md).

Para obter mais informações sobre como definir senhas, consulte a seção comentários em [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir cria um objeto [**ConnectionOptions**](connectionoptions.md) e define a **senha**.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





