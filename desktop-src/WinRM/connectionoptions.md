---
title: Objeto ConnectionOptions (WSManDisp. h)
description: O objeto ConnectionOptions é passado para o método CreateSession para fornecer o nome de usuário e a senha associados à conta local no computador remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objeto ConnectionOptions Gerenciamento Remoto do Windows
- Gerenciamento Remoto do Windows de objeto ConnectionOptions, descrito
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765697"
---
# <a name="connectionoptions-object"></a>Objeto ConnectionOptions

O objeto **ConnectionOptions** é passado para o método [**CreateSession**](wsman-createsession.md) para fornecer o nome de usuário e a senha associados à conta local no computador remoto. Se nenhum parâmetro for fornecido, as credenciais da conta que executa o script serão definidas com os valores padrão.

## <a name="members"></a>Membros

O objeto **ConnectionOptions** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **ConnectionOptions** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso           | Descrição                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Senha**](connectionoptions-password.md)<br/> | Somente gravação<br/> | Define a senha de uma conta local ou de domínio no computador remoto.<br/>           |
| [**Usu**](connectionoptions-username.md)<br/> | Leitura/gravação<br/> | Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **ConnectionOptions** corresponde à interface [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .

Se um aplicativo cliente Gerenciamento Remoto do Windows estiver sendo executado sob representação, ocorrerá uma falha se você definir a propriedade [**password**](connectionoptions-password.md) . Um aplicativo cliente é um script ou outro programa que envia uma solicitação para o WinRM no computador local ou remoto. O aplicativo cliente pode estar sendo executado sob representação porque ele chamou uma função como [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Uma página de Active Server (ASP) ou serviço não pode solicitar um nome de usuário e senha se o processo ASP for executado em uma conta que representa um cliente.

O sinalizador **WSManFlagCredUserNamePassword** deve ser definido na chamada [**WSman. CreateSession**](wsman-createsession.md) ao usar o [**nome de usuário**](connectionoptions-username.md) e a [**senha**](connectionoptions-password.md) para autenticação.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir mostra como criar um objeto **ConnectionOptions** , definir as propriedades da conta no computador remoto e usá-lo na criação de um objeto de [**sessão**](session.md) .


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
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

[Autenticação para conexões remotas](authentication-for-remote-connections.md)
</dt> <dt>

[API de script do WinRM](winrm-scripting-api.md)
</dt> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtendo dados do computador local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

