---
title: Constantes de autenticação (WSManDisp. h)
description: Especifique o método de autenticação e como lidar com servidores de certificado para transporte HTTPS de solicitações.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885e3b782c4af67304f1a92eca324c0f266e71665a7a876683cbb1dbff472ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132809"
---
# <a name="authentication-constants"></a>Constantes de autenticação

As constantes de autenticação são constantes na enumeração **\_ \_ WSManSessionFlags** que especificam o método de autenticação e como lidar com servidores de certificado para transporte HTTPS de solicitações.

Uma ou mais das constantes listadas na lista a seguir são necessárias no parâmetro *flags* em chamadas para [**WSMan. CreateSession**](wsman-createsession.md) ou em chamadas [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectam a um computador remoto.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Use o nome de usuário e a senha como as credenciais. Defina esse sinalizador ao criar um objeto [**ConnectionOptions**](connectionoptions.md) e fornecer o [**nome de usuário**](connectionoptions-username.md) e a [**senha**](connectionoptions-password.md). As credenciais podem ser uma conta de domínio ou uma conta no computador local. Por padrão, a conta deve ser um membro do grupo local de administradores no computador local ou remoto. No entanto, o serviço WinRM pode ser configurado para permitir outros usuários. para obter mais informações, consulte [instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md). você pode definir esse sinalizador ao especificar credenciais para autenticação de negociação (também conhecida como [*autenticação integrada Windows*](windows-remote-management-glossary.md)) ou para [*autenticação básica*](windows-remote-management-glossary.md).

O método de script associado é [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)e o método C++ é [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Ao se conectar via HTTPS, o cliente não valida se o certificado do servidor está assinado por uma autoridade de certificação (CA) confiável. Use esse valor somente quando o computador remoto for confiável por outros meios, por exemplo, se o computador remoto fizer parte de uma rede que esteja fisicamente segura e isolada ou o computador remoto estiver listado como um host confiável na configuração do WinRM.

O método de script associado é [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)e o método C++ é [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Ao se conectar via HTTPS, o cliente não validará que o CN (nome comum) no certificado do servidor corresponde ao nome do computador na cadeia de conexão. Use somente quando o computador remoto for confiável por outros meios, por exemplo, se o computador remoto fizer parte de uma rede fisicamente segura e isolada ou se o computador remoto estiver listado como um host confiável na configuração do WinRM.

O método de script associado é [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)e o método C++ é [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



Não use nenhuma autenticação. Especifique essa constante ao testar uma conexão com um computador remoto para determinar se um serviço que implementa o protocolo de WS-Management está configurado para escutar solicitações de dados. **WSManFlagUseNoAuthentication** não pode ser combinado com nenhuma outra constante de [**sessão**](session.md) . O método de script associado é [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)e o método C++ é [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Use a autenticação Digest. Apenas o computador cliente pode iniciar uma solicitação de autenticação Digest. O cliente envia uma solicitação ao servidor para autenticar e receber uma cadeia de caracteres de token do servidor. Em seguida, o cliente envia a solicitação de recurso, incluindo o nome de usuário e um hash criptográfico da senha combinada com a cadeia de caracteres do token. A autenticação Digest tem suporte para HTTP e HTTPS. Os aplicativos e scripts do cliente WinRM podem especificar a autenticação Digest, mas não o serviço.

O método de script associado é [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)e o método C++ é [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Use a autenticação de negociação. O cliente envia uma solicitação ao servidor para autenticar. O servidor determina se o Kerberos ou NTLM deve ser usado. O Kerberos está selecionado para autenticar uma conta de domínio e o NTLM está selecionado para contas de computador local. O nome de usuário deve ser especificado no formato domínio \\ nome de usuário para um domínio user ou ServerName \\ username para um usuário local em um computador servidor.

O [UAC (controle de conta de usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afeta o acesso ao serviço WinRM. Quando a autenticação de negociação é usada em um grupo de trabalho ou domínio, somente a conta de administrador interno pode acessar o serviço. para permitir que todas as contas no grupo administradores acessem o serviço, defina a seguinte chave do registro como 1: **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ policies \\ system \\ LocalAccountTokenFilterPolicy**.

O método de script associado é [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)e o método C++ é [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Use a autenticação básica. O cliente apresenta credenciais na forma de um nome de usuário e senha, transmitidos diretamente na mensagem de solicitação. Você pode especificar apenas as credenciais que identificam uma conta de administrador local no computador remoto.

O método de script associado é [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)e o método C++ é [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Usar a autenticação Kerberos. O cliente e o servidor se autenticam mutuamente usando tíquetes Kerberos.

O método de script associado é [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)e o método C++ é [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Não use criptografia. O tráfego não criptografado não é permitido por padrão e deve ser habilitado no cliente e no servidor.

O método de script associado é [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)e o método C++ é [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Use a autenticação baseada em certificado do cliente.

O método de script associado é [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)e o método C++ é [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Use a autenticação do Credential Security Support Provider (CredSSP).

O método de script associado é [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)e o método C++ é [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Não verificar revogação de certificado durante a autenticação.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Permitir credenciais implícitas.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



Usar camada de soquete seguro, habilita HTTPS.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de sessão](session-constants.md)
</dt> </dl>

 

 





