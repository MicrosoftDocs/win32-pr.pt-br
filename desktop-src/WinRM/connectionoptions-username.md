---
title: Propriedade ConnectionOptions. UserName (WSManDisp. h)
description: Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto. Essa propriedade determina o nome de usuário para autenticação.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Gerenciamento Remoto do Windows
- Propriedade UserName Gerenciamento Remoto do Windows, objeto ConnectionOptions
- Objeto ConnectionOptions Gerenciamento Remoto do Windows, Propriedade UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085857"
---
# <a name="connectionoptionsusername-property"></a>Propriedade ConnectionOptions. UserName

Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto. Essa propriedade determina o nome de usuário para autenticação. Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres que contém o nome de usuário de uma conta local ou de domínio no computador remoto.

Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** não estiver definido, o nome de usuário da conta que está executando o script será usado.

Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** estiver definido, o script solicitará que o usuário insira o nome de usuário e a senha. Se um nome de usuário e senha válidos não forem inseridos, um erro de acesso negado será retornado.

## <a name="remarks"></a>Comentários

A sintaxe a seguir é usada para especificar essa propriedade.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Você pode fornecer o **nome de usuário** e a [**senha**](connectionoptions-password.md) para uma conta de domínio ao usar a autenticação [*Negotiate*](windows-remote-management-glossary.md) ou *Kerberos* , ou para uma conta local com autenticação [*básica*](windows-remote-management-glossary.md) . Para se conectar a uma conta local, os sinalizadores [**WSMan. CreateSession**](wsman-createsession.md) devem conter a combinação do sinalizador **WSManFlagUseBasic** e do sinalizador **WsmanFlagCredUserNamePassword** . Para se conectar a uma conta de domínio, os sinalizadores **WSMan. CreateSession** devem conter a combinação do sinalizador **WSManFlagUseNegotiate** e do sinalizador **WsmanFlagCredUserNamePassword** , ou a combinação do sinalizador **WSManFlagUseKerberos** e do sinalizador **WsmanFlagCredUserNamePassword** . Para uma conta de domínio, o **nome de usuário** deve ser especificado no formato "computador \\ nome de usuário", em que a parte "computador" da cadeia de caracteres pode ser o nome ou o endereço IP. Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Para se conectar a uma conta de domínio, os sinalizadores [**WSMan. CreateSession**](wsman-createsession.md) devem conter a combinação do sinalizador **WSManFlagUseNegotiate** e o sinalizador **WsmanFlagCredUserNamePassword** para se conectar a uma conta de domínio, o que exige autenticação de negociação.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
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

 

 





