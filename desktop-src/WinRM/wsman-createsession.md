---
title: Método WSMan. CreateSession (WSManDisp. h)
description: Cria um objeto de sessão que pode ser usado para operações de rede subsequentes.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Método CreateSession Gerenciamento Remoto do Windows
- Método CreateSession Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499496"
---
# <a name="wsmancreatesession-method"></a>Método WSMan. CreateSession

Cria um objeto de [**sessão**](session.md) que pode ser usado para operações de rede subsequentes.

## <a name="syntax"></a>Sintaxe


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexão* \[ do em, opcional\]
</dt> <dd>

O protocolo e o serviço aos quais se conectar, incluindo o IPv4 ou IPv6. O formato das informações de conexão é o seguinte: <sufixo de endereço de *transporte* ><  >< >. Para obter exemplos, consulte comentários. Se nenhuma informação de conexão for fornecida, o computador local será usado.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Os sinalizadores de sessão que especificam o método de autenticação, como [*autenticação de negociação*](windows-remote-management-glossary.md) ou [*autenticação Digest*](windows-remote-management-glossary.md), para conexão a um computador remoto. Esses sinalizadores também especificam outras informações de conexão de sessão, como codificação ou criptografia. Esse parâmetro deve conter um ou mais dos sinalizadores em **\_ \_ WSManSessionFlags** para uma conexão remota. Para obter mais informações, consulte [constantes de sessão](session-constants.md). Nenhuma configuração de sinalizador é necessária para uma conexão com o WinRM no computador local. O padrão é **WSManFlagUseNegotiate**.

Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md) e o parâmetro *ConnectionOptions* .

</dd> <dt>

*ConnectionOptions* \[ em, opcional\]
</dt> <dd>

Um ponteiro para um objeto [**ConnectionOptions**](connectionoptions.md) que contém um nome de usuário e senha. O padrão é **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto de [**sessão**](session.md) que pode ser usado para executar operações WinRM locais ou remotas.

## <a name="remarks"></a>Comentários

O método **CreateSession** Inicializa o objeto de [**sessão**](session.md) coletando parâmetros, como sinalizadores, credenciais e uma cadeia de conexão para o parâmetro de *conexão* . **CreateSession** não se conecta de fato ao computador local ou remoto. Se a conexão não puder ser estabelecida, ocorrerá uma falha na primeira operação de **sessão** , como [**obter**](session-get.md) ou [**enumerar**](session-enumerate.md), após a chamada para **CreateSession**. Esse comportamento é diferente de uma conexão [*WMI*](windows-remote-management-glossary.md) com um [*namespace*](windows-remote-management-glossary.md) em um computador remoto. Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).

O exemplo de código VBScript a seguir é usado para chamar esse método.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



Os exemplos a seguir mostram os diferentes formatos usados para especificar informações de conexão no parâmetro de *conexão* (ao criar uma sessão HTTPS, o campo de> de *endereço* <deve corresponder ao nome do certificado do computador do servidor; caso contrário, ocorre uma falha):

-   "https://service"

    Usa HTTPS para se conectar ao local do serviço Web padrão.

-   "https://service.corp.com/websvcs/wsman"

    Usa HTTPS para se conectar ao local específico do serviço Web.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "

    Usa HTTPS e IPv6 com a porta padrão.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/WSMan"

    Usa HTTPS e IPv6 com a porta fornecida.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir cria uma sessão no computador local.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



O exemplo de código VBScript a seguir cria uma sessão em um computador remoto que é identificada por um endereço IP. O script fornece um nome de usuário e uma senha para uma conta. Os sinalizadores **WSManFlagCredUserNamePassword** e **WSManFlagUseBasic** são combinados para indicar que a conta é uma conta local no computador remoto. Se a criação da sessão falhar, o script será encerrado. O script usa os métodos que retornam a constante, como [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).

Para executar esse script, lembre-se de que você deve definir as definições de configuração padrão para cliente e servidor para permitir tráfego não criptografado e autenticação básica (**AllowUnencrypted** definido como **true** e Basic definido como **true**). Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



No exemplo de código VBScript a seguir, a conta é uma conta de domínio e a autenticação de negociação é usada. Com a autenticação de negociação, você deve especificar o nome de usuário como `computername\username` ou `ipaddress\username` .


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
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

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Session**](session.md)
</dt> <dt>

[Autenticação para conexões remotas](authentication-for-remote-connections.md)
</dt> <dt>

[Instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





