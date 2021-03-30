---
description: Une um sistema de computador a um domínio ou grupo de trabalho.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Método JoinDomainOrWorkgroup da classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826593"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método JoinDomainOrWorkgroup da classe Win32 \_ ComputerSystem

O método **JoinDomainOrWorkgroup** une um sistema de computador a um domínio ou grupo de trabalho.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Especifica o domínio ou grupo de trabalho a ser associado. Não pode ser **nulo**.

</dd> <dt>

*Senha* \[ do no\]
</dt> <dd>

Se o parâmetro *username* especificar um nome de conta, o parâmetro *password* deverá apontar para a senha a ser usada na conexão com o controlador de domínio. Caso contrário, esse parâmetro deve ser **nulo**.

</dd> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres constante terminada em **nulo** que especifica o nome da conta a ser usada ao conectar-se ao controlador de domínio. É necessário especificar um nome NetBIOS de domínio e uma conta de usuário, por exemplo, usuário de domínio \\ . Se esse parâmetro for **nulo**, as informações do chamador serão usadas.

Você também pode usar o nome principal do usuário (UPPED) no formulário user@domain .

</dd> <dt>

*AccountOU* \[ no\]
</dt> <dd>

Especifica o ponteiro para uma cadeia de caracteres constante terminada em **nulo** que contém o nome do formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) da unidade organizacional (UO) da conta do computador. Se você especificar esse parâmetro, a cadeia de caracteres deverá conter um caminho completo; caso contrário, o *acento* deve ser **nulo**.

Exemplo: "OU = testOU; DC = Domain; DC = Domain; DC = com "

</dd> <dt>

*FJoinOptions* \[ no\]
</dt> <dd>

Conjunto de sinalizadores de bits que definem as opções de junção.

<dt>



  acima (0)


</dt> <dd>

Padrão. Nenhuma opção de junção.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>INSTALAÇÃO do NET **\_ INGRESSAr no \_ domínio** (0x00000001)


</dt> <dd>

Une o computador a um domínio. Se esse valor não for especificado, o ingressará o computador em um grupo de trabalho.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>INSTALAÇÃO do NET **\_ \_Create de acct** (0x00000002)


</dt> <dd>

Cria a conta no domínio.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>INSTALAÇÃO do NET **\_ \_Atualização do Win9x** (0x00000010)


</dt> <dd>

A operação de junção está ocorrendo como parte de uma atualização.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>INSTALAÇÃO do NET **\_ Ingresso no domínio \_ \_ se \_ Unido** (0x00000020)


</dt> <dd>

Permite uma junção a um novo domínio, mesmo que o computador já tenha ingressado em um domínio.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>INSTALAÇÃO do NET **\_ JUNÇÃO \_ não segura** (0x00000040)


</dt> <dd>

Executa uma junção não segura.

Esta opção solicita um ingresso no domínio para uma conta criada previamente sem autenticação com credenciais de usuário do domínio. Essa opção pode ser usada em conjunto com a opção de **instalação do \_ computador \_ pwd \_ aprovada** . Nesse caso, *password* é a senha da conta de máquina criada previamente.

Antes do Windows Vista com SP1 e do Windows Server 2008, uma junção não segura não se autenticou no controlador de domínio. Toda a comunicação foi executada usando uma sessão nula (não autenticada). A partir do Windows Vista com SP1 e do Windows Server 2008, o nome da conta de computador e a senha são usados para autenticar no controlador de domínio.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>INSTALAÇÃO do NET **\_ PWD do computador \_ \_ aprovado** (0x00000080)


</dt> <dd>

Indica que o parâmetro de *senha* especifica uma senha de conta de computador local, em vez de uma senha de usuário. Esse sinalizador é válido somente para junções não seguras, que você deve indicar, definindo também o \_ sinalizador de junção não segura do Netsetup \_ .

Se você definir esse sinalizador, depois que a operação de junção for concluída com sucesso, a senha do computador será definida como o valor de *senha*, se esse valor for uma senha de computador válida.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>INSTALAÇÃO do NET **\_ ADIAr \_ \_ conjunto de SPN** (0x00000100)


</dt> <dd>

Indica que o SPN (nome da entidade de serviço) e as propriedades de DnsHostName no objeto de computador não devem ser atualizados no momento.

Normalmente, essas propriedades são atualizadas durante a operação de junção. Em vez disso, essas propriedades devem ser atualizadas durante uma chamada subsequente para o método [**Rename**](rename-method-in-class-win32-computersystem.md) . Essas propriedades são sempre atualizadas durante a operação de renomeação.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>INSTALAÇÃO do NET **\_ INGRESSAr na \_ \_ conta DC** (0x00000200)


</dt> <dd>

Permitir ingresso no domínio se a conta existente for um controlador de domínio.

> [!Note]  
> Esse sinalizador tem suporte no Windows Vista e versões posteriores.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>INSTALAÇÃO do NET **\_ \_DC ambíguo** (0x00001000)


</dt> <dd>

Ao ingressar no domínio, não tente definir o controlador de domínio preferencial no registro.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>INSTALAÇÃO do NET **\_ NENHUM \_ \_ cache Netlogon** (0x00002000)


</dt> <dd>

Ao ingressar no domínio, não crie o cache Netlogon.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>INSTALAÇÃO do NET **\_ Não 0x00004000 ( \_ \_ serviços de controle** )


</dt> <dd>

Ao ingressar no domínio, não force o início do serviço Netlogon.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>INSTALAÇÃO do NET **\_ DEFINIR \_ \_ nome do computador** (0x00008000)


</dt> <dd>

Ao ingressar no domínio somente para junção offline, defina nome de host do computador de destino e NetBIOS.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>INSTALAÇÃO do NET **\_ FORÇAR \_ \_ conjunto de SPN** (0x00010000)


</dt> <dd>

Ao ingressar no domínio, substitua outras configurações durante o ingresso no domínio e defina o SPN (nome da entidade de serviço).

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>INSTALAÇÃO do NET **\_ NENHUMA \_ \_ reutilização de acct** (0x00020000)


</dt> <dd>

Ao ingressar no domínio, não reutilize uma conta existente.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>INSTALAÇÃO do NET **\_ IGNORAR \_ \_ sinalizadores sem suporte** (0x10000000)


</dt> <dd>

Se esse bit for definido, os sinalizadores não reconhecidos serão ignorados pela função **JoinDomainOrWorkgroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comportará como se os sinalizadores não fossem definidos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um [código de erro do sistema](/windows/desktop/Debug/system-error-codes), que pode incluir um dos valores numéricos a seguir. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Êxito**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

O acesso foi negado.

</dd> <dt>

**87**
</dt> <dd>

O parâmetro está incorreto.

</dd> <dt>

**110**
</dt> <dd>

o sistema não pode abrir o objeto especificado.

</dd> <dt>

**1323**
</dt> <dd>

Não é possível atualizar a senha.

</dd> <dt>

**1326**
</dt> <dd>

Falha de logon: nome de usuário desconhecido ou senha inadequada.

</dd> <dt>

**1355**
</dt> <dd>

O domínio especificado não existe ou não pôde ser contatado.

</dd> <dt>

**2224**
</dt> <dd>

A conta já existe.

</dd> <dt>

**2691**
</dt> <dd>

O computador já ingressou no domínio.

</dd> <dt>

**2692**
</dt> <dd>

O computador não está atualmente associado a um domínio.

</dd> <dt>

**conexão de WBEM \_ E \_ criptografada \_ \_ necessária**
</dt> <dd>

0x80041087

A *senha* e o *nome de usuário* são especificados, mas o nível de autenticação não é do **RPC \_ C \_ Authn \_ nível de \_ \_ privacidade de PCT**. Por Visual Basic, **wbemErrEncryptedConnectionRequired** é retornado.

</dd> <dt>

**Outras**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao mover um computador de um domínio para um grupo de trabalho, você deve remover o computador do domínio (com uma chamada para [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) antes de chamar esse método para ingressar em um grupo de trabalho (com uma chamada para **JoinDomainOrWorkgroup**). Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.

O *nome de usuário* e a *senha* podem ser **nulos**. No entanto, a autenticação da conexão com o WMI deve ser 6 em script ou **WbemAuthenticationLevelPktPrivacy** no Visual Basic e em outras linguagens que podem usar a biblioteca de [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) . Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

Em C++, defina a autenticação na **\_ privacidade do \_ PCT do \_ nível \_ \_ de autenticação do RPC C** em [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), para todo o processo ou em [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), para uma conexão com o proxy de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Para obter mais informações, consulte [definindo a autenticação usando C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e [definindo a segurança em IWbemServices e em outros proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Exemplos

O exemplo [ingressar um computador em um domínio](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) do PowerShell une um computador a um domínio.

O exemplo de código VBScript a seguir une um computador a um domínio e cria a conta do computador no Active Directory.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Sistema de ComputerSystem Win32**](win32-computersystem.md)
</dt> <dt>

[**Método UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

