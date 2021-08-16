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
ms.openlocfilehash: b9faf923cf6c771e95a7dfb4f0b04f896c54d79c6b5548e97850d867057b065b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834643"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método JoinDomainOrWorkgroup da classe \_ ComputerSystem win32

O **método JoinDomainOrWorkgroup** une um sistema de computador a um domínio ou grupo de trabalho.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

*Nome* \[ Em\]
</dt> <dd>

Especifica o domínio ou grupo de trabalho a ingressar. Não pode ser **NULL.**

</dd> <dt>

*Senha* \[ Em\]
</dt> <dd>

Se o *parâmetro UserName* especificar um nome de conta, o parâmetro *Password* deverá apontar para a senha a ser usada ao se conectar ao controlador de domínio. Caso contrário, esse parâmetro deve ser **NULL.**

</dd> <dt>

*UserName* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia **de** caracteres terminada em nulo constante que especifica o nome da conta a ser usado ao se conectar ao controlador de domínio. Deve especificar um nome netBIOS de domínio e uma conta de usuário, por exemplo, Usuário de \\ domínio. Se esse parâmetro for **NULL,** as informações do chamador são usadas.

Você também pode usar o nome UPPED no formato user@domain .

</dd> <dt>

*AccountOU* \[ Em\]
</dt> <dd>

Especifica o ponteiro para uma cadeia de caracteres terminada em nulo constante que contém o nome de formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) da UO (unidade organizacional) da conta do computador. Se você especificar esse parâmetro, a cadeia de caracteres deverá conter um caminho completo; caso contrário, *Accent* deverá ser **NULL.**

Exemplo: "OU=testOU; DC=domain; DC=Domain; DC=com"

</dd> <dt>

*FJoinOptions* \[ Em\]
</dt> <dd>

Conjunto de sinalizadores de bits que definem as opções de junção.

<dt>



  acima (0)


</dt> <dd>

Padrão. Nenhuma opção de junção.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_ JOIN \_ DOMAIN** (0x00000001)


</dt> <dd>

Une o computador a um domínio. Se esse valor não for especificado, unirá o computador a um grupo de trabalho.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_ ACCT \_ CREATE** (0x00000002)


</dt> <dd>

Cria a conta no domínio.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ WIN9X \_ UPGRADE** (0x00000010)


</dt> <dd>

A operação de junção está ocorrendo como parte de uma atualização.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_ INGRESSO \_ NO DOMÍNIO SE \_ \_ INGRESSADO** (0X00000020)


</dt> <dd>

Permite uma junção a um novo domínio mesmo que o computador já tenha ingressado em um domínio.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_ JOIN \_ UNSECURE** (0x00000040)


</dt> <dd>

Executa uma junção não segura.

Essa opção solicita uma junção de domínio para uma conta pré-criada sem autenticar com credenciais de usuário de domínio. Essa opção pode ser usada em conjunto com a **opção NETSETUP \_ MACHINE \_ PWD \_ PASSED.** Nesse caso, *Senha é* a senha da conta de computador pré-criada.

Antes de Windows Vista com SP1 e Windows Server 2008, uma junção não seguro não era autenticada no controlador de domínio. Toda a comunicação foi executada usando uma sessão nula (não autenticada). A partir do Windows Vista com SP1 e Windows Server 2008, o nome e a senha da conta do computador são usados para autenticar no controlador de domínio.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_ MACHINE \_ PWD \_ PASSED** (0x00000080)


</dt> <dd>

Indica que o parâmetro *Password* especifica uma senha de conta de computador local em vez de uma senha de usuário. Esse sinalizador é válido somente para junções não asseguradas, que você deve indicar também definindo o sinalizador NETSETUP \_ JOIN \_ UNSECURE.

Se você definir esse sinalizador, depois que a operação de junção for bem-sucedida, a senha do computador será definida como o valor de *Senha*, se esse valor for uma senha de computador válida.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_ DEFER \_ SPN \_ SET** (0x00000100)


</dt> <dd>

Indica que o SPN (nome da entidade de serviço) e as propriedades DnsHostName no objeto de computador não devem ser atualizadas no momento.

Normalmente, essas propriedades são atualizadas durante a operação de junção. Em vez disso, essas propriedades devem ser atualizadas durante uma chamada subsequente para o [**método Renomear.**](rename-method-in-class-win32-computersystem.md) Essas propriedades são sempre atualizadas durante a operação de renomear.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_ JOIN \_ DC \_ ACCOUNT** (0x00000200)


</dt> <dd>

Permitir a junção de domínio se a conta existente for um controlador de domínio.

> [!Note]  
> Esse sinalizador tem suporte no Windows Vista e posterior.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_ \_DC AMBÍGUO** (0x00001000)


</dt> <dd>

Ao ingressar no domínio, não tente definir o controlador de domínio preferencial no Registro.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_ NENHUM \_ CACHE NETLOGON \_** (0x00002000)


</dt> <dd>

Ao ingressar no domínio, não crie o cache Netlogon.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_ DONT \_ CONTROL \_ SERVICES** (0X00004000)


</dt> <dd>

Ao ingressar no domínio, não force o início do serviço Netlogon.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_ SET \_ MACHINE \_ NAME** (0x00008000)


</dt> <dd>

Ao ingressar no domínio somente para junção offline, de definido o nome do host do computador de destino e o nome NetBIOS.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_ FORCE \_ SPN \_ SET** (0x00010000)


</dt> <dd>

Ao ingressar no domínio, substitua outras configurações durante a junção de domínio e de definir o SPN (nome da entidade de serviço).

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_ NO \_ ACCT \_ REUSE** (0x00020000)


</dt> <dd>

Ao ingressar no domínio, não reutilizar uma conta existente.

> [!Note]  
> Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_ IGNORAR \_ SINALIZADORES SEM \_ SUPORTE** (0X10000000)


</dt> <dd>

Se esse bit estiver definido, os sinalizadores não marcados serão ignorados pela função **JoinDomainOrWorkgroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comportará como se os sinalizadores não fossem definidos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um [código de erro do sistema](/windows/desktop/Debug/system-error-codes), que pode incluir um dos seguintes valores numéricos. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Êxito**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

Acesso negado.

</dd> <dt>

**87**
</dt> <dd>

O parâmetro está incorreto.

</dd> <dt>

**110**
</dt> <dd>

O sistema não pode abrir o objeto especificado.

</dd> <dt>

**1323**
</dt> <dd>

Não é possível atualizar a senha.

</dd> <dt>

**1326**
</dt> <dd>

Falha de logon: nome de usuário desconhecido ou senha incorreta.

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

O computador já está ingressado no domínio.

</dd> <dt>

**2692**
</dt> <dd>

No momento, o computador não está ingressado em um domínio.

</dd> <dt>

**CONEXÃO \_ CRIPTOGRAFADA DO WBEM E \_ \_ \_ NECESSÁRIA**
</dt> <dd>

0x80041087

*Senha* e *UserName são* especificados, mas o nível de autenticação não é **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Por Visual Basic, **wbemErrEncryptedConnectionRequired** é retornado.

</dd> <dt>

**Outras**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao mover um computador de um domínio para um grupo de trabalho, você deve remover o computador do domínio (com uma chamada para [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) antes de chamar esse método para ingressar em um grupo de trabalho (com uma chamada para **JoinDomainOrWorkgroup**). Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.

*UserName* e *Password podem* ser deixados **nulos.** No entanto, a autenticação da conexão com o WMI deve ser 6 no script ou **WbemAuthenticationLevelPktPrivacy** no Visual Basic e em outras linguagens que podem usar [a bibliotecawbemdisp.dll.](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) Para obter mais informações, consulte Definindo o nível de segurança [do processo padrão usando o VBScript.](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript)

No C++, de definido a autenticação em **\_ RPC C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** em [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), para todo o processo ou em [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), para uma conexão com o proxy [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Para obter mais informações, consulte Configurando a autenticação [usando C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e Definindo a segurança em [IWbemServices e outros proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Exemplos

O [exemplo Ingressar um computador em um domínio do](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell une um computador a um domínio.

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
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Método UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

